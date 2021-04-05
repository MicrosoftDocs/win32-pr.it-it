---
title: Protocollo di notifica per le applicazioni server
description: BITS usa la proprietà BITSServerNotificationType per determinare il modo in cui BITS invia il contenuto del file di caricamento all'applicazione server.
ms.assetid: d5193d0c-3ab4-47ab-a570-fea2904a4371
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0d35f6f5fec1a1de9ebd5c2c244a55bc1806b06
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955213"
---
# <a name="notification-protocol-for-server-applications"></a><span data-ttu-id="c190f-103">Protocollo di notifica per le applicazioni server</span><span class="sxs-lookup"><span data-stu-id="c190f-103">Notification Protocol for Server Applications</span></span>

<span data-ttu-id="c190f-104">BITS usa la proprietà [BITSServerNotificationType](bits-iis-extension-properties.md) per determinare il modo in cui bits invia il contenuto del file di caricamento all'applicazione server.</span><span class="sxs-lookup"><span data-stu-id="c190f-104">BITS uses the [BITSServerNotificationType](bits-iis-extension-properties.md) property to determine how BITS sends the contents of the upload file to the server application.</span></span> <span data-ttu-id="c190f-105">Se la proprietà BITSServerNotificationType è impostata su 1, [bits passa il percorso del file di caricamento in un'intestazione](#sending-the-location-of-the-upload-file-in-a-header).</span><span class="sxs-lookup"><span data-stu-id="c190f-105">If the BITSServerNotificationType property is set to 1, [BITS passes the location of the upload file in a header](#sending-the-location-of-the-upload-file-in-a-header).</span></span> <span data-ttu-id="c190f-106">Se la proprietà BITSServerNotificationType è impostata su 2, [bits passa il contenuto del file di caricamento nel corpo della richiesta](#sending-the-upload-file-in-the-body-of-the-request).</span><span class="sxs-lookup"><span data-stu-id="c190f-106">If the BITSServerNotificationType property is set to 2, [BITS passes the contents of the upload file in the body of the request](#sending-the-upload-file-in-the-body-of-the-request).</span></span>

<span data-ttu-id="c190f-107">Per informazioni dettagliate sul modo in cui BITS gestisce gli errori dall'applicazione server, vedere [gestione degli errori dell'applicazione server](#handling-server-application-errors).</span><span class="sxs-lookup"><span data-stu-id="c190f-107">For details on how BITS handles errors from the server application, see [Handling server application errors](#handling-server-application-errors).</span></span>

## <a name="sending-the-location-of-the-upload-file-in-a-header"></a><span data-ttu-id="c190f-108">Invio del percorso del file di caricamento in un'intestazione</span><span class="sxs-lookup"><span data-stu-id="c190f-108">Sending the location of the upload file in a header</span></span>

<span data-ttu-id="c190f-109">BITS passa il percorso dei file di caricamento e di risposta all'applicazione server nelle intestazioni se la proprietà [BITSServerNotificationType](bits-iis-extension-properties.md) è impostata su 1.</span><span class="sxs-lookup"><span data-stu-id="c190f-109">BITS passes the location of the upload and reply files to the server application in the headers if the [BITSServerNotificationType](bits-iis-extension-properties.md) property is set to 1.</span></span> <span data-ttu-id="c190f-110">L'applicazione server apre il file di caricamento, elabora i dati e quindi genera il file di risposta.</span><span class="sxs-lookup"><span data-stu-id="c190f-110">The server application opens the upload file, processes the data, and then generates the reply file.</span></span> <span data-ttu-id="c190f-111">Per impostazione predefinita, BITS rimuove i file di caricamento e di risposta dal server dopo aver ricevuto la risposta dall'applicazione server.</span><span class="sxs-lookup"><span data-stu-id="c190f-111">By default, BITS removes the upload and reply files from the server after it receives the response from the server application.</span></span> <span data-ttu-id="c190f-112">Per fare in modo che BITS copi il file di caricamento nel percorso specificato dal nome del file remoto nel processo, includere l'intestazione BITS-copy-file-to-Destination nella risposta.</span><span class="sxs-lookup"><span data-stu-id="c190f-112">To have BITS copy the upload file to the location specified by the remote file name in the job, include the BITS-Copy-File-To-Destination header in your response.</span></span> <span data-ttu-id="c190f-113">Se non si include l'intestazione e si desidera salvare i file di caricamento e di risposta, è necessario copiare i file di caricamento e di risposta in un nuovo percorso prima di rispondere.</span><span class="sxs-lookup"><span data-stu-id="c190f-113">If you do not include the header and you want to save the upload and reply files, you must copy the upload and reply files to a new location before responding.</span></span> <span data-ttu-id="c190f-114">Nella tabella seguente vengono illustrate le intestazioni della richiesta.</span><span class="sxs-lookup"><span data-stu-id="c190f-114">The following table shows the request headers.</span></span>



| <span data-ttu-id="c190f-115">Intestazione della richiesta</span><span class="sxs-lookup"><span data-stu-id="c190f-115">Request header</span></span>              | <span data-ttu-id="c190f-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c190f-116">Description</span></span>                                                                                |
|-----------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="c190f-117">BITS-originale-request-URL</span><span class="sxs-lookup"><span data-stu-id="c190f-117">BITS-Original-Request-URL</span></span>   | <span data-ttu-id="c190f-118">Contiene il nome remoto specificato nel processo.</span><span class="sxs-lookup"><span data-stu-id="c190f-118">Contains the remote name specified in the job.</span></span>                                             |
| <span data-ttu-id="c190f-119">BITS-request-DataFile-Name</span><span class="sxs-lookup"><span data-stu-id="c190f-119">BITS-Request-DataFile-Name</span></span>  | <span data-ttu-id="c190f-120">Contiene il percorso completo dei dati caricati.</span><span class="sxs-lookup"><span data-stu-id="c190f-120">Contains the full path to the uploaded data.</span></span>                                               |
| <span data-ttu-id="c190f-121">BITS-Response-DataFile-Name</span><span class="sxs-lookup"><span data-stu-id="c190f-121">BITS-Response-DataFile-Name</span></span> | <span data-ttu-id="c190f-122">Contiene il percorso completo in cui BITS prevede che l'applicazione server scriva la risposta.</span><span class="sxs-lookup"><span data-stu-id="c190f-122">Contains the full path to where BITS expects the server application to write the response.</span></span> |



 

<span data-ttu-id="c190f-123">Nella tabella seguente vengono illustrate le intestazioni della risposta.</span><span class="sxs-lookup"><span data-stu-id="c190f-123">The following table shows the response headers.</span></span>



| <span data-ttu-id="c190f-124">Intestazione risposta</span><span class="sxs-lookup"><span data-stu-id="c190f-124">Response header</span></span>               | <span data-ttu-id="c190f-125">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c190f-125">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|-------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c190f-126">BITS-static-Response-URL</span><span class="sxs-lookup"><span data-stu-id="c190f-126">BITS-Static-Response-URL</span></span>      | <span data-ttu-id="c190f-127">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="c190f-127">Optional.</span></span> <span data-ttu-id="c190f-128">Contiene l'URL assoluto (non specificare un URL relativo) a un file di dati statici da utilizzare come risposta.</span><span class="sxs-lookup"><span data-stu-id="c190f-128">Contains the absolute URL (do not specify a relative URL) to a static data file to use as the response.</span></span> <span data-ttu-id="c190f-129">Il file di dati statici deve essere accessibile dal client BITS.</span><span class="sxs-lookup"><span data-stu-id="c190f-129">The static data file must be accessible by the BITS client.</span></span> <span data-ttu-id="c190f-130">Se si usa questa intestazione, non creare il file di risposta specificato nell'intestazione della richiesta BITS-Response-DataFile-Name.</span><span class="sxs-lookup"><span data-stu-id="c190f-130">If you use this header, do not create the response file specified in the BITS-Response-DataFile-Name request header.</span></span> <span data-ttu-id="c190f-131">Si noti che BITS non elimina il file per l'utente.</span><span class="sxs-lookup"><span data-stu-id="c190f-131">Note that BITS does not delete this file for you.</span></span><br/>                                                                                                           |
| <span data-ttu-id="c190f-132">BITS-copy-file-to-Destination</span><span class="sxs-lookup"><span data-stu-id="c190f-132">BITS-Copy-File-To-Destination</span></span> | <span data-ttu-id="c190f-133">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="c190f-133">Optional.</span></span> <span data-ttu-id="c190f-134">Per impostazione predefinita, se la proprietà [BITSServerNotificationType](bits-iis-extension-properties.md) è impostata su 1 o 2, il server BITS non copia il file di caricamento nel percorso specificato dal nome file remoto nel processo.</span><span class="sxs-lookup"><span data-stu-id="c190f-134">By default, if the [BITSServerNotificationType](bits-iis-extension-properties.md) property is set to 1 or 2, the BITS server does not copy the upload file to the location specified by the remote file name in the job.</span></span> <span data-ttu-id="c190f-135">Per fare in modo che BITS copi il file nel percorso specificato dal nome del file remoto nel processo, inviare questa intestazione di risposta.</span><span class="sxs-lookup"><span data-stu-id="c190f-135">To have BITS copy the file to the location specified by the remote file name in the job, send this response header.</span></span> <span data-ttu-id="c190f-136">È possibile specificare qualsiasi valore. BITS non utilizza il valore.</span><span class="sxs-lookup"><span data-stu-id="c190f-136">You can specify any value; BITS does not use the value.</span></span> <span data-ttu-id="c190f-137">Si noti che è necessario che le cartelle nel percorso del file remoto esistano.</span><span class="sxs-lookup"><span data-stu-id="c190f-137">Note that the folders in the remote file path must exist.</span></span> |



 

<span data-ttu-id="c190f-138">La richiesta seguente mostra i bit che inviano il percorso del file di caricamento all'applicazione server.</span><span class="sxs-lookup"><span data-stu-id="c190f-138">The following request shows BITS sending the location of the upload file to the server application.</span></span>

``` syntax
POST https://myserver/myvdir/handle_upload.asp?ACCOUNT=873112 HTTP/1.1
Host: myserver
BITS-Original-Request-URL: https://front-end-server/vdir
BITS-Request-DataFile-Name: c:\physical-path\BITS-Sessions\{5e53c221-f2d6-4bf2-
b994-1dc43ceaca8d}\request
BITS-Response-DataFile-Name: c:\physical-path\BITS-Sessions\{5e53c221-f2d6-4bf2-
b994-1dc43ceaca8d}\response
Content-Length: 0
```

<span data-ttu-id="c190f-139">Di seguito viene illustrata la risposta dell'applicazione server a BITS; la risposta viene inserita nel file specificato dall'intestazione della richiesta BITS-Response-DataFile-Name.</span><span class="sxs-lookup"><span data-stu-id="c190f-139">The following shows the server application's reply to BITS; the reply is placed in the file specified by the BITS-Response-DataFile-Name request header.</span></span>

``` syntax
HTTP/1.1 200 - OK
Content-Length: 0
```

## <a name="sending-the-upload-file-in-the-body-of-the-request"></a><span data-ttu-id="c190f-140">Invio del file di caricamento nel corpo della richiesta</span><span class="sxs-lookup"><span data-stu-id="c190f-140">Sending the upload file in the body of the request</span></span>

<span data-ttu-id="c190f-141">BITS invia il file di caricamento nel corpo della richiesta se la proprietà [BITSServerNotificationType](bits-iis-extension-properties.md) è impostata su 2.</span><span class="sxs-lookup"><span data-stu-id="c190f-141">BITS sends the upload file in the body of the request if the [BITSServerNotificationType](bits-iis-extension-properties.md) property is set to 2.</span></span> <span data-ttu-id="c190f-142">Inviando il file di caricamento nel corpo della richiesta, gli script e le applicazioni esistenti funzionano con modifiche minime.</span><span class="sxs-lookup"><span data-stu-id="c190f-142">Sending the upload file in the body of the request lets existing scripts and applications work with minimal modifications.</span></span> <span data-ttu-id="c190f-143">Il file di caricamento e il file di risposta vengono passati rispettivamente nella richiesta e nella risposta.</span><span class="sxs-lookup"><span data-stu-id="c190f-143">The upload file and reply file are passed in the request and response, respectively.</span></span> <span data-ttu-id="c190f-144">Nella tabella seguente viene illustrata l'intestazione della richiesta.</span><span class="sxs-lookup"><span data-stu-id="c190f-144">The following table shows the request header.</span></span>



| <span data-ttu-id="c190f-145">Intestazione della richiesta</span><span class="sxs-lookup"><span data-stu-id="c190f-145">Request header</span></span>            | <span data-ttu-id="c190f-146">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c190f-146">Description</span></span>                                    |
|---------------------------|------------------------------------------------|
| <span data-ttu-id="c190f-147">BITS-originale-request-URL</span><span class="sxs-lookup"><span data-stu-id="c190f-147">BITS-Original-Request-URL</span></span> | <span data-ttu-id="c190f-148">Contiene il nome remoto specificato nel processo.</span><span class="sxs-lookup"><span data-stu-id="c190f-148">Contains the remote name specified in the job.</span></span> |



 

<span data-ttu-id="c190f-149">Nella tabella seguente vengono illustrate le intestazioni della risposta.</span><span class="sxs-lookup"><span data-stu-id="c190f-149">The following table shows the response headers.</span></span>



| <span data-ttu-id="c190f-150">Intestazione risposta</span><span class="sxs-lookup"><span data-stu-id="c190f-150">Response header</span></span>               | <span data-ttu-id="c190f-151">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c190f-151">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c190f-152">BITS-static-Response-URL</span><span class="sxs-lookup"><span data-stu-id="c190f-152">BITS-Static-Response-URL</span></span>      | <span data-ttu-id="c190f-153">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="c190f-153">Optional.</span></span> <span data-ttu-id="c190f-154">Contiene l'URL assoluto (non specificare un URL relativo) a un file di dati statici da utilizzare come risposta.</span><span class="sxs-lookup"><span data-stu-id="c190f-154">Contains the absolute URL (do not specify a relative URL) to a static data file to use as the response.</span></span> <span data-ttu-id="c190f-155">Il file di dati statici deve essere accessibile dal client BITS.</span><span class="sxs-lookup"><span data-stu-id="c190f-155">The static data file must be accessible by the BITS client.</span></span> <span data-ttu-id="c190f-156">Se si usa questa intestazione, non includere la risposta nel flusso.</span><span class="sxs-lookup"><span data-stu-id="c190f-156">If you use this header, do not include the response in the stream.</span></span> <span data-ttu-id="c190f-157">Si noti che BITS non elimina il file per l'utente.</span><span class="sxs-lookup"><span data-stu-id="c190f-157">Note that BITS does not delete this file for you.</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="c190f-158">BITS-copy-file-to-Destination</span><span class="sxs-lookup"><span data-stu-id="c190f-158">BITS-Copy-File-To-Destination</span></span> | <span data-ttu-id="c190f-159">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="c190f-159">Optional.</span></span> <span data-ttu-id="c190f-160">Se la proprietà [BITSServerNotificationType](bits-iis-extension-properties.md) è impostata su 1 o 2, il server BITS non copia il file di caricamento nel percorso specificato dal nome del file remoto nel processo.</span><span class="sxs-lookup"><span data-stu-id="c190f-160">If the [BITSServerNotificationType](bits-iis-extension-properties.md) property is set to 1 or 2, the BITS server does not copy the upload file to the location specified by the remote file name in the job.</span></span> <span data-ttu-id="c190f-161">Per fare in modo che BITS copi il file nel percorso specificato dal nome del file remoto, inviare questa intestazione di risposta.</span><span class="sxs-lookup"><span data-stu-id="c190f-161">To have BITS copy the file to the location specified by the remote file name, send this response header.</span></span> <span data-ttu-id="c190f-162">È possibile specificare qualsiasi valore. BITS non utilizza il valore.</span><span class="sxs-lookup"><span data-stu-id="c190f-162">You can specify any value; BITS does not use the value.</span></span> <span data-ttu-id="c190f-163">Si noti che è necessario che le cartelle nel percorso del file remoto esistano.</span><span class="sxs-lookup"><span data-stu-id="c190f-163">Note that the folders in the remote file path must exist.</span></span> |



 

<span data-ttu-id="c190f-164">La richiesta seguente mostra i bit che passano il file caricato all'applicazione server nel corpo della richiesta.</span><span class="sxs-lookup"><span data-stu-id="c190f-164">The following request shows BITS passing the uploaded file to the server application in the body of the request.</span></span>

``` syntax
POST https://myserver/myvdir/handle_upload.asp?ACCOUNT=873112 HTTP/1.1
Host: myserver
BITS-Original-Request-URL: https://front-end-server/vdir
Content-Length: 80000

80000 bytes of upload data goes here
```

<span data-ttu-id="c190f-165">La risposta seguente mostra l'applicazione server che passa i dati di risposta a BITS nel corpo della risposta.</span><span class="sxs-lookup"><span data-stu-id="c190f-165">The following reply shows the server application passing the reply data to BITS in the body of the response.</span></span>

``` syntax
HTTP/1.1 200 - OK
Content-Length: 100

100 bytes of reply data goes here
```

## <a name="handling-server-application-errors"></a><span data-ttu-id="c190f-166">Gestione degli errori dell'applicazione server</span><span class="sxs-lookup"><span data-stu-id="c190f-166">Handling server application errors</span></span>

<span data-ttu-id="c190f-167">Vedere [gestione degli errori dell'applicazione server](handling-server-application-errors.md).</span><span class="sxs-lookup"><span data-stu-id="c190f-167">See [Handling Server Application Errors](handling-server-application-errors.md).</span></span>

 

 





