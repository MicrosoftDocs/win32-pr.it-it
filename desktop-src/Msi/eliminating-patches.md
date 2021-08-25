---
description: Una patch che non deve più essere usata può essere eliminata dalla sequenza di applicazione di patch.
ms.assetid: b1d499d9-4fd3-4996-84a1-c32acefbb98f
title: Eliminazione delle patch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f025c6487293d07df7963514b79f551045398f8d86f51dd7ab98b589a605e762
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119913521"
---
# <a name="eliminating-patches"></a>Eliminazione delle patch

Una patch che non deve più essere usata può essere eliminata dalla sequenza di applicazione di patch. In questo modo si impedisce l'applicazione della patch quando viene applicata una patch all'applicazione di destinazione. Questa operazione è diversa rispetto alla rimozione di una patch già applicata a un'applicazione. Per informazioni sulla rimozione delle patch applicate, vedere [Rimozione di patch.](removing-patches.md)

**Windows Installer 3.0 e versioni successive: **

Le patch con la [tabella MsiPatchSequence](msipatchsequence-table.md) possono usare questa tabella per eliminare le patch dalla sequenza di applicazione di patch. Una patch può eliminare le patch precedenti nella sequenza di applicazione di patch e sostituire le informazioni di tali patch con le proprie informazioni. Sia la patch che specifica quali patch eliminare che le patch eliminate devono avere una tabella MsiPatchSequence contenente informazioni.

Se le patch eliminate e le patch di sostituzione non hanno tabelle [MsiPatchSequence,](msipatchsequence-table.md) il pacchetto di patch può specificare un elenco di patch da eliminare dalla sequenza di applicazione di patch nella relativa proprietà [**Riepilogo**](revision-number-summary.md) numero revisione. Windows Il programma di installazione 3.0 ignora questo elenco se le patch eliminate o di sostituzione hanno una tabella MsiPatchSequence.

Quando il pacchetto patch contiene patch con informazioni sulla sequenza nella tabella [MsiPatchSequence](msipatchsequence-table.md) e alcune patch senza queste informazioni, il programma di installazione di Windows 3.0 sequenzia le patch nell'ordine descritto nella sezione seguente: [Sequenziazione](sequencing-patches.md)delle patch .

Ad esempio, Patch1, Patch2 e Patch3 possono essere tre patch che non hanno la tabella [MsiPatchSequence.](msipatchsequence-table.md) Patch2 può essere una patch applicabile solo se Patch1 è già stato applicato all'applicazione. Patch3 può essere una patch successiva che contiene tutte le informazioni in Patch1 ed elimina anche Patch1 dalla sequenza di applicazione di patch. Ciò significa che quando si applica Patch3, anche Patch 2 diventa inapplicabile, perché richiede Patch1. Tutte le informazioni solo in Patch2 non vengono recapitate all'applicazione.

**Windows Installer 2.0:** Non supportato. L'unico metodo disponibile è specificare l'elenco di patch da eliminare dalla sequenza di applicazione di patch nella [**proprietà Riepilogo numero revisione.**](revision-number-summary.md)

> [!Note]  
> Gli autori di patch devono usare le funzioni [**MsiDeterminePatchSequence**](/windows/desktop/api/Msi/nf-msi-msideterminepatchsequencea) e [**MsiDetermineApplicablePatches**](/windows/desktop/api/Msi/nf-msi-msidetermineapplicablepatchesa) per determinare la sequenza di patch effettivamente applicate al prodotto perché l'eliminazione di alcune patch può rendere inapplicabili altre patch.

 

 

 



