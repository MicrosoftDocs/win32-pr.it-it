---
title: Il servizio Dischi virtuali sta per essere Windows Archiviazione API Gestione
description: Il servizio Dischi virtuali sta per essere Windows Archiviazione API Gestione
ms.assetid: AB2A7D08-03B2-4595-A8EC-805D111A0E89
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a45e25452ae0b6bb20e0ca04130b7fa2fd64f2a191d504380f973f663b7931ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117852038"
---
# <a name="virtual-disk-service-is-transitioning-to-windows-storage-management-api"></a>Il servizio Dischi virtuali sta per essere Windows Archiviazione API Gestione

## <a name="platforms"></a>Piattaforme

**Client** : Windows 8  
**Server** - Windows Server 2012  


## <a name="description"></a>Descrizione

A partire da Windows 8 e Windows Server 2012, l'interfaccia COM del servizio dischi virtuali viene sostituita dal Archiviazione API Gestione, un'interfaccia di programmazione basata su WMI. Per la gestione di sottosistemi di archiviazione, (Windows) dischi, partizioni e volumi, è consigliabile usare il Archiviazione API Gestione. Per altre informazioni, [vedere](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)Windows Archiviazione API Gestione .

Per tutti gli utilizzi, ad eccezione dei volumi di avvio mirror (che usano un volume mirror per ospitare il sistema operativo), i dischi dinamici sono deprecati. Per i dati che richiedono resilienza in caso di errore dell'unità, usare Spazi di archiviazione, una soluzione di virtualizzazione dell'archiviazione resiliente. Per altre informazioni, vedere [Spazi di archiviazione Technical Preview.](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831739(v=ws.11))

È possibile continuare a usare DiskPart, DiskRAID e Gestione disco durante il periodo di deprecazione, ma questi strumenti non funzioneranno con Spazi di archiviazione o con altre nuove API di gestione di Windows Archiviazione basate su Windows Management Instrumentation (WMI) o utilità o client di gestione dell'archiviazione in-box.


| API | Sottosistemi di archiviazione | Dischi di base | Dischi dinamici | Spazi di archiviazione |
| --- | --- | --- | --- | --- |
| Vds | Sì | Sì | Sì | No |
| WMI | Sì | Sì | No | Sì |
| DiskPart | n/d | Sì | Sì | No |
| DiskRAID |  Sì | n/d | n/d | n/d |
| Interfaccia utente grafica di Mgmt del disco | n/d | Sì | Sì | No |
| PowerShell | Sì | Sì | No | Sì |
| Spazi di archiviazione Pannello di controllo | n/d | No | No | Sì |


Il risultato di questa transizione sarà una maggiore resilienza, disponibilità e scalabilità dell'archiviazione; un linguaggio di scripting e programmazione unificato, costi di gestione dell'archiviazione ridotti e una gestione più semplice dell'archiviazione remota.

## <a name="manifestation"></a>Manifestazione

Le utilità DiskPart e DiskRAID usate nell'ambiente VDS non supportano il nuovo Spazi di archiviazione. Analogamente, la nuova Archiviazione di PowerShell non supporta i dischi dinamici deprecati

## <a name="mitigation"></a>Strategia di riduzione del rischio

Microsoft consiglia di basare le nuove app di gestione dell'archiviazione sul Windows Archiviazione API Gestione e di pianificare la transizione delle app esistenti basate sull'infrastruttura VDS al Windows Archiviazione API Gestione durante i cicli di aggiornamento standard.

## <a name="resources"></a>Risorse

-   [API di gestione dell'archiviazione di Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)
-   [Cmdlet di archiviazione in Windows PowerShell](/powershell/module/storage/?view=win10-ps)
-   [Strumentazione gestione Windows (WMI)](../wmisdk/wmi-start-page.md)
-   [Windows PowerShell](https://msdn.microsoft.com/library/dd835506(v=VS.85).aspx)

 

 