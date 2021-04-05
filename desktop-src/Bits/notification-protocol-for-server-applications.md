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
# <a name="notification-protocol-for-server-applications"></a>Protocollo di notifica per le applicazioni server

BITS usa la proprietà [BITSServerNotificationType](bits-iis-extension-properties.md) per determinare il modo in cui bits invia il contenuto del file di caricamento all'applicazione server. Se la proprietà BITSServerNotificationType è impostata su 1, [bits passa il percorso del file di caricamento in un'intestazione](#sending-the-location-of-the-upload-file-in-a-header). Se la proprietà BITSServerNotificationType è impostata su 2, [bits passa il contenuto del file di caricamento nel corpo della richiesta](#sending-the-upload-file-in-the-body-of-the-request).

Per informazioni dettagliate sul modo in cui BITS gestisce gli errori dall'applicazione server, vedere [gestione degli errori dell'applicazione server](#handling-server-application-errors).

## <a name="sending-the-location-of-the-upload-file-in-a-header"></a>Invio del percorso del file di caricamento in un'intestazione

BITS passa il percorso dei file di caricamento e di risposta all'applicazione server nelle intestazioni se la proprietà [BITSServerNotificationType](bits-iis-extension-properties.md) è impostata su 1. L'applicazione server apre il file di caricamento, elabora i dati e quindi genera il file di risposta. Per impostazione predefinita, BITS rimuove i file di caricamento e di risposta dal server dopo aver ricevuto la risposta dall'applicazione server. Per fare in modo che BITS copi il file di caricamento nel percorso specificato dal nome del file remoto nel processo, includere l'intestazione BITS-copy-file-to-Destination nella risposta. Se non si include l'intestazione e si desidera salvare i file di caricamento e di risposta, è necessario copiare i file di caricamento e di risposta in un nuovo percorso prima di rispondere. Nella tabella seguente vengono illustrate le intestazioni della richiesta.



| Intestazione della richiesta              | Descrizione                                                                                |
|-----------------------------|--------------------------------------------------------------------------------------------|
| BITS-originale-request-URL   | Contiene il nome remoto specificato nel processo.                                             |
| BITS-request-DataFile-Name  | Contiene il percorso completo dei dati caricati.                                               |
| BITS-Response-DataFile-Name | Contiene il percorso completo in cui BITS prevede che l'applicazione server scriva la risposta. |



 

Nella tabella seguente vengono illustrate le intestazioni della risposta.



| Intestazione risposta               | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|-------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BITS-static-Response-URL      | facoltativo. Contiene l'URL assoluto (non specificare un URL relativo) a un file di dati statici da utilizzare come risposta. Il file di dati statici deve essere accessibile dal client BITS. Se si usa questa intestazione, non creare il file di risposta specificato nell'intestazione della richiesta BITS-Response-DataFile-Name. Si noti che BITS non elimina il file per l'utente.<br/>                                                                                                           |
| BITS-copy-file-to-Destination | facoltativo. Per impostazione predefinita, se la proprietà [BITSServerNotificationType](bits-iis-extension-properties.md) è impostata su 1 o 2, il server BITS non copia il file di caricamento nel percorso specificato dal nome file remoto nel processo. Per fare in modo che BITS copi il file nel percorso specificato dal nome del file remoto nel processo, inviare questa intestazione di risposta. È possibile specificare qualsiasi valore. BITS non utilizza il valore. Si noti che è necessario che le cartelle nel percorso del file remoto esistano. |



 

La richiesta seguente mostra i bit che inviano il percorso del file di caricamento all'applicazione server.

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

Di seguito viene illustrata la risposta dell'applicazione server a BITS; la risposta viene inserita nel file specificato dall'intestazione della richiesta BITS-Response-DataFile-Name.

``` syntax
HTTP/1.1 200 - OK
Content-Length: 0
```

## <a name="sending-the-upload-file-in-the-body-of-the-request"></a>Invio del file di caricamento nel corpo della richiesta

BITS invia il file di caricamento nel corpo della richiesta se la proprietà [BITSServerNotificationType](bits-iis-extension-properties.md) è impostata su 2. Inviando il file di caricamento nel corpo della richiesta, gli script e le applicazioni esistenti funzionano con modifiche minime. Il file di caricamento e il file di risposta vengono passati rispettivamente nella richiesta e nella risposta. Nella tabella seguente viene illustrata l'intestazione della richiesta.



| Intestazione della richiesta            | Descrizione                                    |
|---------------------------|------------------------------------------------|
| BITS-originale-request-URL | Contiene il nome remoto specificato nel processo. |



 

Nella tabella seguente vengono illustrate le intestazioni della risposta.



| Intestazione risposta               | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BITS-static-Response-URL      | facoltativo. Contiene l'URL assoluto (non specificare un URL relativo) a un file di dati statici da utilizzare come risposta. Il file di dati statici deve essere accessibile dal client BITS. Se si usa questa intestazione, non includere la risposta nel flusso. Si noti che BITS non elimina il file per l'utente.<br/>                                                                                                                                      |
| BITS-copy-file-to-Destination | facoltativo. Se la proprietà [BITSServerNotificationType](bits-iis-extension-properties.md) è impostata su 1 o 2, il server BITS non copia il file di caricamento nel percorso specificato dal nome del file remoto nel processo. Per fare in modo che BITS copi il file nel percorso specificato dal nome del file remoto, inviare questa intestazione di risposta. È possibile specificare qualsiasi valore. BITS non utilizza il valore. Si noti che è necessario che le cartelle nel percorso del file remoto esistano. |



 

La richiesta seguente mostra i bit che passano il file caricato all'applicazione server nel corpo della richiesta.

``` syntax
POST https://myserver/myvdir/handle_upload.asp?ACCOUNT=873112 HTTP/1.1
Host: myserver
BITS-Original-Request-URL: https://front-end-server/vdir
Content-Length: 80000

80000 bytes of upload data goes here
```

La risposta seguente mostra l'applicazione server che passa i dati di risposta a BITS nel corpo della risposta.

``` syntax
HTTP/1.1 200 - OK
Content-Length: 100

100 bytes of reply data goes here
```

## <a name="handling-server-application-errors"></a>Gestione degli errori dell'applicazione server

Vedere [gestione degli errori dell'applicazione server](handling-server-application-errors.md).

 

 





