---
description: Il Servizio dischi virtuali (VDS) gestisce un'ampia gamma di configurazioni di archiviazione, da desktop a disco singolo a array di archiviazione esterni. Il servizio espone un'API (Application Programming Interface).
ms.assetid: 536aafd2-cc04-48cc-8ee7-920efbba2a5f
title: Servizio dischi virtuali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c84217b1ca63debe3e117e33b2358e4b0e55697c02ce8e00ce7f764c1fbf692
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119137134"
---
# <a name="virtual-disk-service"></a>Servizio dischi virtuali

\[A partire Windows 8 e Windows Server 2012, l'interfaccia COM del servizio disco virtuale viene sostituita dal Windows Archiviazione API Gestione [.](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)\]

## <a name="purpose"></a>Scopo

Il Servizio dischi virtuali (VDS) gestisce un'ampia gamma di configurazioni di archiviazione, da desktop a disco singolo a array di archiviazione esterni. Il servizio espone un'API (Application Programming Interface).

## <a name="where-applicable"></a>Se applicabile

A partire da Windows 8 e Windows Server 8, l'interfaccia COM del servizio disco virtuale viene sostituita da Archiviazione API Gestione, un'interfaccia di programmazione basata su WMI. Per la gestione di sottosistemi di archiviazione, (Windows) dischi, partizioni e volumi, è consigliabile usare il Archiviazione API Gestione. Per altre informazioni, vedere [l'Windows Archiviazione API Gestione](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).

Per tutti gli utilizzi, ad eccezione dei volumi di avvio mirror (utilizzando un volume mirror per ospitare il sistema operativo), i dischi dinamici sono deprecati. Per i dati che richiedono resilienza in caso di errore dell'unità, usare Spazi di archiviazione, una soluzione di virtualizzazione dell'archiviazione resiliente. Per altre informazioni, vedere [Spazi di archiviazione Technical Preview.](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831739(v=ws.11))

Gli sviluppatori di applicazioni che usano le interfacce descritte in questa guida possono eseguire query e configurare un set eterogeneo di risorse di archiviazione fornite dal fornitore e gestite internamente. VDS nasconde alle applicazioni le complessità associate all'archiviazione, rendendo il servizio neutro sia dal fornitore che dalla tecnologia.

## <a name="developer-audience"></a>Sviluppatori

Questa documentazione è destinata agli sviluppatori di applicazioni che hanno familiarità con le funzionalità di archiviazione delle piattaforme Microsoft Windows e che hanno una conoscenza approfondita dello sviluppo COM.

La guida è destinata anche ai produttori di sottosistemi hardware che sviluppano e supportano i programmi del provider di hardware VDS.

## <a name="run-time-requirements"></a>Requisiti di runtime

VDS è supportato in Windows Server 2003, Windows Vista e versioni successive. Per informazioni sui requisiti di run-time per un particolare elemento di programmazione, vedere la sezione Requisiti della documentazione relativa a tale elemento.

L'esecuzione di applicazioni VDS a 32 bit in WOW64 è supportata, ma i provider VDS a 64 bit devono essere eseguiti come applicazioni native in versioni Windows a 64 bit.

VDS è disponibile in Microsoft Windows Software Development Kit (SDK). È possibile installare l'SDK per Windows 7 e Windows Server 2008 R2 [dall'Area download Windows .](https://www.microsoft.com/download/details.aspx?id=8279) Questa versione di Windows SDK può essere usata per sviluppare applicazioni VDS per Windows Server 2003, Windows Vista e versioni successive. È anche possibile scaricare la [versione ISO dell'SDK](https://www.microsoft.com/download/details.aspx?id=8442) dall'area Windows download.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                         | Descrizione                                                                                            |
|-----------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [Informazioni su VDS](about-vds.md)<br/>         | Descrive il modello a oggetti VDS, le strategie di configurazione dell'archiviazione e le notifiche VDS.<br/>    |
| [Uso di VDS](using-vds.md)<br/>         | Viene descritto come usare VDS per eseguire query e configurare dispositivi di archiviazione.<br/>                            |
| [Informazioni di riferimento su VDS](vds-reference.md)<br/> | Descrive costanti VDS, tipi di dati, enumerazioni, interfacce, strutture e codici di errore.<br/> |



 

 

