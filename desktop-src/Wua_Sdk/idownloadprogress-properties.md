---
description: L'interfaccia IDownloadProgress definisce le proprietà seguenti.
ms.assetid: 8f64c702-b2b5-4a5f-9365-bc962e35f499
title: Proprietà di IDownloadProgress
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 469246acb59b4aa58efcbf4bb5aa7f04b7e44b6a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966740"
---
# <a name="idownloadprogress-properties"></a>Proprietà di IDownloadProgress

L'interfaccia [**IDownloadProgress**](/windows/desktop/api/Wuapi/nn-wuapi-idownloadprogress) definisce le proprietà seguenti.



| Proprietà                                                                               | Descrizione                                                                                                                                      |
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CurrentUpdateBytesDownloaded**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_currentupdatebytesdownloaded) | Ottiene una stringa che specifica la quantità di dati trasferiti per il file o i file di contenuto dell'aggiornamento in fase di download, in byte.  |
| [**CurrentUpdateBytesToDownload**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_currentupdatebytestodownload) | Ottiene una stringa che stima la quantità di dati che devono essere trasferiti per il file o i file di contenuto dell'aggiornamento in fase di download, in byte. |
| [**CurrentUpdateDownloadPhase**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_currentupdatedownloadphase)     | Ottiene un valore di enumerazione [**DownloadPhase**](/windows/win32/api/wuapi/ne-wuapi-downloadphase) che specifica la fase del download attualmente in corso.          |
| [**CurrentUpdateIndex**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_currentupdateindex)                     | Ottiene un valore di indice in base zero che specifica l'aggiornamento attualmente in fase di download quando sono stati selezionati più aggiornamenti.             |
| [**CurrentUpdatePercentComplete**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_currentupdatepercentcomplete) | Ottiene una stima della percentuale dell'aggiornamento corrente che è stato scaricato.                                                               |
| [**PercentComplete**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_percentcomplete)                           | Ottiene una stima della percentuale di tutti gli aggiornamenti che sono stati scaricati.                                                                 |
| [**TotalBytesDownloaded**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_totalbytesdownloaded)                 | Ottiene una stringa che specifica la quantità totale di dati scaricati, in byte.                                                        |
| [**TotalBytesToDownload**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_totalbytestodownload)                 | Ottiene una stringa che rappresenta la stima della quantità totale di dati che verrà scaricata in byte.                                        |



 

 

 



