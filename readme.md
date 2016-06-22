# Wonde PHP Client
Documentation https://wonde.com/docs/api/1.0/

## Installation

Requires PHP 5.6.

Using Composer:

```json
{
    "require": {
      "wondeltd/php-client": "1.*"
    }
}
```

or 
```bash
composer require wondeltd/php-client
```


### Client

```php
$client = new \Wonde\Client('TOKEN_GOES_HERE');
```

### Schools

```php
$client = new \Wonde\Client('TOKEN_GOES_HERE');

// Loop through the schools your account has access to
foreach ($client->schools->all() as $school) {
    // Display school name
    echo $school->name . PHP_EOL;
}
```

### Students

```php
$client = new \Wonde\Client('TOKEN_GOES_HERE');

$school = $client->school('SCHOOL_ID_GOES_HERE');

// Get students
foreach ($school->students->all() as $student) {
    echo $students->forename . ' ' . $students->surname . PHP_EOL;
}

// Get single student
$student = $school->students->get('STUDENT_ID_GOES_HERE');

// Get students and include contact_details object
foreach ($school->students->all(['contact_details']) as $student) {
    echo $students->forename . ' ' . $students->surname . PHP_EOL;
}

// Get students and include contacts array
foreach ($school->students->all(['contacts']) as $student) {
    echo $students->forename . ' ' . $students->surname . PHP_EOL;
}

// Get students, include contact_details object, include extended_details object and filter by updated after date
foreach ($school->students->all(['contact_details', 'extended_details'], ['updated_after' => '2016-06-24 00:00:00']) as $student) {
    echo $students->forename . ' ' . $students->surname . PHP_EOL;
}
```

### Achievements

```php
$client = new \Wonde\Client('TOKEN_GOES_HERE');

$school = $client->school('SCHOOL_ID_GOES_HERE');

// Get achievements
foreach ($school->achievements->all() as $achievement) {
    echo $achievement->comment . PHP_EOL;
}
```

### Attendance

```php
$client = new \Wonde\Client('TOKEN_GOES_HERE');

$school = $client->school('SCHOOL_ID_GOES_HERE');

// Get attendance
foreach ($school->attendance->all() as $attendance) {
    echo $attendance->comment . PHP_EOL;
}
```

### Attendance Codes

```php
$client = new \Wonde\Client('TOKEN_GOES_HERE');

$school = $client->school('SCHOOL_ID_GOES_HERE');

// Get attendance codes
foreach ($client->attendanceCodes->all() as $attendanceCode) {
    echo $attendanceCode->code . PHP_EOL;
 }
```

### Behaviours

```php
$client = new \Wonde\Client('TOKEN_GOES_HERE');

$school = $client->school('SCHOOL_ID_GOES_HERE');

// Get behaviours
foreach ($school->behaviours->all() as $behaviour) {
    echo $behaviour->incident . PHP_EOL;
}
```

### Classes

```php
$client = new \Wonde\Client('TOKEN_GOES_HERE');

$school = $client->school('SCHOOL_ID_GOES_HERE');

// Get classes
foreach ($school->classes->all() as $class) {
    echo $class->name . PHP_EOL;
}
```

### Contacts

```php
$client = new \Wonde\Client('TOKEN_GOES_HERE');

$school = $client->school('SCHOOL_ID_GOES_HERE');

// Get contacts
foreach ($school->contacts->all() as $contacts) {
    echo $contacts->forename . ' ' . $contacts->surname . PHP_EOL;
}
```

### Employees

```php
$client = new \Wonde\Client('TOKEN_GOES_HERE');

$school = $client->school('SCHOOL_ID_GOES_HERE');

// Get employees
foreach ($school->employees->all() as $employee) {
    echo $employee->forename . ' ' . $employee->surname . PHP_EOL;
}
```

### Groups

```php
$client = new \Wonde\Client('TOKEN_GOES_HERE');

$school = $client->school('SCHOOL_ID_GOES_HERE');

// Get groups
foreach ($school->groups->all() as $group) {
    echo $group->name . PHP_EOL;
}
```

### Lessons

```php
$client = new \Wonde\Client('TOKEN_GOES_HERE');

$school = $client->school('SCHOOL_ID_GOES_HERE');

// Get lessons
foreach ($school->lessons->all() as $lesson) {
    echo $lesson->period_id . '-' . $lesson->class_id . PHP_EOL;
}
```

### Lesson Attendance

```php
$client = new \Wonde\Client('TOKEN_GOES_HERE');

$school = $client->school('SCHOOL_ID_GOES_HERE');

// Get lesson attendance
foreach ($school->lessonAttendance->all() as $lessonAttendance) {
    echo $lessonAttendance->comment . PHP_EOL;
}
```

### Medical Conditions

```php
$client = new \Wonde\Client('TOKEN_GOES_HERE');

$school = $client->school('SCHOOL_ID_GOES_HERE');

// Get medical conditions
foreach ($school->medicalConditions->all() as $medicalCondition) {
    echo $medicalCondition->description . PHP_EOL;
}
```

### Medical Events

```php
$client = new \Wonde\Client('TOKEN_GOES_HERE');

$school = $client->school('SCHOOL_ID_GOES_HERE');

// Get medical events
foreach ($school->medicalEvents->all() as $medicalEvent) {
    echo $medicalEvent->description . PHP_EOL;
}
```

### Periods

```php
$client = new \Wonde\Client('TOKEN_GOES_HERE');

$school = $client->school('SCHOOL_ID_GOES_HERE');

// Get periods
foreach ($school->periods->all() as $period) {
    echo $period->name . PHP_EOL;
}
```

### Photos

```php
$client = new \Wonde\Client('TOKEN_GOES_HERE');

$school = $client->school('SCHOOL_ID_GOES_HERE');

// Get photos
foreach ($school->photos->all() as $photo) {
    echo $photo->hash . PHP_EOL;
}
```

### Rooms

```php
$client = new \Wonde\Client('TOKEN_GOES_HERE');

$school = $client->school('SCHOOL_ID_GOES_HERE');

// Get rooms
foreach ($school->rooms->all() as $room) {
    echo $room->name . PHP_EOL;
}
```

### Subjects

```php
$client = new \Wonde\Client('TOKEN_GOES_HERE');

$school = $client->school('SCHOOL_ID_GOES_HERE');

// Get subjects
foreach ($school->subjects->all() as $subject) {
    echo $subject->name . PHP_EOL;
}
```
