---
title: Registrazione client (Windows Media Format 11 SDK)
description: Informazioni sulla registrazione client per Windows Media Format 11 SDK. La registrazione consente al server multimediale di tenere traccia dell'attività dei client che si connettono al server.
ms.assetid: 3e0d0fea-4370-41f8-b461-73a37de8d8bc
keywords:
- Windows Media Format SDK, registrazione client
- Windows Media Format SDK, registrazione
- Advanced Systems Format (ASF), registrazione client
- ASF (Advanced Systems Format), registrazione client
- Advanced Systems Format (ASF), registrazione
- ASF (Advanced Systems Format),registrazione
- registrazione client
- client di registrazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 460058d6ad4009fab301c6ce322df3144bdd0e5d9bb4732d54126f7675cd9e2a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119028029"
---
# <a name="client-logging-windows-media-format-11-sdk"></a>Registrazione client (Windows Media Format 11 SDK)

Quando l'oggetto lettore legge i dati da un server, invia le informazioni di registrazione al server. I provider di contenuti usano in genere queste informazioni per misurare la qualità del servizio, generare informazioni di fatturazione o tenere traccia della pubblicità. Le informazioni di registrazione non contengono dati personali.

L'applicazione può specificare alcune delle informazioni registrate chiamando il metodo [**IWMReaderAdvanced::SetClientInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setclientinfo) sull'oggetto reader. Ad esempio, è possibile specificare la stringa agente utente, il nome dell'applicazione lettore o la pagina Web che ospita il lettore.

Le informazioni di registrazione includono un GUID che identifica la sessione. Per impostazione predefinita, il lettore genera un ID sessione anonimo. Facoltativamente, il lettore può invece inviare un ID che identifica in modo univoco l'utente corrente. Per abilitare questa funzionalità, chiamare il [**metodo IWMReaderAdvanced2::SetLogClientID**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setlogclientid) con il valore **TRUE.**

È possibile configurare l'oggetto lettore per inviare le informazioni di registrazione a un altro server, oltre al server di origine. A tale scopo, chiamare il [**metodo IWMReaderNetworkConfig::AddLoggingUrl**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-addloggingurl) con l'URL del server. Questo URL deve puntare a uno script o a un eseguibile in grado di gestire le richieste HTTP GET e POST. È possibile usare Multicast e Logging Advertisement Agent (wmsiislog.dll) oppure scrivere uno script ASP o CGI personalizzato per ricevere i dati di log.

> [!Note]  
> È possibile ottenere la stessa funzionalità creando una playlist sul lato server con un **attributo logURL.**

 

Quando l'oggetto lettore invia il log, esegue le operazioni seguenti:

1.  Invia una richiesta GET vuota al server.
2.  Analizza la risposta del server per una delle stringhe seguenti:
    -   `<body><h1>NetShow ISAPI Log Dll</h1>`
    -   `<body><h1>WMS ISAPI Log Dll/0.0.0.0</h1>` dove "0.0.0.0" è qualsiasi numero di versione valido.
3.  Invia una richiesta POST con le informazioni di log.

Il codice seguente illustra uno script ASP di esempio che riceve le informazioni di registrazione e le scrive in un file:


```
<html>
<body>
<h1>WMS ISAPI Log Dll/9.00.00.00.00</h1>
<%@ Language=VBScript %>
<%
  Dim temp, i, post, file, fso

  ' Convert the binary data to a string.
  For i = 1 To Request.TotalBytes
    temp = Request.BinaryRead(1)
    pose = pose & Chr(AscB(temp))
  Next

  Set fso = createobject("Scripting.FileSystemObject")
  Set file = fso.OpenTextFile("C:\log.txt", 8, TRUE)

  file.writeline Now
  file.writeline post
  file.writeBlankLines 2 
%>
</body>
</html>
```



È possibile specificare più server per ricevere le informazioni di registrazione. è sufficiente **chiamare AddLoggingUrl una** volta con ogni URL. Per cancellare l'elenco dei server che ricevono i log, chiamare il [**metodo IWMReaderNetworkConfig::ResetLoggingUrlList.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-resetloggingurllist)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Implementazione della funzionalità di rete**](implementing-network-functionality.md)
</dt> <dt>

[**Interfaccia IWMReaderAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced)
</dt> <dt>

[**Interfaccia IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2)
</dt> </dl>

 

 




