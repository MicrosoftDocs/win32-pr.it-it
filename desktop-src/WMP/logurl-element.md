---
title: Elemento LOGURL
description: L'elemento LOGURL indica a Windows Media Player di inviare i dati di log all'URL specificato.
ms.assetid: fc1895af-c9d7-43ca-9839-7e884cc219f4
keywords:
- Finestra elementi LOGURL Media Player
topic_type:
- apiref
api_name:
- LOGURL Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0f5fc4a5259f009e7298c0609fc4e6fa8c533b94
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327718"
---
# <a name="logurl-element"></a>Elemento LOGURL

L'elemento **LogURL** indica a Windows Media Player di inviare i dati di log all'URL specificato.

``` syntax
<LOGURL
   HREF = "URL"
/>
```

## <a name="attributes"></a>Attributi

**Href** (obbligatorio)

URL di un host in grado di elaborare le richieste di registrazione.

## <a name="parentchild-elements"></a>Elementi padre/figlio



| Gerarchia       | Elementi           |
|-----------------|--------------------|
| Elementi padre | **ASX**, **voce** |
| Elementi figlio  | nessuno               |



 

## <a name="remarks"></a>Osservazioni

L'elemento **LogURL** consente a una playlist del metafile client di inviare informazioni di registrazione aggiuntive ai server specificati. Le informazioni di registrazione vengono inviate automaticamente al server di origine di una playlist quando viene aperto e a ogni **LogURL** specificato per l'elemento **ASX** , se presenti. Le informazioni di registrazione vengono inviate anche a ogni **LogURL** specificato per un elemento **entry** quando viene raggiunta tale voce. L'URL specificato nell'attributo **href** di un elemento **LogURL** deve essere l'indirizzo di un host in grado di elaborare le richieste di registrazione. L'URL può essere qualsiasi URL HTTP valido. L'URL può anche indicare la posizione di uno script CGI.

Gli unici protocolli validi per un elemento **LogURL** sono http e HTTPS.

Un elemento **LogURL** all'interno dell'ambito di un elemento **ASX** è applicabile solo al metafile in cui risiede, indipendentemente dal fatto che venga fatto riferimento a tale metafile da un altro metafile. Un elemento **LogURL** forza l'invio di dati di log per tutto il contenuto trasmesso dall'interno dell'ambito definito e solo per il contenuto trasmesso dall'interno dell'ambito definito. I dati di log verranno inviati al server di origine e a tutti gli URL elencati in ogni elemento **LogURL** nell'ambito. I dati del log verranno inviati solo una volta a ogni URL elencato, anche se lo stesso URL è elencato più di una volta in un determinato ambito. Una ripetizione di una **voce** comporterebbe un altro invio agli URL elencati.

Non esiste alcun limite al numero di elementi **LogURL** in una playlist del metafile.

## <a name="examples"></a>Esempio


```XML
<ASX VERSION="3.0">
  <TITLE>Example Media Player Show</TITLE>
  <LOGURL HREF="https://example.microsoft.com/info/showlog.asp?whatsup" />
  <ENTRY>
    <REF href="mms://ucast.proseware.com/Media1.asf" />
    <LOGURL HREF="https://www.proseware.com/cgi-bin/logging.pl?SomeArg=SomeVal"/>
  </ENTRY>
</ASX>
```



Di seguito sono riportati alcuni esempi di URL validi.

URL di un'applicazione ISAPI:


```XML
https://www.proseware.com/logs/WMSLogging.dll
```



URL di uno script CGI:


```XML
https://www.proseware.com/cgi-bin/My_WMS_Logging_Script.pl
```



Un URL HTTP valido:


```XML
https://www.proseware.com/some/arbitrary/path/My_WMS_Logging_Page.asp?PubPoint=FooPubPoint&AnotherName=AnotherValue
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------|
| Versione<br/> | Windows Media Player versione 70 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Riferimento agli elementi metafile di Windows Media**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Informazioni di riferimento sui metafile di Windows Media**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





