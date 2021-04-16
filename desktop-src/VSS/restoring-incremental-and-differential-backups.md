---
description: Il ripristino di un backup incrementale o differenziale in VSS non è significativamente diverso rispetto a qualsiasi altra operazione di ripristino VSS.
ms.assetid: 67143f6f-0bb8-4740-9289-8bbfeb7caadf
title: Ripristino di backup incrementali e differenziali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 639919ea24f12fbc036116bd89b1630321cbae54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528704"
---
# <a name="restoring-incremental-and-differential-backups"></a>Ripristino di backup incrementali e differenziali

Il ripristino di un backup incrementale o differenziale in VSS non è significativamente diverso rispetto a qualsiasi altra operazione di ripristino VSS.

Un writer può modificare le destinazioni di ripristino o la destinazione diretta della richiesta e un richiedente deve gestire i mapping del percorso alternativo e le nuove destinazioni, come per qualsiasi altro ripristino. Esistono tuttavia due problemi significativi da tenere presente durante la gestione del ripristino di un backup incrementale o differenziale, ovvero ripristini aggiuntivi e timbri di backup.

## <a name="additional-restores"></a>Ripristini aggiuntivi

Il primo problema è quello di ripristini aggiuntivi. Un operatore di backup potrebbe dover eseguire diverse operazioni di ripristino utilizzando come origine un supporto di backup incrementale o differenziale iniziale completo e successivo.

Alcuni writer, in genere come parte della gestione di un evento [*PostRestore*](vssgloss-p.md) con [**CVssWriter:: OnPostRestore**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostrestore), usano i file ripristinati per eseguire aggiornamenti dei dati attualmente su disco. Per alcuni di questi writer non è efficiente, o pericoloso, per aggiornare ripetutamente i dati su disco dai file ripristinati.

È pertanto importante che le applicazioni di backup indichino quando un componente o un set di componenti può richiedere ripristini successivi chiamando [**IVssBackupComponents:: SetAdditionalRestores**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setadditionalrestores).

Un writer chiama [**IVssComponent:: GetAdditionalRestores**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getadditionalrestores) per determinare se l'operatore di backup ha pianificato un maggior numero di ripristini del componente o del set di componenti.

Se il richiedente non ha chiamato [**IVssBackupComponents:: SetAdditionalRestores**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setadditionalrestores), [**IVssComponent:: GetAdditionalRestores**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getadditionalrestores) restituisce false e il writer può eseguire qualsiasi elaborazione successiva al ripristino necessaria.

Se è stato chiamato [**IVssBackupComponents:: SetAdditionalRestores**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setadditionalrestores) , [**IVssComponent:: GetAdditionalRestores**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getadditionalrestores) restituisce **true** e un writer deve decidere come gestire le operazioni di post-ripristino. ad esempio, il writer può scegliere di non aggiornare i dati su disco.

## <a name="backup-stamps"></a>Timbri di backup

Nell'ambito dell'operazione di backup completo precedente, un writer potrebbe avere archiviato un timbro di backup nel documento relativo ai componenti di backup del richiedente.

L'indicatore di backup viene archiviato come stringa e il formato e le informazioni non sono intelligibili per il richiedente. Pertanto, il richiedente non è in grado di utilizzare direttamente le informazioni sul timbro di backup.

L'attività consiste invece nel rendere le informazioni disponibili al writer, chiamando il metodo [**IVssBackupComponents:: SetPreviousBackupStamp**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setpreviousbackupstamp) prima della generazione di un evento [**PrepareForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) per un backup incrementale.

Il richiedente esegue questa operazione in base al componente. Un richiedente esamina le informazioni del timbro di backup del componente o del set di componenti archiviati usando [**IVssComponent:: GetBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupstamp).

Se le informazioni sul timbro di backup sono appropriate per il tipo di ripristino, il richiedente viene reso disponibile come timestamp dell'ultimo backup di un componente con il metodo [**IVssBackupComponents:: SetPreviousBackupStamp**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setpreviousbackupstamp) .

Un writer recupera le informazioni sull'indicatore di backup usando [**IVssComponent:: GetPreviousBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpreviousbackupstamp). Un writer di questa classe ha generato l'indicatore di backup iniziale, quindi il writer è in grado di decodificare questo timbro e di usare le informazioni. In base a questo, durante la gestione di un evento di [**preripristino**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) , un writer può scegliere di eseguire azioni quali la modifica delle destinazioni di ripristino o la richiesta di destinazione diretta.

 

 



