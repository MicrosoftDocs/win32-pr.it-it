---
description: A partire da Windows Installer 3.0, è possibile applicare più patch a un prodotto in un ordine costante, indipendentemente dall'ordine in cui le patch vengono fornite al sistema.
ms.assetid: 10af1857-d59f-490d-9b50-49619b1e892c
title: Installazione di più patch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65dc6b65997bd6bcb2b9f4c8da5022adda9a38b0b93401dc507397421799d260
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119893851"
---
# <a name="installing-multiple-patches"></a>Installazione di più patch

A partire da Windows Installer 3.0, è possibile applicare più patch a un prodotto in un ordine costante, indipendentemente dall'ordine in cui le patch vengono fornite al sistema.

**Windows Installer 2.0:** Non supportato. Windows Le versioni del programma di installazione precedenti alla versione 3.0 installano sempre le patch nell'ordine in cui vengono fornite al sistema.

**Windows Installer 3.0 e versioni successive:** Il programma di installazione può usare le informazioni fornite nella tabella [MsiPatchSequence](msipatchsequence-table.md) per determinare quali patch sono applicabili al pacchetto del programma di installazione di Windows e in quale ordine devono essere applicate. Le applicazioni possono usare [**le funzioni MsiDetermineApplicablePatches**](/windows/desktop/api/Msi/nf-msi-msidetermineapplicablepatchesa) [**e MsiDeterminePatchSequence.**](/windows/desktop/api/Msi/nf-msi-msideterminepatchsequencea)

La [**funzione MsiDetermineApplicablePatches**](/windows/desktop/api/Msi/nf-msi-msidetermineapplicablepatchesa) determina quali patch si applicano al pacchetto Windows Installer e in quale sequenza. La funzione può essere utilizzata per le patch sostituite o obsolete. Questa funzione non viene utilizzata per i prodotti o le patch installate nel sistema che non sono specificati nel set.

La [**funzione Della sequenza MsiDeterminePatchSequence**](/windows/desktop/api/Msi/nf-msi-msideterminepatchsequencea) può determinare la sequenza di applicazione migliore per le patch per un prodotto installato specificato. Questa funzione rappresenta le patch già applicate al prodotto e le patch obsolete e sostituite.

Quando il pacchetto di patch non ha una tabella [MsiPatchSequence,](msipatchsequence-table.md) il programma di installazione applica sempre le patch nell'ordine in cui vengono fornite al sistema.

Quando il pacchetto di patch contiene una combinazione di patch con informazioni sulla sequenza nella tabella [MsiPatchSequence](msipatchsequence-table.md) e alcune patch senza queste informazioni, il programma di installazione di Windows versione 3.0 sequenzia le patch nell'ordine descritto nella sezione seguente: [Sequenziazione](sequencing-patches.md)delle patch .

Un pacchetto Windows Installer può installare non più di 127 patch durante l'installazione o l'aggiornamento di un'applicazione. Quando sono necessari molti aggiornamenti, devono essere combinati e le patch obsolete precedenti devono essere eliminate dalla sequenza di applicazione delle patch.

Una patch che non deve essere usata può essere eliminata dalla sequenza di applicazione di patch. In questo modo si impedisce l'applicazione della patch quando viene applicata una patch all'applicazione di destinazione. Questa operazione è diversa rispetto alla rimozione di una patch che è già stata applicata a un'applicazione. Per altre informazioni sull'eliminazione delle patch dalla sequenza di applicazione di patch, vedere [Eliminazione di patch.](eliminating-patches.md) Per informazioni sulla rimozione delle patch applicate, vedere [Rimozione di patch.](removing-patches.md)

Per un esempio di come Windows installer applica più patch quando tutte hanno tabelle [MsiPatchSequence,](msipatchsequence-table.md) vedere Multiple Patching Example (Esempio di applicazione [di più patch).](multiple-patching-example.md)

 

 



