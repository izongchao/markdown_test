[www.baidu.com](http://note.youdao.com/)

![image](http://note.youdao.com/favicon.ico)


```php
<?php

namespace Superwechat\Lib;

/**
 * Class Connection
 * 
 * @author xuzongchao
 *
 */
class Connection implements \ArrayAccess
{
	/**
	 * @var array
	 */
	private $container = array();
	
	/**
	 * Constructor
	 * 
	 * @param array $contents
	 */
    public function __construct(array $contents) {
        $this->container = $contents;
    }
    
    /**
     * __set
     *  
     * @param mixed $key
     * @param mixed $value
     * 
     * @return void
     */
    public function __set($key, $value){
    	$this->container[$key] = $value;
    }
    
    /**
     * __isset
     * 
     * @param mixed $key
     * 
     * @return bool
     */
    public function __isset($key){
    	return isset($this->container[$key]);
    }
    
    /**
     * __get
     * 
     * @param mixed $key
     * 
     * @return mixed
     */
    public function __get($key){
    	return isset($this->container[$key]) ? $this->container[$key] : NULL;
    }
    
    /**
     * 
     * @param unknown $offset
     * @param unknown $value
     * 
     * @return void
     */
    public function offsetSet($offset, $value) {
        if (is_null($offset)) {
            $this->container[] = $value;
        } else {
            $this->container[$offset] = $value;
        }
    }
    
    /**
     * offsetExists
     * 
     * @param mixed $offset
     * 
     * @return bool
     */
    public function offsetExists($offset) {
        return isset($this->container[$offset]);
    }
    
    /**
     * offsetUnset
     * 
     * @param mixed $offset
     * 
     * @return void
     */
    public function offsetUnset($offset) {
        unset($this->container[$offset]);
    }
    
    /**
     * offsetGet
     * 
     * @param mixed $offset
     * 
     * @return void
     */
    public function offsetGet($offset) {
        return isset($this->container[$offset]) ? $this->container[$offset] : null;
    }
	
}

```

```
graph LR
A-->B
```

```
sequenceDiagram
A->>B: How are you?
B->>A: Great!
```

```
gantt
dateFormat YYYY-MM-DD
section S1
T1: 2014-01-01, 9d
section S2
T2: 2014-01-11, 9d
section S3
T3: 2014-01-02, 9d
```
