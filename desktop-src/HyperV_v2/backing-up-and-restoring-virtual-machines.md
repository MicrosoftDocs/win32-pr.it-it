---
description: Hyper-V usa il Servizio Copia Shadow del volume (VSS) per eseguire il backup e il ripristino delle macchine virtuali.
ms.assetid: 94C67F22-658D-49DD-9588-6BB4FCF7ADA9
title: Backup e ripristino di macchine virtuali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f9cf6d5b80a4c7392fb38e893a4fafad3f90435
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312336"
---
# <a name="backing-up-and-restoring-virtual-machines"></a>Backup e ripristino di macchine virtuali

Hyper-V usa il Servizio Copia Shadow del volume (VSS) per eseguire il backup e il ripristino delle macchine virtuali. Se i servizi di integrazione di backup (snapshot del volume) sono installati nel sistema operativo guest, viene installato un richiedente VSS che consentirà ai writer VSS nel sistema operativo guest di partecipare al backup della macchina virtuale. Per informazioni dettagliate, vedere le sezioni seguenti:

-   [Esecuzione del backup delle macchine virtuali](#backing-up-the-virtual-machines)
-   [Ripristino delle macchine virtuali](#restoring-the-virtual-machines)
-   [Clustering di failover e VSS di Hyper-V](#failover-clustering-and-hyper-v-vss)
-   [Dettagli sul writer VSS di Hyper-V](#details-on-the-hyper-v-vss-writer)
-   [Argomenti correlati](#related-topics)

## <a name="backing-up-the-virtual-machines"></a>Esecuzione del backup delle macchine virtuali

Hyper-V usa uno dei due meccanismi per eseguire il backup di ogni macchina virtuale. Il meccanismo di backup predefinito viene chiamato metodo "stato salvato", in cui la macchina virtuale viene spostata in uno stato salvato durante l'elaborazione dell'evento PrepareForSnapshot, vengono presi gli snapshot dei volumi appropriati e la macchina virtuale viene restituita allo stato precedente durante l'elaborazione dell'evento PostSnapshot.

L'altro meccanismo di backup è denominato "snapshot VM figlio", che utilizza VSS all'interno della macchina virtuale figlio per partecipare al backup. Per poter supportare il metodo "snapshot VM figlio", è necessario che siano soddisfatte tutte le condizioni seguenti:

-   Il servizio di integrazione backup (snapshot del volume) è installato e in esecuzione nella macchina virtuale figlio. Il nome del servizio è "richiedente copia shadow del volume Hyper-V".
-   La macchina virtuale figlio deve essere nello stato in esecuzione.
-   Il percorso del file di snapshot per la macchina virtuale è impostato sullo stesso volume del sistema operativo host dei file VHD della macchina virtuale.
-   Tutti i volumi della macchina virtuale figlio sono dischi di base e non ci sono dischi dinamici.
-   Tutti i dischi della macchina virtuale figlio devono usare un file system che supporti gli snapshot, ad esempio NTFS.

In generale, il processo di backup delle macchine virtuali è identico a quello descritto in [Panoramica dell'elaborazione di un backup in VSS](/windows/desktop/VSS/overview-of-processing-a-backup-under-vss). Il comportamento univoco si verifica quando l'VSS writer Hyper-V (parte del servizio "Virtual Machine Management" di Hyper-V) elabora l'evento PrepareForSnapshot. Se il backup è stato eseguito usando il metodo "snapshot VM figlio", l'elaborazione aggiuntiva è stata completata ma non è visibile alla macchina virtuale figlio.

Nella procedura seguente viene descritto come eseguire il backup di macchine virtuali.

**Per eseguire il backup di macchine virtuali**

1.  Per ogni macchina virtuale nei metadati del writer, se viene usato il metodo "stato salvato", la macchina virtuale viene messa in uno stato salvato. Per le macchine virtuali che usano il metodo "snapshot VM figlio", il servizio richiedente copia shadow del volume Hyper-V nella macchina virtuale figlio elabora il backup come descritto in dettaglio in [Panoramica sull'elaborazione di un backup in VSS](/windows/desktop/VSS/overview-of-processing-a-backup-under-vss). Tutti gli eventi VSS nella macchina virtuale figlio si verificano durante l'elaborazione del sistema operativo host dell'evento PrepareForSnapshot.
2.  Dopo che tutte le macchine virtuali sono state inserite nello stato salvato o hanno eseguito snapshot, l'VSS writer Hyper-V viene restituito dall'evento PrepareForSnapshot. Nessuna elaborazione viene eseguita dal VSS writer Hyper-V durante gli eventi di blocco e di sblocco.
3.  Quando l'VSS writer Hyper-V elabora l'evento di post-snapshot, le macchine virtuali di cui è stato eseguito il backup con il metodo "stato salvato" e inserite in uno stato salvato dal VSS writer Hyper-V vengono restituite allo stato in cui si trovavano prima dell'avvio del backup. Per le macchine virtuali di cui è stato eseguito il backup con il metodo "snapshot VM figlio", viene eseguito il rollback dell'immagine host dei file VHD con gli snapshot eseguiti durante l'elaborazione dell'evento PrepareForSnapshot. Questa elaborazione viene eseguita indipendentemente dai writer VSS nelle macchine virtuali figlio, in modo che gli snapshot eseguiti debbano essere ripristinabili automaticamente. (**VSS VolSnap non è impostato \_ \_ \_ alcun \_ recupero automatico** nel contesto).

I backup parziali non sono supportati. Se una macchina virtuale non riesce a creare uno snapshot, non verrà eseguito il backup di macchine virtuali.

> [!Note]  
> I dischi pass-through e iSCSI non sono visibili al sistema operativo host e pertanto non sono supportati dal VSS writer Hyper-V. I backup di questi volumi devono essere eseguiti interamente nella macchina virtuale.

 

## <a name="restoring-the-virtual-machines"></a>Ripristino delle macchine virtuali

Il ripristino delle macchine virtuali viene eseguito interamente dal sistema operativo host. i writer VSS nelle macchine virtuali figlio non sono interessati.

Nella procedura riportata di seguito viene descritto come ripristinare le macchine virtuali.

**Per ripristinare le macchine virtuali**

1.  Durante l'elaborazione dell'evento di preripristino, Hyper-V VSS writer disattiva ed Elimina tutte le macchine virtuali che stanno per essere ripristinate.
2.  Dopo che tutti i writer VSS hanno elaborato l'evento di preripristino, i file vengono ripristinati.
3.  Durante l'elaborazione dell'evento PostRestore, l'VSS writer Hyper-V chiama il metodo [**IVssComponent:: GetFileRestoreStatus**](/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-getfilerestorestatus) . Se il valore restituito non **è \_ All VSS RS \_ ALL**, il VSS Writer Hyper-V chiama il metodo [**SetWriterFailure**](/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-setwriterfailure) e restituisce **false** dal metodo [**OnPostRestore**](/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onpostrestore) .
4.  Per ogni macchina virtuale ripristinata, Hyper-V VSS writer registra la macchina virtuale con il servizio di gestione Hyper-V. Se la macchina virtuale viene ripristinata in un percorso non predefinito, viene creato un collegamento simbolico nel percorso predefinito che si collega a tale posizione.
5.  Per ogni disco rigido virtuale che è stato ripristinato, il percorso viene confrontato con quello specificato per la macchina virtuale. Se il percorso è diverso, la configurazione viene aggiornata con il percorso appropriato.
6.  La configurazione di rete viene aggiornata. Se i commutatori virtuali a cui la macchina virtuale è stata connessa quando è stato eseguito il backup sono ancora in uscita, vengono create nuove porte e connesse alla macchina virtuale.

## <a name="failover-clustering-and-hyper-v-vss"></a>Clustering di failover e VSS di Hyper-V

Il VSS writer Hyper-V non fornisce alcuna considerazione per le macchine virtuali che fanno parte di un cluster di failover. Durante i backup del metodo "stato salvato" e tutti i ripristini, la macchina virtuale viene inserita nello stato salvato o completamente eliminata. Questa situazione verrebbe considerata come un errore del servizio di clustering e causerebbe il failover delle applicazioni su tali nodi in altri nodi. Per evitare questo problema durante i backup con stato "salvato", lo stato della macchina virtuale deve essere salvato utilizzando il servizio clustering. Per evitare questo problema, è necessario portare offline le risorse della macchina virtuale.

## <a name="details-on-the-hyper-v-vss-writer"></a>Dettagli sul writer VSS di Hyper-V

Nome writer: Microsoft Hyper-V VSS Writer

ID Writer: 66841CD4-6DED-4F4B-8F17-FD23F8DDC3DE

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Cenni preliminari sull'elaborazione di un backup in VSS](/windows/desktop/VSS/overview-of-processing-a-backup-under-vss)
</dt> <dt>

[Panoramica dell'elaborazione di un ripristino in VSS](/windows/desktop/VSS/overview-of-processing-a-restore-under-vss)
</dt> </dl>

 

 
