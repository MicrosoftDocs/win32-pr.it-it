---
description: In alcune circostanze, i file di cui eseguire il backup non sono il percorso predefinito per tali file.
ms.assetid: b9e96827-a678-45ca-8ede-4508a406f071
title: Utilizzo di percorsi alternativi durante il backup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a98e93af4d12b804032a64841542e731ff77e048
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307129"
---
# <a name="working-with-alternate-paths-during-backup"></a>Utilizzo di percorsi alternativi durante il backup

In alcune circostanze, i file di cui eseguire il backup non sono il percorso predefinito per tali file.

Alcuni writer, ad esempio, non possono garantire che i dati siano stati scaricati entro la finestra temporale tra gli eventi di [*blocco*](vssgloss-f.md) e di [*sblocco*](vssgloss-t.md) . Tali writer possono scegliere di generare file duplicati contenenti un'ultima configurazione corretta nota in una directory di origine non predefinita o in un [*percorso alternativo*](vssgloss-a.md).

Il termine percorso alternativo, come usato con VSS, non deve essere confuso con il termine [*mapping del percorso alternativo*](vssgloss-a.md). I percorsi alternativi vengono usati solo durante le operazioni di backup e fanno riferimento a un'origine alternativa da cui eseguire il backup. I mapping dei percorsi alternativi vengono utilizzati solo durante le operazioni di ripristino e fanno riferimento a una destinazione alternativa per le operazioni di ripristino.

**Per utilizzare un percorso alternativo durante il backup**

1.  Durante la fase di individuazione di un'operazione di backup (vedere [Panoramica della fase di individuazione del backup](overview-of-the-backup-discovery-phase.md)) un richiedente esamina i dati dei componenti di ogni writer usando [**IVssExamineWriterMetadata:: getComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getcomponent) e ottiene le istanze dell'interfaccia [**IVssWMComponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent) .
2.  Un richiedente ottiene quindi il [*set di file*](vssgloss-f.md) gestito da ogni componente, rappresentato da istanze dell'interfaccia [**IVssWMFiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc) , chiamando il metodo [**IVssWMComponent:: GetFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getfile) .
3.  Oltre a un percorso ([**IVssWMFiledesc:: GetPath**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getpath)), una specifica del file ([**IVssWMFiledesc:: GetFilespec**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getfilespec)) e un flag di ricorsione ([**IVssWMFiledesc:: getricorsival**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getrecursive)), un oggetto [**IVssWMFiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc) può contenere un percorso alternativo (usato come percorso alternativo per le operazioni di backup e un mapping del percorso alternativo per le operazioni di ripristino) usando il metodo [**IVssWMFiledesc:: GetAlternateLocation**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation) .
4.  Se il valore restituito da [**IVssWMFiledesc:: GetAlternateLocation**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation) è diverso da null, le applicazioni di backup utilizzano tale valore anziché il valore ottenuto da [**IVssWMFiledesc:: GetPath**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getpath) per selezionare e individuare i file di cui eseguire il backup.
5.  Nonostante l'uso di un percorso alternativo, i richiedenti devono comunque rispettare la specifica del file e le impostazioni ricorsive restituite da [**IVssWMFiledesc:: GetFilespec**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getfilespec) e [**IVssWMFiledesc:: getricorsival**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getrecursive).

Si noti che, in fase di ripristino, qualsiasi percorso alternativo, ovvero un percorso alternativo restituito da un'istanza di [**IVssWMFiledesc:: GetAlternateLocation**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation) ottenuto da un'istanza di [**IVssWMComponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent), che a sua volta è stato ottenuto da un'istanza di [**IVssExamineWriterMetadata**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata) ottenuta recuperando un documento di metadati del writer archiviato, non viene utilizzato durante il ripristino.

Il percorso predefinito, restituito dal metodo [**GetPath**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getpath) della stessa istanza di [**IVssWMFiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc), viene usato per definire un percorso di ripristino oppure un mapping del percorso alternativo, individuato tramite il metodo [**IVssWMFiledesc:: GetAlternateLocation**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation) , indica dove deve essere ripristinato un file. vedere uso di [percorsi alternativi durante il ripristino](working-with-alternate-locations-during-restore.md).

 

 



