# Evolution CMS Reflected XSS v3.2.3

## Author: (Sergio)

**Description:** A cross-site scripting (XSS) reflected vulnerability in the evolution v.3.2.3 installation process connection allows a local attacker to execute arbitrary web scripts via a crafted payload injected into the uid parameter.

**Attack Vectors:** A vulnerability in the sanitization of the uid parameter of the Database installation process allows JavaScript code to be injected.

---

### POC:


During the installation process we enter the XSS payload in the uid parameter and when we click on next, we will obtain the XSS pop-up.

### XSS Payload:

```js
'"><svg/onload=alert('XSS')>
```


In the following image you can see the embedded code that executes the payload in the instalaltion process.
![XSS Payloadpng](https://github.com/sromanhu/Evolution-Reflected-XSS---Installation-Connection-/assets/87250597/7167dff2-6212-40c0-b8fd-b68fd1e7b623)


And the result will be reflected with the pop-up of the following evidence:

![XSS Resultado](https://github.com/sromanhu/Evolution-Reflected-XSS---Installation-Connection-/assets/87250597/74cc29b8-585a-4db5-880b-107f755be5ea)



</br>

### Additional Information:

https://evo.im/

