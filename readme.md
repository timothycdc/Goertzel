Goertzel
========

Arduino Library implementation of the Goertzel algorithm, originally written by [jacobrosenthal](https://github.com/jacobrosenthal/Goertzel). Adapted fixes for running on an SAMD Arduino Metro M0



Example
-------

```cpp
void loop()
{
  goertzel.sample(sensorPin); //Will take n samples
  
  float magnitude = goertzel.detect();  //check them for target_freq
  
  if(magnitude>THRESHOLD) //if you're getting false hits or no hits adjust this
    digitalWrite(led, HIGH); //if found, enable led
  else
    digitalWrite(led, LOW); //if not found, or lost, disable led
    
  Serial.println(magnitude);
}
```



