---
description: L'interfaccia IDownloadProgress definisce le proprietà seguenti.
ms.assetid: 8f64c702-b2b5-4a5f-9365-bc962e35f499
title: Proprietà IDownloadProgress
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eeed70acfb6b350c463b731d44cfe0d48cc1fd8a5190c247fcda316c4707126f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119130573"
---
# <a name="idownloadprogress-properties"></a>Proprietà IDownloadProgress

[**L'interfaccia IDownloadProgress**](/windows/desktop/api/Wuapi/nn-wuapi-idownloadprogress) definisce le proprietà seguenti.



| Proprietà                                                                               | Descrizione                                                                                                                                      |
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CurrentUpdateBytesDownloaded**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_currentupdatebytesdownloaded) | Ottiene una stringa che specifica la quantità di dati trasferiti per il file di contenuto o i file dell'aggiornamento da scaricare, in byte.  |
| [**CurrentUpdateBytesToDownload**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_currentupdatebytestodownload) | Ottiene una stringa che stima la quantità di dati da trasferire per il file di contenuto o i file dell'aggiornamento scaricato, in byte. |
| [**CurrentUpdateDownloadPhase**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_currentupdatedownloadphase)     | Ottiene un [**valore di enumerazione DownloadPhase**](/windows/win32/api/wuapi/ne-wuapi-downloadphase) che specifica la fase del download attualmente in corso.          |
| [**CurrentUpdateIndex**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_currentupdateindex)                     | Ottiene un valore di indice in base zero che specifica l'aggiornamento attualmente scaricato quando sono stati selezionati più aggiornamenti.             |
| [**CurrentUpdatePercentComplete**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_currentupdatepercentcomplete) | Ottiene una stima della percentuale dell'aggiornamento corrente scaricato.                                                               |
| [**PercentComplete**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_percentcomplete)                           | Ottiene una stima della percentuale di tutti gli aggiornamenti scaricati.                                                                 |
| [**TotalBytesDownloaded**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_totalbytesdownloaded)                 | Ottiene una stringa che specifica la quantità totale di dati scaricati, in byte.                                                        |
| [**TotalBytesToDownload**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_totalbytestodownload)                 | Ottiene una stringa che rappresenta la stima della quantità totale di dati che verranno scaricati, in byte.                                        |



 

 

 



