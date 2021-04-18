---
title: Funzioni client di servizi di distribuzione Windows
description: Le funzioni seguenti vengono utilizzate con l'API client di servizi di distribuzione Windows.
ms.assetid: 4cedd8a8-7f46-4229-9d96-58965b751e43
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe124c6f02d12943d40fbc98af4a687d5b892f86
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298797"
---
# <a name="windows-deployment-services-client-functions"></a>Funzioni client di servizi di distribuzione Windows

Le funzioni seguenti vengono utilizzate con l'API client di servizi di distribuzione Windows.



| Funzione                                                                                 | Descrizione                                                                                                                            |
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| [*\_WDSCLICALLBACK PFN*](/windows/desktop/api/WdsClientAPI/nc-wdsclientapi-pfn_wdsclicallback)                                          | Messaggi di errore e di notifica sullo stato di avanzamento durante il trasferimento di file o immagini.                                                              |
| [*\_WDSCLITRACEFUNCTION PFN*](/windows/desktop/api/WdsClientAPI/nc-wdsclientapi-pfn_wdsclitracefunction)                                | Riceve i messaggi di debug dal client WDS.                                                                                       |
| [**WdsCliAuthorizeSession**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscliauthorizesession)                                 | Converte una sessione anonima in una sessione autenticata.                                                                           |
| [**WdsCliCancelTransfer**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdsclicanceltransfer)                                     | Annulla un'operazione di trasferimento WDS.                                                                                                      |
| [**WdsCliClose**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscliclose)                                                       | Chiude un handle a una sessione o un'immagine di WDS e rilascia le risorse.                                                                      |
| [**WdsCliCreateSession**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdsclicreatesession)                                       | Avvia una nuova sessione con un server WDS.                                                                                                |
| [**WdsCliFindFirstImage**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdsclifindfirstimage)                                     | Avvia l'enumerazione delle immagini archiviate in un server WDS e restituisce un handle di ricerca che fa riferimento alla prima immagine.                     |
| [**WdsCliFindNextImage**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdsclifindnextimage)                                       | Sposta in avanti il riferimento di un handle di ricerca alla successiva immagine archiviata in un server WDS.                                                      |
| [**WdsCliFreeStringArray**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdsclifreestringarray)                                   | Libera la matrice di valori stringa che viene allocata dalla funzione [**WdsCliObtainDriverPackages**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscliobtaindriverpackages) . |
| [**WdsCliGetEnumerationFlags**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscligetenumerationflags)                           | Restituisce il flag di enumerazione dell'immagine per l'handle dell'immagine corrente.                                                                       |
| [**WdsCliGetImageArchitecture**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagearchitecture)                         | Restituisce l'architettura del processore per l'immagine corrente.                                                                              |
| [**WdsCliGetImageDescription**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagedescription)                           | Restituisce la descrizione dell'immagine corrente.                                                                                          |
| [**WdsCliGetImageGroup**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagegroup)                                       | Restituisce il nome del gruppo di immagini per l'immagine corrente.                                                                                    |
| [**WdsCliGetImageHalName**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagehalname)                                   | Restituisce il nome HAL (Hardware Abstraction Layer) per l'immagine corrente.                                                               |
| [**WdsCliGetImageHandleFromFindHandle**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagehandlefromfindhandle)         | Restituisce un handle di immagine per l'immagine corrente.                                                                                         |
| [**WdsCliGetImageHandleFromTransferHandle**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagehandlefromtransferhandle) | Restituisce un handle di immagine da un handle di trasferimento completato.                                                                              |
| [**WdsCliGetImageIndex**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscligetimageindex)                                       | Restituisce l'indice dell'immagine per l'immagine corrente.                                                                                         |
| [**WdsCliGetImageLanguage**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagelanguage)                                 | Restituisce la lingua predefinita dell'immagine corrente.                                                                                     |
| [**WdsCliGetImageLanguages**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagelanguages)                               | Restituisce una matrice di linguaggi supportati dall'immagine corrente.                                                                          |
| [**WdsCliGetImageLastModifiedTime**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagelastmodifiedtime)                 | Restituisce l'ora dell'Ultima modifica per l'immagine corrente.                                                                                  |
| [**WdsCliGetImageName**](/windows/desktop/api/WdsClientApi/nf-wdsclientapi-wdscligetimagename)                                         | Restituisce il nome dell'immagine corrente.                                                                                                 |
| [**WdsCliGetImageNamespace**](/windows/desktop/api/WdsClientApi/nf-wdsclientapi-wdscligetimagenamespace)                               | Restituisce il nome dell'immagine corrente.                                                                                                 |
| [**WdsCliGetImagePath**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagepath)                                         | Restituisce il percorso del file di immagine che contiene l'immagine corrente.                                                                    |
| [**WdsCliGetImageSize**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagesize)                                         | Restituisce le dimensioni dell'immagine corrente.                                                                                                 |
| [**WdsCliGetImageVersion**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscligetimageversion)                                   | Restituisce la versione dell'immagine corrente.                                                                                              |
| [**WdsCliGetTransferSize**](/windows/desktop/api/WdsClientApi/nf-wdsclientapi-wdscligettransfersize)                                   | Restituisce la dimensione del trasferimento corrente.                                                                                              |
| [**WdsCliInitializeLog**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscliinitializelog)                                       | Inizializza il log per il client.                                                                                                    |
| [**WdsCliLog**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdsclilog)                                                           | Invia un evento log al server WDS.                                                                                                   |
| [**WdsCliObtainDriverPackages**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscliobtaindriverpackages)                         | Ottiene da un'immagine di WDS, i pacchetti driver (file INF) che possono essere usati in questo computer.                                           |
| [**WdsCliRegisterTrace**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscliregistertrace)                                       | Registra una funzione di callback che riceverà i messaggi di debug.                                                                    |
| [**WdsCliTransferFile**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdsclitransferfile)                                         | Trasferisce un file da un server WDS al client WDS utilizzando un protocollo di trasferimento multicast.                                              |
| [**WdsCliTransferImage**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdsclitransferimage)                                       | Trasferisce un'immagine da un server WDS.                                                                                                  |
| [**WdsCliWaitForTransfer**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscliwaitfortransfer)                                   | Attende il completamento di un trasferimento.                                                                                                      |



 



| Funzione                                                             | Descrizione                                                                                                                                                    |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WdsCliGetDriverQueryXml**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscligetdriverqueryxml)           | Genera una stringa XML che può essere utilizzata per eseguire una query su un server WDS per i pacchetti driver. Disponibile a partire da Windows 8 e Windows Server 2012.               |
| [**WdsCliObtainDriverPackagesEx**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscliobtaindriverpackagesex) | Ottiene i pacchetti driver (file INF) applicabili al codice XML di query del driver WDS specificato. Disponibile a partire da Windows 8 e Windows Server 2012. |



 

 

 




