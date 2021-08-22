---
description: Questo argomento identifica le linee guida da seguire quando si eseguono operazioni asincrone Windows update agent (WUA).
ms.assetid: 1fb16904-732d-4341-8267-ab8896fc0f7c
title: Linee guida per le operazioni wua asincrone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24801c7639e75f34f1517ee626ff7acb7c1d13f85a6ebf57e7d824f7f0d3191d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119049489"
---
# <a name="guidelines-for-asynchronous-wua-operations"></a>Linee guida per le operazioni wua asincrone

Questo argomento identifica le linee guida da seguire quando si eseguono operazioni asincrone Windows update agent (WUA).

-   Le operazioni WUA asincrone non garantiscono una particolare velocità di completamento. L'ora di completamento di un'operazione WUA asincrona può variare notevolmente a seconda dell'hardware del computer, della versione del sistema operativo e della configurazione di rete. Come per altre API Windows che hanno dipendenze di rete e che non contengono un parametro di timeout o una durata di timeout documentata, è consigliabile implementare meccanismi di timeout personalizzati se sono necessari tempi di risposta garantiti. Ad esempio, è possibile creare un thread di lavoro che chiama un metodo WUA asincrono e che imposta un evento o un altro oggetto di sincronizzazione al completamento dell'operazione wua asincrona; Il thread principale può quindi usare la [**funzione WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) o [**WaitForMultipleObjects,**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjects) che consente di specificare un valore di timeout.
-   Quando si termina una ricerca, un download, un'installazione o una disinstallazione degli aggiornamenti, è possibile usare [**IUpdateSearcher::EndSearch**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-endsearch), [**IUpdateDowloader::EndDownload**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatedownloader), [**IUpdateInstaller::EndInstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-endinstall) [**e IUpdateInstaller::EndUninstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-enduninstall) da qualsiasi thread.
-   Quando si avvia una ricerca, un download, un'installazione o una disinstallazione di aggiornamenti tramite [**IUpdateSearcher::BeginSearch**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-beginsearch), [**IUpdateDownloader::BeginDownload**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-begindownload), [**IUpdateInstaller::BeginInstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-begininstall) [**e IUpdateInstaller::BeginUninstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-beginuninstall), assicurarsi di mantenere autorizzazioni di accesso sufficienti quando si rilasciano riferimenti a oggetti API WUA.
    -   Assicurarsi che tutti gli oggetti callback usati nell'operazione asincrona non siano referenziati prima di eliminarli. Attendere che il conteggio dei riferimenti di un oggetto callback torni al valore iniziale prima di eliminare il valore.
    -   Il riferimento all'oggetto processo restituito dal metodo **Begin** corrispondente deve essere controllato da un oggetto diverso dagli oggetti callback. Usare un oggetto diverso dagli oggetti callback per evitare riferimenti circolari.
    -   Se si tenta di controllare il riferimento all'oggetto processo usando un oggetto callback, è necessario chiamare il metodo [**IDownloadJob::CleanUp**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadjob-cleanup), [**IInstallationJob::CleanUp**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationjob-cleanup)o [**ISearchJob::CleanUp**](/windows/desktop/api/Wuapi/nf-wuapi-isearchjob-cleanup) all'esterno della funzione di callback per disconnettere l'oggetto processo dall'oggetto callback. È necessario eseguire questa operazione prima di rilasciare il riferimento all'oggetto processo restituito dal **metodo Begin.**
-   Assicurarsi che le operazioni WUA asincrone siano state completate. Windows L'host di script può terminare uno script quando tutti i comandi all'esterno di qualsiasi funzione sono completi, anche se l'API WUA contiene ancora riferimenti all'oggetto callback.
    -   Usare uno dei metodi **CleanUp** o fare in modo che la funzione di callback imposta una variabile globale condivisa al completamento.
    -   Non chiamare [**mai IDownloadJob::CleanUp,**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadjob-cleanup) [**IInstallationJob::CleanUp**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationjob-cleanup)o [**ISearchJob::CleanUp**](/windows/desktop/api/Wuapi/nf-wuapi-isearchjob-cleanup) su un oggetto processo nella relativa funzione di callback.
    -   Per garantire la sequenza di pulizia corretta in uno script in esecuzione in Windows Internet Explorer, chiamare il metodo **CleanUp** su tutti gli oggetti processo durante l'elaborazione di window.onbeforeunload.
-   Non usare tipi di dati definiti dall'utente (UDT) per operazioni WUA asincrone. Il tipo non è supportato da [**IUpdateSearcher::BeginSearch**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-beginsearch), [**IUpdateDownloader::BeginDownload**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-begindownload), [**IUpdateInstaller::BeginInstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-begininstall)o [**IUpdateInstaller::BeginUninstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-beginuninstall).

 

 
