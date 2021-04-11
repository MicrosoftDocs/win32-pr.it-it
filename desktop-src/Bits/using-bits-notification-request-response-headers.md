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
# <a name="using-bits-notification-requestresponse-headers"></a><span data-ttu-id="487fb-103">Uso delle intestazioni di richiesta/risposta per le notifiche BITS</span><span class="sxs-lookup"><span data-stu-id="487fb-103">Using BITS Notification Request/Response Headers</span></span>

<span data-ttu-id="487fb-104">BITS può inviare il percorso del file di caricamento (per riferimento) all'applicazione server oppure inviare il file di caricamento nel corpo della richiesta (per valore).</span><span class="sxs-lookup"><span data-stu-id="487fb-104">BITS can send the location of the upload file (by reference) to your server application or it can send the upload file in the body of the request (by value).</span></span> <span data-ttu-id="487fb-105">Per specificare il modo in cui BITS invia il file di caricamento all'applicazione server, impostare la proprietà della metabase IIS [**BITSServerNotificationType**](bits-iis-extension-properties.md).</span><span class="sxs-lookup"><span data-stu-id="487fb-105">To specify how BITS sends the upload file to your server application, set the IIS metabase property, [**BITSServerNotificationType**](bits-iis-extension-properties.md).</span></span> <span data-ttu-id="487fb-106">Se si specifica per riferimento, BITS passa il percorso del file nell'intestazione BITS-request-DataFile-Name.</span><span class="sxs-lookup"><span data-stu-id="487fb-106">If you specify by reference, BITS passes the location of the file in the BITS-Request-DataFile-Name header.</span></span> <span data-ttu-id="487fb-107">Per inviare una risposta, creare e scrivere la risposta al file specificato nell'intestazione BITS-Response-DataFile-Name.</span><span class="sxs-lookup"><span data-stu-id="487fb-107">To send a reply, create and write your response to the file specified in the BITS-Response-DataFile-Name header.</span></span>

<span data-ttu-id="487fb-108">Le applicazioni server che inviano la stessa risposta a molti client devono usare per riferimento, quindi è presente una sola copia della risposta sul server.</span><span class="sxs-lookup"><span data-stu-id="487fb-108">Server applications that send the same reply to many clients should use by reference, so there is only one copy of the reply on the server.</span></span> <span data-ttu-id="487fb-109">Ad esempio, in un'applicazione di aggiornamento software, il client caricherà la configurazione software nell'applicazione server.</span><span class="sxs-lookup"><span data-stu-id="487fb-109">For example, in a software update application, the client would upload its software configuration to the server application.</span></span> <span data-ttu-id="487fb-110">L'applicazione server determina il pacchetto necessario per il client e invia l'URL del pacchetto a BITS.</span><span class="sxs-lookup"><span data-stu-id="487fb-110">The server application determines which package the client needs and sends the URL of the package to BITS.</span></span> <span data-ttu-id="487fb-111">BITS scarica quindi il pacchetto come risposta.</span><span class="sxs-lookup"><span data-stu-id="487fb-111">Then, BITS downloads the package as the reply.</span></span>

<span data-ttu-id="487fb-112">Le applicazioni server che generano risposte univoche per ogni client devono utilizzare per valore.</span><span class="sxs-lookup"><span data-stu-id="487fb-112">Server applications that generate unique replies for each client should use by value.</span></span> <span data-ttu-id="487fb-113">Ad esempio, un'applicazione server che supporta l'acquisto di file musicali deve inviare un file musicale firmato al client.</span><span class="sxs-lookup"><span data-stu-id="487fb-113">For example, a server application that supports the purchase of music files would need to send a signed music file to the client.</span></span> <span data-ttu-id="487fb-114">Poiché il file Music firmato è univoco per il client, l'applicazione server non lo archivia nel server.</span><span class="sxs-lookup"><span data-stu-id="487fb-114">Because the signed music file is unique to the client, the server application would not store it on the server.</span></span> <span data-ttu-id="487fb-115">Per valore è utile anche per un'applicazione che è già stata scritta per accettare direttamente i dati del client Web.</span><span class="sxs-lookup"><span data-stu-id="487fb-115">By value is also useful for an application that is already written to accept web client data directly.</span></span>

<span data-ttu-id="487fb-116">Per informazioni dettagliate sulle intestazioni di richiesta e risposta usate tra BITS e l'applicazione server, vedere [protocollo di notifica per le applicazioni server](notification-protocol-for-server-applications.md).</span><span class="sxs-lookup"><span data-stu-id="487fb-116">For details on the request and response headers used between BITS and your server application, see [Notification Protocol for Server Applications](notification-protocol-for-server-applications.md).</span></span>

<span data-ttu-id="487fb-117">Nell'esempio JavaScript seguente viene illustrato come accedere ai file di richiesta e risposta in un'applicazione server che utilizza la notifica di riferimento (BITS passa il percorso dei file nelle intestazioni).</span><span class="sxs-lookup"><span data-stu-id="487fb-117">The following JavaScript example shows how to access the request and response files in a server application that uses by reference notification (BITS passes the location of the files in the headers).</span></span>


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



<span data-ttu-id="487fb-118">Se si vuole usare un file di risposta diverso da quello specificato in BITS-Response-DataFile-Name, chiamare il metodo **Response. AddHeader** per aggiungere bits-static-Response-URL, come illustrato nell'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="487fb-118">If you want to use a different response file than the one specified in BITS-Response-DataFile-Name, call the **Response.AddHeader** method to add the BITS-Static-Response-URL as shown in the following example.</span></span> <span data-ttu-id="487fb-119">Se si specifica un file di risposta diverso, non creare il file di risposta specificato in BITS-Response-DataFile-Name.</span><span class="sxs-lookup"><span data-stu-id="487fb-119">If you specify a different response file, do not create the response file specified in BITS-Response-DataFile-Name.</span></span>


```JavaScript
  Response.AddHeader "BITS-Static-Response-URL" "https://myserver/mypath/myfile"
```
 

 




