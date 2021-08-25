---
description: Il ripristino di un backup incrementale o differenziale in VSS non è notevolmente diverso da qualsiasi altra operazione di ripristino vss.
ms.assetid: 67143f6f-0bb8-4740-9289-8bbfeb7caadf
title: Ripristino di backup incrementali e differenziali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcc0c2df57e2f7c0f21436248ddaa46231c7bf6440c76a38f4d1c92ab2adf97f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119864051"
---
# <a name="restoring-incremental-and-differential-backups"></a>Ripristino di backup incrementali e differenziali

Il ripristino di un backup incrementale o differenziale in VSS non è notevolmente diverso da qualsiasi altra operazione di ripristino vss.

Un writer può modificare le destinazioni di ripristino o richiedere la destinazione diretta e un richiedente deve gestire i mapping di percorsi alternativi e le nuove destinazioni, come per qualsiasi altro ripristino. Esistono tuttavia due problemi significativi da tenere presenti nella gestione del ripristino di un backup incrementale o differenziale: ripristini aggiuntivi e indicatori di backup.

## <a name="additional-restores"></a>Ripristini aggiuntivi

Il primo problema è quello dei ripristini aggiuntivi. Un operatore di backup potrebbe dover eseguire diverse operazioni di ripristino usando come origine un supporto di backup incrementale o differenziale iniziale e incrementale successivo.

Alcuni writer, in genere come parte della gestione di un evento [*PostRestore*](vssgloss-p.md) tramite [**CVssWriter::OnPostRestore,**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostrestore)usano i file ripristinati per eseguire aggiornamenti dei dati attualmente su disco. Per alcuni di questi writer è inefficiente o pericoloso aggiornare ripetutamente i dati su disco dai file ripristinati.

È quindi importante che le applicazioni di backup indichi quando un componente o un set di componenti può richiedere ripristini successivi chiamando [**IVssBackupComponents::SetAdditionalRestores**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setadditionalrestores).

Un writer chiama [**IVssComponent::GetAdditionalRestores**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getadditionalrestores) per determinare se l'operatore di backup ha pianificato più ripristini del componente o del set di componenti.

Se il richiedente non ha chiamato [**IVssBackupComponents::SetAdditionalRestores,**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setadditionalrestores) [**IVssComponent::GetAdditionalRestores**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getadditionalrestores) restituisce false e il writer può eseguire qualsiasi elaborazione post-ripristino a cui è necessario.

Se È stato chiamato [**IVssBackupComponents::SetAdditionalRestores,**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setadditionalrestores) [**IVssComponent::GetAdditionalRestores**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getadditionalrestores) restituisce **true** e un writer deve decidere come gestire le operazioni di post-ripristino. Ad esempio, il writer può scegliere di non aggiornare i dati su disco.

## <a name="backup-stamps"></a>Stamp di backup

Come parte dell'operazione di backup completo precedente, è possibile che un writer abbia archiviato un indicatore di backup nel documento dei componenti di backup del richiedente.

Lo stamp di backup viene archiviato come stringa e il formato e le informazioni non sono comprensibili per il richiedente. Pertanto, il richiedente non può usare direttamente le informazioni del timbro di backup.

L'attività è invece quella di rendere disponibili le informazioni al writer chiamando il metodo [**IVssBackupComponents::SetPreviousBackupStamp**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setpreviousbackupstamp) prima della generazione di un evento [**PrepareForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) per un backup incrementale.

Il richiedente esegue questa operazione componente per componente. Un richiedente esamina le informazioni sul timestamp di backup del componente o del set di componenti archiviate [**usando IVssComponent::GetBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupstamp).

Se le informazioni sul timestamp di backup sono appropriate per il tipo di ripristino che il richiedente sta effettuando, le rende disponibili come timestamp dell'ultimo backup di un componente con il metodo [**IVssBackupComponents::SetPreviousBackupStamp.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setpreviousbackupstamp)

Un writer recupera le informazioni dello stamp di backup [**usando IVssComponent::GetPreviousBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpreviousbackupstamp). Un writer di questa classe ha generato l'indicatore di backup iniziale, in modo che il writer sia in grado di decodificare questo stamp e usare le informazioni. In base a questo, durante la gestione di un evento [**PreRestore,**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) un writer può scegliere di eseguire azioni come la modifica delle destinazioni di ripristino o la richiesta di destinazioni indirizzate.

 

 



