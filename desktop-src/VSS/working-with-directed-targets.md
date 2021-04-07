---
description: Il meccanismo di destinazione diretto consente ai writer di rimappare i file in fase di ripristino.
ms.assetid: c0b4ab26-2bb6-4b0f-b837-01057983b49b
title: Utilizzo di destinazioni dirette
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bd2e15ec873b87030a2d01be69d2c3e5f95a193
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049500"
---
# <a name="working-with-directed-targets"></a>Utilizzo di destinazioni dirette

Il meccanismo di [*destinazione diretto*](vssgloss-d.md) consente ai writer di rimappare i file in fase di ripristino. Questo consente ai writer di eseguire le operazioni seguenti:

-   Specificare i nuovi percorsi di destinazione (analogamente a un richiedente [**IVssBackupComponents:: AddNewTarget**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addnewtarget)).
-   Recuperare spazio su disco ripristinando solo le parti necessarie di un file su disco, in particolare quando è stato eseguito il backup di un file utilizzando il meccanismo di [*file parziale*](vssgloss-p.md) .
-   Modificare il formato del file in modo che soddisfi le esigenze correnti.

Qualsiasi file da usare con un'operazione di destinazione diretta deve avere una [*destinazione di ripristino*](vssgloss-r.md) di VSS \_ RT \_ diretta.

Una volta stabilito che un richiedente può supportare un'operazione di destinazione diretta, un writer (durante la gestione dell'evento di [**preripristino**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) ) utilizza [**IVssComponent:: AddDirectedTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddirectedtarget) per l'istanza di [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) corrispondente al componente che gestisce il file (o il componente che definisce il set di componenti che contiene il file) per definire la modalità di modifica del mapping del file durante il ripristino.

Quando si usa [**IVssComponent:: AddDirectedTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddirectedtarget), i writer specificano il nome e il percorso del file usati per eseguire il backup del file, il nome del file e il percorso della destinazione di ripristino (questi valori possono corrispondere al nome e al percorso del file originale) e agli intervalli di file di origine e di destinazione.

Come per le operazioni di file parziali, gli elenchi di intervalli sono coppie di offset nel file di cui eseguire il backup (in byte) e la lunghezza della sezione da ripristinare (in byte), offset e lunghezza separati da due punti e ogni coppia è separata da una virgola: *Offset1 ***:**_length1_*_,_* * Offset2 ***:**_length2_. Ogni valore è un Integer a 64 bit in formato esadecimale o decimale.

Se un writer deve usare il meccanismo di destinazione diretto per fare in modo che il richiedente ripristini un file in un nuovo percorso, avrebbe chiamato [**IVssComponent:: AddDirectedTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddirectedtarget) con il nome e il percorso del file originale e il nome e il percorso del nuovo file e specificare gli intervalli di destinazione di origine con un offset zero e una lunghezza uguale a quella dell'intera dimensione del file.

Se ad esempio un writer deve avere un file da 200 mila, C: \\ WriterData \\ index. dat, ripristinato come c: \\ WriterData \\ OldIndex. dat, la stringa dell'intervallo di origine e di destinazione sarà "**0:204880**".

Per modificare il mapping di un file di backup di grandi dimensioni parzialmente, il richiedente utilizzerebbe l'intervallo di origine utilizzato per eseguire il backup del file e un intervallo di destinazione che ridurrà le dimensioni del file. È possibile ottenere le informazioni sull'intervallo di origine utilizzando [**IVssComponent:: GetPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfile) per l'istanza di [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) corrispondente al componente che gestisce il file (o il componente che definisce il set di componenti che contiene il file).

Se il file parzialmente sottoposto a backup era inizialmente un file di grandi dimensioni la cui intestazione, byte 64-512, contiene un numero di record e altre informazioni aggiornate di frequente e i cui dati più recenti si trovano negli ultimi 65536 byte del file, ovvero i byte da 0x1239E8577A a 0x1239E7577A, un writer potrebbe specificare un elenco di intervalli di origine come stringa "**64:448, 0x1239E8577A: 65536**".

Se il writer vuole modificare il mapping del file ripristinato in modo che contenga solo l'intestazione e i dati più recenti, l'elenco di intervalli potrebbe essere la stringa "**0:488488:65536**".

Prima di eseguire effettivamente un'operazione di ripristino, un richiedente deve verificare se i file richiedono il supporto diretto della destinazione.

A tale scopo, il richiedente scorre prima i writer con i componenti archiviati nel documento relativo ai componenti di backup usando [**IVssBackupComponents:: GetWriterComponentsCount**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponentscount) e [**IVssBackupComponents:: GetWriterComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponents).

L'interfaccia [**IVssBackupComponents:: GetWriterComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponents) viene quindi utilizzata per restituire le istanze dell'interfaccia [**IVssWriterComponentsExt**](/windows/win32/api/vsbackup/nl-vsbackup-ivsswritercomponentsext) che fornisce i metodi [**IVssWriterComponentsExt:: getComponent**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswritercomponents-getcomponent) e [**IVssWriterComponentsExt:: GetComponentCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswritercomponents-getcomponentcount) che consentono al richiedente di ottenere istanze di [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) .

Questo consente a un richiedente di ottenere i candidati indirizzati di destinazione usando [**IVssComponent:: GetDirectedTargetCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdirectedtargetcount) e [**IVssComponent:: GetDirectedTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdirectedtarget) per l'istanza di [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) corrispondente al componente che gestisce il file (o il componente che definisce il set di componenti che contiene il file).

 

 
