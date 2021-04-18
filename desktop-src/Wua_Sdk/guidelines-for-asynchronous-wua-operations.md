---
description: In questo argomento vengono identificate le linee guida da seguire quando si eseguono operazioni asincrone di Windows Update Agent (WUA).
ms.assetid: 1fb16904-732d-4341-8267-ab8896fc0f7c
title: Linee guida per le operazioni WUA asincrone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1a4b2198a235d9a03e3730e5d6dce2cd54c0e1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309731"
---
# <a name="guidelines-for-asynchronous-wua-operations"></a>Linee guida per le operazioni WUA asincrone

In questo argomento vengono identificate le linee guida da seguire quando si eseguono operazioni asincrone di Windows Update Agent (WUA).

-   Le operazioni WUA asincrone non garantiscono una particolare velocità di completamento. Il tempo di completamento per un'operazione WUA asincrona può variare notevolmente a seconda dell'hardware del computer, della versione del sistema operativo e della configurazione di rete. Come per le altre API Windows con dipendenze di rete e che non contengono un parametro di timeout o una durata documentata di timeout, è consigliabile implementare i propri meccanismi di timeout se sono necessari tempi di risposta garantiti. Ad esempio, è possibile creare un thread di lavoro che chiama un metodo WUA asincrono e che imposta un evento o un altro oggetto di sincronizzazione al completamento dell'operazione WUA asincrona; il thread principale può quindi usare la funzione [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) o [**WaitForMultipleObjects**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjects) , che consente di specificare un valore di timeout.
-   Quando si termina una ricerca, il download, l'installazione o la disinstallazione degli aggiornamenti, è possibile usare [**IUpdateSearcher:: EndSearch**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-endsearch), [**IUpdateDowloader:: Metodo**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatedownloader), [**IUpdateInstaller:: EndInstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-endinstall) e [**IUpdateInstaller:: EndUninstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-enduninstall) da qualsiasi thread.
-   Quando si avvia una ricerca, il download, l'installazione o la disinstallazione degli aggiornamenti tramite [**IUpdateSearcher:: BeginSearch**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-beginsearch), [**IUpdateDownloader:: BeginDownload**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-begindownload), [**IUpdateInstaller:: BeginInstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-begininstall)e [**IUpdateInstaller:: BeginUninstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-beginuninstall), assicurarsi di mantenere un accesso sufficiente le autorizzazioni quando si rilasciano i riferimenti agli oggetti API WUA.
    -   Assicurarsi che per tutti gli oggetti di callback utilizzati nell'operazione asincrona non venga fatto riferimento prima di eliminarli. Attendere che il conteggio dei riferimenti di un oggetto callback torni al valore iniziale prima di eliminarlo.
    -   Il riferimento all'oggetto processo restituito dal metodo **Begin** corrispondente deve essere controllato da un oggetto che differisce dagli oggetti di callback. Usare un oggetto diverso dagli oggetti di callback per evitare riferimenti circolari.
    -   Se si tenta di controllare il riferimento all'oggetto processo usando un oggetto callback, è necessario chiamare il metodo [**IDownloadJob:: Cleanup**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadjob-cleanup), [**IInstallationJob:: Cleanup**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationjob-cleanup)o [**ISearchJob:: Cleanup**](/windows/desktop/api/Wuapi/nf-wuapi-isearchjob-cleanup) al di fuori della funzione di callback per disconnettere l'oggetto processo dall'oggetto callback. È necessario eseguire questa operazione prima di rilasciare il riferimento all'oggetto processo restituito dal metodo **Begin** .
-   Assicurarsi che le operazioni WUA asincrone siano completate. Windows script host può terminare uno script quando tutti i comandi all'esterno di qualsiasi funzione sono completati, anche se l'API WUA contiene ancora riferimenti all'oggetto callback.
    -   Usare uno dei metodi di **pulitura** o fare in modo che la funzione di callback imposti una variabile globale condivisa al termine dell'esecuzione.
    -   Non chiamare mai [**IDownloadJob:: Cleanup**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadjob-cleanup), [**IInstallationJob:: Cleanup**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationjob-cleanup)o [**ISearchJob:: Cleanup**](/windows/desktop/api/Wuapi/nf-wuapi-isearchjob-cleanup) su un oggetto processo nella relativa funzione di callback.
    -   Per garantire la corretta sequenza di pulizia in uno script in esecuzione in Windows Internet Explorer, chiamare il metodo **Cleanup** su tutti gli oggetti processo durante l'elaborazione di Window. onbeforeunload.
-   Non usare tipi di dati definiti dall'utente (UDT) per le operazioni WUA asincrone. Il tipo non è supportato da [**IUpdateSearcher:: BeginSearch**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-beginsearch), [**IUpdateDownloader:: BeginDownload**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-begindownload), [**IUpdateInstaller:: BeginInstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-begininstall)o [**IUpdateInstaller:: BeginUninstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-beginuninstall).

 

 
