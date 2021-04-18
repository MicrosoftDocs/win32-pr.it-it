---
description: Il servizio dischi virtuali (VDS) gestisce un'ampia gamma di configurazioni di archiviazione, da desktop su disco singolo ad array di archiviazione esterni. Il servizio espone un Application Programming Interface (API).
ms.assetid: 536aafd2-cc04-48cc-8ee7-920efbba2a5f
title: Servizio dischi virtuali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcfef0c5a73fcb2e6911395c829380c4bdfe56ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312706"
---
# <a name="virtual-disk-service"></a>Servizio dischi virtuali

\[A partire da Windows 8 e Windows Server 2012, l'interfaccia COM del servizio dischi virtuali viene sostituita dall' [API di gestione archiviazione di Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

## <a name="purpose"></a>Scopo

Il servizio dischi virtuali (VDS) gestisce un'ampia gamma di configurazioni di archiviazione, da desktop su disco singolo ad array di archiviazione esterni. Il servizio espone un Application Programming Interface (API).

## <a name="where-applicable"></a>Se applicabile

A partire da Windows 8 e Windows Server 8, l'interfaccia COM del servizio dischi virtuali viene sostituita dall'API di gestione dell'archiviazione, un'interfaccia di programmazione basata su WMI. Per gestire i sottosistemi di archiviazione (Windows), i dischi, le partizioni e i volumi, si consiglia vivamente di usare l'API di gestione dell'archiviazione. Per ulteriori informazioni, vedere l' [API di gestione archiviazione di Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).

Per tutti gli utilizzi tranne i volumi di avvio speculare (usando un volume mirror per ospitare il sistema operativo), i dischi dinamici sono deprecati. Per i dati che richiedono resilienza in caso di errore dell'unità, usare spazi di archiviazione, una soluzione di virtualizzazione dell'archiviazione resiliente. Per altre informazioni, vedere [Storage Spaces Technical Preview](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831739(v=ws.11)).

Gli sviluppatori di applicazioni che utilizzano le interfacce descritte in questa guida possono eseguire query e configurare un set eterogeneo di archiviazione gestita internamente e fornita dal fornitore. VDS nasconde dalle applicazioni le complessità associate all'archiviazione, rendendo il servizio sia indipendente dal fornitore che dalla tecnologia.

## <a name="developer-audience"></a>Sviluppatori

Questa documentazione è destinata agli sviluppatori di applicazioni che hanno familiarità con le funzionalità di archiviazione delle piattaforme Microsoft Windows e che conoscono lo sviluppo COM.

La guida è destinata anche ai produttori di sottosistemi hardware che sviluppano e supportano i programmi del provider hardware VDS.

## <a name="run-time-requirements"></a>Requisiti di runtime

VDS è supportato in Windows Server 2003, Windows Vista e versioni successive. Per informazioni sui requisiti della fase di esecuzione per un particolare elemento di programmazione, vedere la sezione requisiti della documentazione relativa a tale elemento.

L'esecuzione di applicazioni VDS a 32 bit in WOW64 è supportata, ma i provider VDS a 64 bit devono essere eseguiti come applicazioni native nelle versioni di Windows a 64 bit.

VDS è disponibile nel Software Development Kit (SDK) di Microsoft Windows. È possibile installare l'SDK per Windows 7 e Windows Server 2008 R2 dall' [area download di Windows](https://www.microsoft.com/download/details.aspx?id=8279). Questa versione di Windows SDK può essere usata per sviluppare applicazioni VDS per Windows Server 2003, Windows Vista e versioni successive. È anche possibile scaricare la [versione ISO](https://www.microsoft.com/download/details.aspx?id=8442) dell'SDK dall'area download di Windows.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                         | Descrizione                                                                                            |
|-----------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [Informazioni su VDS](about-vds.md)<br/>         | Descrive il modello a oggetti VDS, le strategie di configurazione dell'archiviazione e le notifiche VDS.<br/>    |
| [Uso di VDS](using-vds.md)<br/>         | Viene descritto come utilizzare VDS per eseguire query e configurare i dispositivi di archiviazione.<br/>                            |
| [Riferimento VDS](vds-reference.md)<br/> | Descrive le costanti VDS, i tipi di dati, le enumerazioni, le interfacce, le strutture e i codici di errore.<br/> |



 

 

