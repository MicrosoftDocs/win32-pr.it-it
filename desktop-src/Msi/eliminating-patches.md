---
description: Una patch che non dovrebbe più essere utilizzata può essere eliminata dalla sequenza di patch.
ms.assetid: b1d499d9-4fd3-4996-84a1-c32acefbb98f
title: Eliminazione di patch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a705ce5919ffd36e6fc860403e11db56c6df1592
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309490"
---
# <a name="eliminating-patches"></a>Eliminazione di patch

Una patch che non dovrebbe più essere utilizzata può essere eliminata dalla sequenza di patch. In questo modo si impedisce che la patch venga applicata quando l'applicazione di destinazione è stata patchata. Questa operazione è diversa rispetto alla rimozione di una patch già applicata a un'applicazione. Per informazioni sulla rimozione delle patch applicate, vedere [rimozione di patch](removing-patches.md).

* * Windows Installer 3,0 e versioni successive: * *

Le patch con la tabella [MsiPatchSequence](msipatchsequence-table.md) possono usare questa tabella per eliminare le patch dalla sequenza di patch. Una patch può eliminare le patch che lo precedono nella sequenza di patch e sostituire le informazioni da tali patch con le relative informazioni. Sia la patch che specifica le patch da eliminare che le patch eliminate devono avere una tabella MsiPatchSequence contenente le informazioni.

Se le patch eliminate e la patch di sostituzione non contengono tabelle [MsiPatchSequence](msipatchsequence-table.md) , il pacchetto di patch può specificare un elenco di patch da eliminare dalla sequenza di patch nella relativa proprietà di [**Riepilogo dei numeri di revisione**](revision-number-summary.md) . Windows Installer 3,0 ignora questo elenco se le patch eliminate o di sostituzione hanno una tabella MsiPatchSequence.

Quando il pacchetto di patch contiene patch con informazioni sulle sequenze nella tabella [MsiPatchSequence](msipatchsequence-table.md) e alcune patch senza queste informazioni, Windows Installer 3,0 Sequenzia le patch nell'ordine descritto nella sezione seguente: [sequenziazione delle patch](sequencing-patches.md).

Ad esempio, patch1, Patch2 e Patch3 possono essere tre patch che non dispongono della tabella [MsiPatchSequence](msipatchsequence-table.md) . Patch2 può essere una patch applicabile solo se patch1 è già stato applicato all'applicazione. Patch3 può essere una patch successiva con tutte le informazioni contenute in patch1 ed Elimina patch1 dalla sequenza di patch. Ciò significa che quando viene applicato Patch3, patch 2 diventa anche inapplicabile, perché richiede patch1. Tutte le informazioni solo in Patch2 non vengono recapitate all'applicazione.

**Windows Installer 2,0:** Non supportato. L'unico metodo disponibile consiste nel specificare l'elenco di patch da eliminare dalla sequenza di patch nella proprietà di [**Riepilogo dei numeri di revisione**](revision-number-summary.md) .

> [!Note]  
> Gli autori delle patch devono usare le funzioni [**MsiDeterminePatchSequence**](/windows/desktop/api/Msi/nf-msi-msideterminepatchsequencea) e [**MsiDetermineApplicablePatches**](/windows/desktop/api/Msi/nf-msi-msidetermineapplicablepatchesa) per determinare la sequenza di patch che vengono effettivamente applicate al prodotto perché l'eliminazione di alcune patch può rendere inapplicabili altre patch.

 

 

 



