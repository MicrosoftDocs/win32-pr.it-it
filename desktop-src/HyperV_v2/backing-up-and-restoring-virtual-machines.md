---
description: Hyper-V usa il Servizio Copia Shadow del volume (VSS) per eseguire il backup e il ripristino delle macchine virtuali.
ms.assetid: 94C67F22-658D-49DD-9588-6BB4FCF7ADA9
title: Backup e ripristino di macchine virtuali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecf5a0db5bf6956557c22445d5745dbaede03389cf6ead7467b32b65e76c59b5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119914041"
---
# <a name="backing-up-and-restoring-virtual-machines"></a>Backup e ripristino di macchine virtuali

Hyper-V usa il Servizio Copia Shadow del volume (VSS) per eseguire il backup e il ripristino delle macchine virtuali. Se i servizi di integrazione di backup (snapshot del volume) sono installati nel sistema operativo guest, viene installato un richiedente vss che consentirà ai writer VSS nel sistema operativo guest di partecipare al backup della macchina virtuale. Per informazioni dettagliate, vedere le sezioni seguenti:

-   [Backup delle macchine virtuali](#backing-up-the-virtual-machines)
-   [Ripristino delle macchine virtuali](#restoring-the-virtual-machines)
-   [Clustering di failover e VsS Hyper-V](#failover-clustering-and-hyper-v-vss)
-   [Informazioni dettagliate su VsS Writer di Hyper-V](#details-on-the-hyper-v-vss-writer)
-   [Argomenti correlati](#related-topics)

## <a name="backing-up-the-virtual-machines"></a>Backup delle macchine virtuali

Hyper-V usa uno dei due meccanismi per eseguire il backup di ogni macchina virtuale. Il meccanismo di backup predefinito è denominato metodo "Saved State", in cui la macchina virtuale viene messa in uno stato salvato durante l'elaborazione dell'evento PrepareForSnapshot, vengono evasi snapshot dei volumi appropriati e la macchina virtuale viene restituita allo stato precedente durante l'elaborazione dell'evento PostSnapshot.

L'altro meccanismo di backup è denominato metodo "Snapshot vm figlio", che usa vss all'interno della macchina virtuale figlio per partecipare al backup. Per il supporto del metodo "Snapshot vm figlio", è necessario che siano soddisfatte tutte le condizioni seguenti:

-   Il servizio di integrazione backup (snapshot del volume) è installato e in esecuzione nella macchina virtuale figlio. Il nome del servizio è "Richiedente copia shadow del volume Hyper-V".
-   La macchina virtuale figlio deve essere in esecuzione.
-   Il percorso del file di snapshot per la macchina virtuale è impostato sullo stesso volume nel sistema operativo host dei file VHD per la macchina virtuale.
-   Tutti i volumi nella macchina virtuale figlio sono dischi di base e non sono presenti dischi dinamici.
-   Tutti i dischi nella macchina virtuale figlio devono usare un file system che supporti gli snapshot, ad esempio NTFS.

In generale, il processo di backup delle macchine virtuali è identico a quello descritto in Panoramica dell'elaborazione di [un backup in VSS.](/windows/desktop/VSS/overview-of-processing-a-backup-under-vss) Il comportamento univoco si verifica quando l'VSS writer Hyper-V (parte del servizio "Gestione macchine virtuali Hyper-V") elabora l'evento PrepareForSnapshot. Se il backup è stato eseguito usando il metodo "Snapshot vm figlio", viene eseguita un'ulteriore elaborazione, ma non è visibile alla macchina virtuale figlio.

La procedura seguente descrive come eseguire il backup delle macchine virtuali.

**Per eseguire il backup di macchine virtuali**

1.  Per ogni macchina virtuale nei metadati del writer, se viene usato il metodo "Saved State" (Stato salvato), la macchina virtuale viene messa in uno stato salvato. Per le macchine virtuali che usano il metodo "Snapshot vm figlio", il servizio richiedente copia shadow del volume Hyper-V nella macchina virtuale figlio elabora il backup come descritto in Panoramica dell'elaborazione di un backup nel Servizio Copia Shadow del [volume.](/windows/desktop/VSS/overview-of-processing-a-backup-under-vss) Tutti gli eventi VSS nella macchina virtuale figlio si verificano durante l'elaborazione del sistema operativo host dell'evento PrepareForSnapshot.
2.  Dopo che tutte le macchine virtuali sono state salvate o sono stati evasi snapshot, il VSS writer Hyper-V viene restituito dall'evento PrepareForSnapshot. L'elaborazione non viene eseguita dal VSS writer Hyper-V durante gli eventi Freeze e Thaw.
3.  Quando il VSS writer Hyper-V elabora l'evento PostSnapshot, le macchine virtuali di cui è stato eseguito il backup con il metodo "Saved State" e che sono state salvate dal VSS writer Hyper-V vengono restituite allo stato in cui si trovavano prima dell'avvio del backup. Per le macchine virtuali di cui è stato eseguito il backup usando il metodo "Child VM Snapshot", viene eseguito il rollback dell'immagine host dei file VHD che hanno creato gli snapshot nello snapshot creato durante l'elaborazione dell'evento PrepareForSnapshot. Questa elaborazione viene eseguita indipendentemente dai writer VSS nelle macchine virtuali figlio, quindi gli snapshot esersi devono essere recuperabili automaticamente. (**VSS \_ VOLSNAP \_ ATTR \_ NO \_ AUTORECOVERY** non è impostato nel contesto.

I backup parziali non sono supportati. Se una macchina virtuale non riesce a creare uno snapshot, non verrà eseguito il backup delle macchine virtuali.

> [!Note]  
> I dischi pass-through e iSCSI non sono visibili per il sistema operativo host e pertanto non sono sottoposti a backup dal VSS writer Hyper-V. I backup di questi volumi devono essere e completati interamente nella macchina virtuale.

 

## <a name="restoring-the-virtual-machines"></a>Ripristino delle macchine virtuali

Il ripristino delle macchine virtuali viene eseguito interamente dal sistema operativo host. I vss writer nelle macchine virtuali figlio non sono coinvolti.

La procedura seguente descrive come ripristinare le macchine virtuali.

**Per ripristinare le macchine virtuali**

1.  Durante l'elaborazione dell'evento PreRestore, il VSS writer Hyper-V disattiva ed elimina tutte le macchine virtuali che stanno per essere ripristinate.
2.  Dopo che tutti i vss writer hanno elaborato l'evento PreRestore, i file vengono ripristinati.
3.  Durante l'elaborazione dell'evento PostRestore, il VSS writer Hyper-V chiama il [**metodo IVssComponent::GetFileRestoreStatus.**](/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-getfilerestorestatus) Se il valore restituito non è **VSS \_ RS \_ ALL,** il VSS writer Hyper-V chiama il metodo [**SetWriterFailure**](/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-setwriterfailure) e restituisce **False** dal [**metodo OnPostRestore.**](/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onpostrestore)
4.  Per ogni macchina virtuale ripristinata, il VSS writer Hyper-V registra la macchina virtuale con il servizio di gestione di Hyper-V. Se la macchina virtuale viene ripristinata in un percorso non predefinito, viene creato un collegamento simbolico nel percorso predefinito che si collega a tale percorso.
5.  Per ogni disco rigido virtuale ripristinato, il percorso viene confrontato con quello specificato per la macchina virtuale. Se la posizione è diversa, la configurazione viene aggiornata con la posizione corretta.
6.  La configurazione di rete viene aggiornata. Se i commutatori virtuali a cui era connessa la macchina virtuale al momento del backup continuano a uscire, vengono create nuove porte e connesse alla macchina virtuale.

## <a name="failover-clustering-and-hyper-v-vss"></a>Clustering di failover e VsS Hyper-V

L'VSS writer Hyper-V non fornisce alcuna considerazione alle macchine virtuali che fanno parte di un cluster di failover. Durante i backup del metodo "Saved State" e tutti i ripristini, la macchina virtuale viene messa nello stato salvato o eliminata completamente. Questo potrebbe essere considerato un errore dal servizio di clustering e causare il failover delle applicazioni in tali nodi in altri nodi. Per evitare questo problema durante i backup dello stato salvato, è necessario salvare lo stato della macchina virtuale usando il servizio di clustering. Per evitare questo problema durante un ripristino, è necessario che le risorse nella macchina virtuale siano offline.

## <a name="details-on-the-hyper-v-vss-writer"></a>Informazioni dettagliate su VsS Writer di Hyper-V

Nome writer: Microsoft Hyper-V VSS Writer

ID writer: 66841cd4-6ded-4f4b-8f17-fd23f8ddc3de

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Panoramica dell'elaborazione di un backup in VSS](/windows/desktop/VSS/overview-of-processing-a-backup-under-vss)
</dt> <dt>

[Panoramica dell'elaborazione di un ripristino in VSS](/windows/desktop/VSS/overview-of-processing-a-restore-under-vss)
</dt> </dl>

 

 
