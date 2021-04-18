---
description: Microsoft Hyper-V Server offre un ambiente di gestione delle macchine virtuali scalabile, affidabile e a disponibilità elevata. Il software per macchine virtuali Hyper-V consolida i server e gli ambienti di sviluppo e test.
ms.assetid: 3359A33F-528B-4955-8B37-30523B8AD33A
title: Provider WMI Hyper-V (v2)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 555fd3cd1e8420c59bb5f1b8ef16480b3ddfcf4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306622"
---
# <a name="hyper-v-wmi-provider-v2"></a>Provider WMI Hyper-V (v2)

## <a name="purpose"></a>Scopo

Hyper-V offre un ambiente di elaborazione server virtualizzato scalabile, affidabile e a disponibilità elevata. Consente l'esecuzione simultanea di uno o più sistemi operativi guest in un singolo computer fisico. Gli utilizzi principali per la tecnologia delle macchine virtuali sono i seguenti:

-   Consolidamento dei server
-   Consolidamento di ambienti di sviluppo e test
-   Ripristino di emergenza semplificato

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                                 | Descrizione                                                                                                                                                                                                                              |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Informazioni sul provider WMI Hyper-V](about-the-virtualization-wmi-provider.md)<br/>                | Il provider WMI per Hyper-V consente agli sviluppatori e ai creatori di script di creare rapidamente strumenti, utilità e miglioramenti personalizzati per la piattaforma di virtualizzazione. Le interfacce WMI possono gestire tutti gli aspetti dei servizi Hyper-V.<br/> |
| [Uso del provider WMI Hyper-V](using-the-virtualization-wmi-provider.md)<br/>                | Negli argomenti seguenti viene descritto come utilizzare il provider WMI Hyper-V.<br/>                                                                                                                                                            |
| [Classi WMI di Hyper-V](hyper-v-wmi-classes.md)<br/>                                             | Di seguito sono riportate le classi WMI di Hyper-V.<br/>                                                                                                                                                                                    |
| [API di monitoraggio dell'integrità dell'applicazione Hyper-V](hyper-v-application-health-monitoring-api.md)<br/> | L'API di monitoraggio dell'integrità dell'applicazione Hyper-V viene usata per monitorare lo stato di integrità delle applicazioni in esecuzione in una macchina virtuale.<br/>                                                                                               |
| [API di replica Hyper-V](hyper-v-replication-api.md)<br/>                                     | L'API di replica Hyper-V viene usata per controllare la replica della macchina virtuale e il ripristino del failover.<br/>                                                                                                                             |
| [API metriche Hyper-V](hyper-v-metrics-api.md)<br/>                                             | L'API della metrica Hyper-V viene usata per monitorare lo stato di integrità delle applicazioni in esecuzione in una macchina virtuale.<br/>                                                                                                                     |
| [API di rete Hyper-V](hyper-v-networking-api.md)<br/>                                       | L'API di rete Hyper-V viene usata per controllare la rete in Hyper-V.<br/>                                                                                                                                                          |
| [API di migrazione Hyper-V](hyper-v-storage-migration-api.md)<br/>                                 | L'API di migrazione Hyper-V viene usata per controllare l'archiviazione e la migrazione in tempo reale in Hyper-V.<br/>                                                                                                                                           |
| [API Fibre Channel virtuale Hyper-V](hyper-v-virtual-fiber-channels-api.md)<br/>                | L'API Fibre Channel virtuale Hyper-V viene utilizzata per controllare le schede Fibre Channel virtuali in Hyper-V.<br/>                                                                                                                           |
| [API selezione host VM Hyper-V](hyper-v-vm-placement-api.md)<br/>                                   | L'API di posizionamento della macchina virtuale Hyper-V contiene le informazioni sulla compatibilità per le macchine virtuali o il sistema di hosting.<br/>                                                                                                        |
| [Classi soglia](threshold-classes.md)<br/>                                                 | Contiene le classi introdotte in Windows 10.<br/>                                                                                                                                                                                |
| [Classi RS2](redstone-classes.md)<br/>                                                        | Contiene le nuove classi per Windows 10, versione 1703.<br/>                                                                                                                                                                        |
| [Classi RS3](rs3-classes.md)<br/>                                                             | Contiene le nuove classi per Windows 10, versione 1709.<br/>                                                                                                                                                                        |
| [Glossario di Hyper-V](virtualization-glossary.md)<br/>                                            | Glossario dei termini usati nella documentazione di Windows Virtualization SDK.<br/>                                                                                                                                                       |



 

## <a name="run-time-requirements"></a>Requisiti di runtime

I servizi Hyper-V richiedono un sistema basato su x64 che supporta la virtualizzazione assistita mediante hardware che esegue Hyper-V. I programmi che interagiscono con le interfacce WMI di Hyper-V, tuttavia, possono essere eseguiti in modalità remota in qualsiasi sistema che supporta WMI.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Hyper-V (raccolta di documentazione tecnica di Windows Server 2008 R2)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc753637(v=ws.10))
</dt> <dt>

[Strumentazione gestione Windows (WMI)](/windows/desktop/WmiSdk/wmi-start-page)
</dt> <dt>

[Virtualizzazione di Windows Server](https://www.microsoft.com/windowsserver2008/virtualization/default.mspx)
</dt> </dl>

 

