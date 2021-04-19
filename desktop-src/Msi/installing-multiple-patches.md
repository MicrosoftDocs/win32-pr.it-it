---
description: A partire da Windows Installer 3,0, è possibile applicare più patch a un prodotto in un ordine costante, indipendentemente dall'ordine con cui le patch vengono fornite al sistema.
ms.assetid: 10af1857-d59f-490d-9b50-49619b1e892c
title: Installazione di più patch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d4edb8d085ede6aee81690bf67bd9c5e19780ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308896"
---
# <a name="installing-multiple-patches"></a>Installazione di più patch

A partire da Windows Installer 3,0, è possibile applicare più patch a un prodotto in un ordine costante, indipendentemente dall'ordine con cui le patch vengono fornite al sistema.

**Windows Installer 2,0:** Non supportato. Windows Installer versioni precedenti alla versione 3,0 installano sempre le patch nell'ordine in cui vengono fornite al sistema.

**Windows Installer 3,0 e versioni successive:** Il programma di installazione può utilizzare le informazioni fornite nella tabella [MsiPatchSequence](msipatchsequence-table.md) per determinare quali patch sono applicabili al pacchetto Windows Installer e in quale ordine applicare le patch. Le applicazioni possono utilizzare le funzioni [**MsiDetermineApplicablePatches**](/windows/desktop/api/Msi/nf-msi-msidetermineapplicablepatchesa) e [**MsiDeterminePatchSequence**](/windows/desktop/api/Msi/nf-msi-msideterminepatchsequencea) .

La funzione [**MsiDetermineApplicablePatches**](/windows/desktop/api/Msi/nf-msi-msidetermineapplicablepatchesa) determina quali patch si applicano al pacchetto di Windows Installer e alla sequenza. La funzione può tenere conto delle patch sostituite o obsolete. Questa funzione non tiene conto dei prodotti o delle patch installate nel sistema che non sono specificate nel set.

La funzione Sequence [**MsiDeterminePatchSequence**](/windows/desktop/api/Msi/nf-msi-msideterminepatchsequencea) è in grado di determinare la migliore sequenza di applicazione per le patch in un prodotto installato specificato. Questa funzione rappresenta le patch che sono già state applicate al prodotto e gli account per le patch obsolete e sostituite.

Quando il pacchetto di patch non dispone di una tabella [MsiPatchSequence](msipatchsequence-table.md) , il programma di installazione applica sempre le patch nell'ordine in cui sono fornite al sistema.

Quando il pacchetto di patch contiene una combinazione di patch con informazioni sulle sequenze nella tabella [MsiPatchSequence](msipatchsequence-table.md) e alcune patch senza queste informazioni, Windows installer versione 3,0 Sequenzia le patch nell'ordine descritto nella sezione seguente: [sequenziazione delle patch](sequencing-patches.md).

Un pacchetto di Windows Installer può installare non più di 127 patch durante l'installazione o l'aggiornamento di un'applicazione. Quando sono necessari molti aggiornamenti, è necessario combinarli e le patch obsolete precedenti devono essere eliminate dalla sequenza di patch.

Una patch che non deve essere usata può essere eliminata dalla sequenza di patch. In questo modo si impedisce che la patch venga applicata quando l'applicazione di destinazione è stata patchata. Questa operazione è diversa rispetto alla rimozione di una patch che è già stata applicata a un'applicazione. Per ulteriori informazioni sull'eliminazione delle patch dalla sequenza di patch, vedere [eliminazione di patch](eliminating-patches.md). Per informazioni sulla rimozione delle patch applicate, vedere [rimozione di patch](removing-patches.md).

Per un esempio di come Windows Installer applica più patch quando tutti hanno tabelle [MsiPatchSequence](msipatchsequence-table.md) , vedere l' [esempio relativo a più patch](multiple-patching-example.md).

 

 



