---
title: Il servizio dischi virtuali sta passando all'API di gestione archiviazione di Windows
description: Il servizio dischi virtuali sta passando all'API di gestione archiviazione di Windows
ms.assetid: AB2A7D08-03B2-4595-A8EC-805D111A0E89
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ceea3ffe82358737ca8f39e9ef6db0bdb1f116ef
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/01/2020
ms.locfileid: "104399811"
---
# <a name="virtual-disk-service-is-transitioning-to-windows-storage-management-api"></a>Il servizio dischi virtuali sta passando all'API di gestione archiviazione di Windows

## <a name="platforms"></a>Piattaforme

**Client** -Windows 8  
**Server** : Windows Server 2012  


## <a name="description"></a>Descrizione

A partire da Windows 8 e Windows Server 2012, l'interfaccia COM del servizio dischi virtuali viene sostituita dall'API di gestione dell'archiviazione, un'interfaccia di programmazione basata su WMI. Per gestire i sottosistemi di archiviazione (Windows), i dischi, le partizioni e i volumi, si consiglia vivamente di usare l'API di gestione dell'archiviazione. Per altre informazioni, vedere [API di gestione dell'archiviazione di Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).

Per tutti gli utilizzi tranne i volumi di avvio speculare (usando un volume mirror per ospitare il sistema operativo), i dischi dinamici sono deprecati. Per i dati che richiedono resilienza in caso di errore dell'unità, usare spazi di archiviazione, una soluzione di virtualizzazione dell'archiviazione resiliente. Per altre informazioni, vedere [Storage Spaces Technical Preview](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831739(v=ws.11)).

È possibile continuare a usare DiskPart, DiskRAID e gestione disco durante il periodo di deprecazione, ma questi strumenti non funzioneranno con gli spazi di archiviazione o con altre nuove API di gestione dell'archiviazione di Windows basate sul Strumentazione gestione Windows (WMI) o con utilità di gestione dell'archiviazione in box o client.


| API | Sottosistemi di archiviazione | Dischi di base | Dischi dinamici | Spazi di archiviazione |
| --- | --- | --- | --- | --- |
| VDS | Sì | Sì | Sì | No |
| WMI | Sì | Sì | No | Sì |
| DiskPart | n/d | Sì | Sì | No |
| DiskRAID |  Sì | n/d | n/d | n/d |
| GUI di gestione disco | n/d | Sì | Sì | No |
| PowerShell | Sì | Sì | No | Sì |
| Pannello di controllo spazi di archiviazione | n/d | No | No | Sì |


Il risultato di questa transizione sarà aumentare la resilienza, la disponibilità e la scalabilità dell'archiviazione; un linguaggio di script e di programmazione unificato, costi ridotti per la gestione dell'archiviazione e una gestione più semplice per l'archiviazione remota.

## <a name="manifestation"></a>Manifestazione

Le utilità DiskPart e DiskRAID usate nell'ambiente VDS non supportano i nuovi spazi di archiviazione. Analogamente, la nuova utilità PowerShell di archiviazione non supporta i dischi dinamici deprecati

## <a name="mitigation"></a>Strategia di riduzione del rischio

Microsoft consiglia di basare le nuove app per la gestione dell'archiviazione nell'API di gestione dell'archiviazione di Windows e di pianificare la transizione delle app esistenti basate sull'infrastruttura VDS all'API di gestione archiviazione di Windows durante i cicli di aggiornamento standard.

## <a name="resources"></a>Risorse

-   [API di gestione dell'archiviazione di Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)
-   [Cmdlet di archiviazione in Windows PowerShell](/powershell/module/storage/?view=win10-ps)
-   [Strumentazione gestione Windows (WMI)](../wmisdk/wmi-start-page.md)
-   [Windows PowerShell](https://msdn.microsoft.com/library/dd835506(v=VS.85).aspx)

 

 