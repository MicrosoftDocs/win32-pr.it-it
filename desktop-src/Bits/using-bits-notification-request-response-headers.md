---
title: Uso delle intestazioni di richiesta/risposta per le notifiche BITS
description: BITS può inviare il percorso del file di caricamento (per riferimento) all'applicazione server oppure inviare il file di caricamento nel corpo della richiesta (per valore).
ms.assetid: b80f9077-54e7-4d10-909a-dee7d8822627
ms.topic: article
ms.date: 11/29/2018
ms.openlocfilehash: 5dcbee8b82d96a4f13db0ae4de6441e9df40ce83
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104220968"
---
# <a name="using-bits-notification-requestresponse-headers"></a>Uso delle intestazioni di richiesta/risposta per le notifiche BITS

BITS può inviare il percorso del file di caricamento (per riferimento) all'applicazione server oppure inviare il file di caricamento nel corpo della richiesta (per valore). Per specificare il modo in cui BITS invia il file di caricamento all'applicazione server, impostare la proprietà della metabase IIS [**BITSServerNotificationType**](bits-iis-extension-properties.md). Se si specifica per riferimento, BITS passa il percorso del file nell'intestazione BITS-request-DataFile-Name. Per inviare una risposta, creare e scrivere la risposta al file specificato nell'intestazione BITS-Response-DataFile-Name.

Le applicazioni server che inviano la stessa risposta a molti client devono usare per riferimento, quindi è presente una sola copia della risposta sul server. Ad esempio, in un'applicazione di aggiornamento software, il client caricherà la configurazione software nell'applicazione server. L'applicazione server determina il pacchetto necessario per il client e invia l'URL del pacchetto a BITS. BITS scarica quindi il pacchetto come risposta.

Le applicazioni server che generano risposte univoche per ogni client devono utilizzare per valore. Ad esempio, un'applicazione server che supporta l'acquisto di file musicali deve inviare un file musicale firmato al client. Poiché il file Music firmato è univoco per il client, l'applicazione server non lo archivia nel server. Per valore è utile anche per un'applicazione che è già stata scritta per accettare direttamente i dati del client Web.

Per informazioni dettagliate sulle intestazioni di richiesta e risposta usate tra BITS e l'applicazione server, vedere [protocollo di notifica per le applicazioni server](notification-protocol-for-server-applications.md).

Nell'esempio JavaScript seguente viene illustrato come accedere ai file di richiesta e risposta in un'applicazione server che utilizza la notifica di riferimento (BITS passa il percorso dei file nelle intestazioni).


```JavaScript
  var fso = new ActiveXObject ("Scripting.FileSystemObject")
  var requestFileName = Request.ServerVariables ("HTTP_BITS-Request-DataFile-Name")
  var responseFileName = Request.ServerVariables ("HTTP_BITS-Response-DataFile-Name")
  var requestStream
  var responseStream
  var ForReading = 1
  var ForWriting = 2
  var TristateUseDefault = -2

  //Open the upload data file as text stream for reading.
  requestStream = fso.OpenTextFile(requestFileName, ForReading, false, TristateUseDefault);

  //Do something with the uploaded data.

  //Close the upload stream.
  requestStream.Close()

  //Open response data file as text stream for writing.
  responseStream = fso.OpenTextFile(responseFileName, ForWriting, true, TristateUseDefault);

  //Write a response to the response file.

  //Close the response text stream
  responseStream.Close()
```



Se si vuole usare un file di risposta diverso da quello specificato in BITS-Response-DataFile-Name, chiamare il metodo **Response. AddHeader** per aggiungere bits-static-Response-URL, come illustrato nell'esempio seguente. Se si specifica un file di risposta diverso, non creare il file di risposta specificato in BITS-Response-DataFile-Name.


```JavaScript
  Response.AddHeader "BITS-Static-Response-URL" "https://myserver/mypath/myfile"
```
 

 




