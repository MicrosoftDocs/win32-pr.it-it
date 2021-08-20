---
description: Microsoft Hyper-V server offre un ambiente di gestione delle macchine virtuali scalabile, affidabile e a disponibilità elevata. Il software delle macchine virtuali Hyper-V consolida i server e gli ambienti di sviluppo e test.
ms.assetid: 3359A33F-528B-4955-8B37-30523B8AD33A
title: Provider WMI Hyper-V (V2)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b82156754f085196eaece86bb4996c1b4a0bb8348e1566894ee78d4921676f96
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014249"
---
# <a name="hyper-v-wmi-provider-v2"></a>Provider WMI Hyper-V (V2)

## <a name="purpose"></a>Scopo

Hyper-V offre un ambiente di elaborazione server virtualizzato scalabile, affidabile e a disponibilità elevata. Consente l'esecuzione simultanea di uno o più sistemi operativi guest in un singolo computer fisico. Gli usi chiave per la tecnologia delle macchine virtuali includono:

-   Consolidamento dei server
-   Consolidamento degli ambienti di sviluppo e test
-   Ripristino di emergenza semplificato

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                                 | Descrizione                                                                                                                                                                                                                              |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Informazioni sul provider WMI Hyper-V](about-the-virtualization-wmi-provider.md)<br/>                | Il provider WMI per Hyper-V consente agli sviluppatori e agli scripter di creare rapidamente strumenti, utilità e miglioramenti personalizzati per la piattaforma di virtualizzazione. Le interfacce WMI possono gestire tutti gli aspetti dei servizi Hyper-V.<br/> |
| [Uso del provider WMI Hyper-V](using-the-virtualization-wmi-provider.md)<br/>                | Negli argomenti seguenti viene descritto come usare il provider WMI Hyper-V.<br/>                                                                                                                                                            |
| [Classi WMI Hyper-V](hyper-v-wmi-classes.md)<br/>                                             | Di seguito sono riportate le classi WMI di Hyper-V.<br/>                                                                                                                                                                                    |
| [API di monitoraggio dell'integrità delle applicazioni Hyper-V](hyper-v-application-health-monitoring-api.md)<br/> | L'API di monitoraggio dell'integrità delle applicazioni Hyper-V viene usata per monitorare lo stato di integrità delle applicazioni in esecuzione in una macchina virtuale.<br/>                                                                                               |
| [API di replica Hyper-V](hyper-v-replication-api.md)<br/>                                     | L'API di replica Hyper-V viene usata per controllare la replica delle macchine virtuali e il ripristino del failover.<br/>                                                                                                                             |
| [API metriche Hyper-V](hyper-v-metrics-api.md)<br/>                                             | L'API metriche di Hyper-V viene usata per monitorare lo stato di integrità delle applicazioni in esecuzione in una macchina virtuale.<br/>                                                                                                                     |
| [API di rete Hyper-V](hyper-v-networking-api.md)<br/>                                       | L'API di rete Hyper-V viene usata per controllare la rete in Hyper-V.<br/>                                                                                                                                                          |
| [API di migrazione Hyper-V](hyper-v-storage-migration-api.md)<br/>                                 | L'API di migrazione Hyper-V viene usata per controllare l'archiviazione e la migrazione in tempo reale in Hyper-V.<br/>                                                                                                                                           |
| [API di gestione Fibre Channel Hyper-V](hyper-v-virtual-fiber-channels-api.md)<br/>                | L'API Fibre Channel virtuale Hyper-V viene usata per controllare le schede Fibre Channel virtuali in Hyper-V.<br/>                                                                                                                           |
| [API di posizionamento di macchine virtuali Hyper-V](hyper-v-vm-placement-api.md)<br/>                                   | L'API di posizionamento delle macchine virtuali Hyper-V contiene le informazioni di compatibilità per le macchine virtuali o il sistema del computer di hosting.<br/>                                                                                                        |
| [Classi di soglia](threshold-classes.md)<br/>                                                 | Contiene le classi introdotte in Windows 10.<br/>                                                                                                                                                                                |
| [Classi RS2](redstone-classes.md)<br/>                                                        | Contiene le nuove classi per Windows 10 versione 1703.<br/>                                                                                                                                                                        |
| [Classi RS3](rs3-classes.md)<br/>                                                             | Contiene le nuove classi per Windows 10 versione 1709.<br/>                                                                                                                                                                        |
| [Glossario di Hyper-V](virtualization-glossary.md)<br/>                                            | Glossario dei termini usati nella documentazione di Windows Virtualization SDK.<br/>                                                                                                                                                       |



 

## <a name="run-time-requirements"></a>Requisiti di runtime

I servizi Hyper-V richiedono un sistema basato su x64 che supporta la virtualizzazione assistita da hardware che esegue Hyper-V. I programmi che interagiscono con le interfacce WMI di Hyper-V, tuttavia, possono essere eseguiti in remoto in qualsiasi sistema che supporta WMI.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Hyper-V (Windows raccolta tecnica di Server 2008 R2)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc753637(v=ws.10))
</dt> <dt>

[Strumentazione gestione Windows (WMI)](/windows/desktop/WmiSdk/wmi-start-page)
</dt> <dt>

[Windows Virtualizzazione server](https://www.microsoft.com/windowsserver2008/virtualization/default.mspx)
</dt> </dl>

 

