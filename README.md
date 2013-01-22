to test in the rubymotion console :
```ruby
xmlList = '<?xml version="1.0" encoding="UTF-8"?><events generator="localhost:3000" version="1"><exported>2013-01-22T15:33:45+01:00</exported><event id="app-here"><title>app here</title></events>'
errorPtr = Pointer.new(:object)
xml = TBXML.alloc.initWithXMLString(xmlList, error:errorPtr)
puts errorPtr[0] # returns nil
# failed : Can't find pointer description for type `{_TBXMLElement=**^{_TBXMLAttribute}^{_TBXMLElement}^{_TBXMLElement}^{_TBXMLElement}^{_TBXMLElement}^{_TBXMLElement}}'
evts = xml.rootXMLElement
```