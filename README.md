# Felipe Rank
---

> I am programmer backend and frontend, i work with web applications, with system for web, institutional sites, applications mobile. Currently i am working with Laravel and AngularJS.

---
```php
<?php

namespace Life\Felipe;

class Resume
{
	/**
	 * The my status of relationship.
	 *
	 * @var bool
	 */
	protected $relationship = false;

	/**
	 * The my birth day.
	 *
	 * @var string
	 */
	protected $birth = '1992-03-16';

	/**
	 * My age
	 *
	 * @var string
	 */
	 protected $years;

	/**
	 * The companies names  that i worked.
	 *
	 * @var array
	 */
	protected $companies = [
		[
			'name' => 'Hyperbolic',
			'function' => 'Front End Developer',
			'start' => '2012-02',
			'end' => '2014-03'
		],
		[
			'name' => 'Milagro',
			'function' => 'Front End Developer',
			'start' => '2014-06',
			'end' => '2015-08'
		],
		[
			'name' => 'Fonix',
			'function' => 'Full Stack Developer',
			'start' => '2015-08',
			'end' => '2016-02'
		],
		[
			'name' => 'Freelancer, Self- Employed',
			'function' => 'Web Developer, Full Stack',
			'start' => '2016-02',
			'end' => 'now'
		]
	];

	/**
	 * All my skills.
	 *
	 * @var array
	 */
	protected $skills = [
		'master' => [
			'PHP',
			'HTML5',
			'CSS3',
			'SASS',
			'jQuery',
			'Laravel',
			'GulpJS'
		],
		'large' => [
			'Photoshop and Illustrator',
			'API RESTfull'
		],
		'medium' => [
			'Javascript',
			'AngularJS',
			'Structure MVC',
			'System for Web'
		],
		'basic' => [
			'Mobile App',
			'Ionic Framework',
			'NodeJS'
		]
	];

	/**
	 * Create a new event.
	 *
	 */
	public function __construct()
	{
		$this->years = $this->getYears( $this->birth, date('Y-m-d'), '%y' );
		$this->companies = $this->getCompaniesThatWorked( $this->companies );
	}

	/**
	 * Treatment of estimated dates.
	 *
	 * @var string|string|string
	 * @return string
	 */
	public function getYears( $start, $end, $type = '%y Year(s), %m Month(s)' )
	{
		$primary = date_create( $start );
		$secondary = date_create( $end );
		$interval = date_diff($primary, $secondary);

		return $interval->format($type);
	}

	/**
	 * Treatment this dataset of companies that i worked.
	 *
	 * @var array
	 * @return array
	 */
	public function getCompaniesThatWorked( $companies )
	{
		if( is_array( $companies ) )
		{
			foreach( $companies as $company )
			{
				$transform[] = [
					'name' => $company[ 'name' ],
					'function' => $company[ 'function' ],
					'start' => $company[ 'start' ],
					'end' => $company[ 'end' ],
					'total' => $this->getYears( $company['start'], $company['end'])
				];
			}
		}

		return (isset( $transform ) ? $transform : null);
	}
}

```
---
> I'm looking for a challenge where I can be remembered.  
Felipe Rank - [view my Linkedin](https://br.linkedin.com/in/raank)  
raank92@gmail.com  
+55 47 9917-1875 - **Skype**: felipe-rank
