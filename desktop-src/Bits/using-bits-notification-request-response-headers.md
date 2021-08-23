---
title: Uso delle intestazioni di richiesta/risposta di notifica BITS
description: BITS può inviare il percorso del file di caricamento (per riferimento) all'applicazione server oppure può inviare il file di caricamento nel corpo della richiesta (per valore).
ms.assetid: b80f9077-54e7-4d10-909a-dee7d8822627
ms.topic: article
ms.date: 11/29/2018
ms.openlocfilehash: 3db568f483468cbc92474f24f830da5bf1be94a2165cbb69a2d1751cc58965dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119021069"
---
# <a name="using-bits-notification-requestresponse-headers"></a>Uso delle intestazioni di richiesta/risposta di notifica BITS

BITS può inviare il percorso del file di caricamento (per riferimento) all'applicazione server oppure può inviare il file di caricamento nel corpo della richiesta (per valore). Per specificare il modo in cui BITS invia il file di caricamento all'applicazione server, impostare la proprietà della metabase IIS [**BITSServerNotificationType**](bits-iis-extension-properties.md). Se si specifica per riferimento, BITS passa il percorso del file nell'intestazione BITS-Request-DataFile-Name. Per inviare una risposta, creare e scrivere la risposta nel file specificato nell'intestazione BITS-Response-DataFile-Name.

Le applicazioni server che inviano la stessa risposta a molti client devono usare per riferimento, pertanto nel server è presente una sola copia della risposta. Ad esempio, in un'applicazione di aggiornamento software, il client carica la configurazione software nell'applicazione server. L'applicazione server determina il pacchetto necessario al client e invia l'URL del pacchetto a BITS. BITS scarica quindi il pacchetto come risposta.

Le applicazioni server che generano risposte univoche per ogni client devono usare per valore. Ad esempio, un'applicazione server che supporta l'acquisto di file musicali dovrà inviare un file musicale firmato al client. Poiché il file musicale firmato è univoco per il client, l'applicazione server non lo archivierebbe nel server. Per valore è utile anche per un'applicazione già scritta per accettare direttamente i dati del client Web.

Per informazioni dettagliate sulle intestazioni di richiesta e risposta usate tra BITS e l'applicazione server, vedere [Protocollo di notifica per applicazioni server.](notification-protocol-for-server-applications.md)

L'esempio JavaScript seguente illustra come accedere ai file di richiesta e risposta in un'applicazione server che usa per notifica di riferimento (BITS passa il percorso dei file nelle intestazioni).


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



Se si vuole usare un file di risposta diverso da quello specificato in BITS-Response-DataFile-Name, chiamare il metodo **Response.AddHeader** per aggiungere BITS-Static-Response-URL, come illustrato nell'esempio seguente. Se si specifica un file di risposta diverso, non creare il file di risposta specificato in BITS-Response-DataFile-Name.


```JavaScript
  Response.AddHeader "BITS-Static-Response-URL" "https://myserver/mypath/myfile"
```
 

 




