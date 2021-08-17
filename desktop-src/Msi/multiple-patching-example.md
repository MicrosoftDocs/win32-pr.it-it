---
description: L'esempio seguente illustra come Windows Installer 3.0 e versioni successive per applicare le patch nell'ordine in cui vengono scritte.
ms.assetid: 98771652-cec2-4371-8132-a741cf8431fb
title: Esempio di applicazione di più patch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b8d33d103bb27fde3b7fdc4ee46a0c5d946e73b6948513ea1b8fffb7bab30bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118943368"
---
# <a name="multiple-patching-example"></a>Esempio di applicazione di più patch

L'esempio seguente illustra come Windows Installer 3.0 e versioni successive per applicare le patch nell'ordine in cui vengono scritte.

## <a name="example"></a>Esempio

In questo esempio sono presenti tre patch, QFE1, QFE2 e ServicePack1, ognuna con una tabella [MsiPatchSequence.](msipatchsequence-table.md) Queste patch sono state scritte per essere applicate alla versione 1.0 dell'applicazione.



| Nome patch   | Tipo di patch    | Numero sequenza |
|--------------|---------------|-----------------|
| QFE1         | Aggiornamento di piccole dimensioni  | 1.1.0           |
| QFE2         | Aggiornamento di piccole dimensioni  | 1.2.0           |
| ServicePack1 | Aggiornamento secondario | 1.3.0           |



 

La [tabella MsiPatchSequence](msipatchsequence-table.md) di ogni patch contiene un solo record che contiene la famiglia di patch, il codice prodotto e il numero di sequenza. Le tre patch vengono tutte applicate allo stesso prodotto e appartengono alla stessa famiglia di patch, denominata AppPatch. Nessuna delle patch ha **l'attributo msidbPatchSequenceSupersedeEarlier.**

[Tabella MsiPatchSequence per](msipatchsequence-table.md) l'aggiornamento QFE1 [di piccole dimensioni](small-updates.md). 

| PatchFamily | ProductCode                            | Sequenza | Attributi |
|-------------|----------------------------------------|----------|------------|
| AppPatch    | {18A9233C-0B34-4127-A966-C257386270BC} | 1.1.0    |            |



 

[Tabella MsiPatchSequence per](msipatchsequence-table.md) l'aggiornamento di piccole [dimensioni](small-updates.md)QFE2 . 

| PatchFamily | ProductCode                            | Sequenza | Attributi |
|-------------|----------------------------------------|----------|------------|
| AppPatch    | {18A9233C-0B34-4127-A966-C257386270BC} | 1.2.0    |            |



 

[Tabella MsiPatchSequence per l'aggiornamento](msipatchsequence-table.md) secondario di ServicePack1 [](minor-upgrades.md). 

| PatchFamily | ProductCode                            | Sequenza | Attributi |
|-------------|----------------------------------------|----------|------------|
| AppPatch    | {18A9233C-0B34-4127-A966-C257386270BC} | 1.3.0    |            |



 

Se un utente installa la versione 1.0 del prodotto e quindi applica QFE2 e successivamente decide di applicare QFE1, il programma di installazione di Windows garantisce che la sequenza effettiva dell'applicazione patch al prodotto sia QFE1 applicata prima di QFE2. Se l'utente applica ServicePack1, quindi applica QFE2 e QFE1 in un secondo momento, il programma di installazione di Windows garantisce che la sequenza effettiva dell'applicazione patch al prodotto sia QFE1 prima di QFE2 e prima di ServicePack1.

Se servicePack1 ha **msidbPatchSequenceSupersedeEarlier** impostato nella colonna Attributi della relativa tabella [MsiPatchSequence,](msipatchsequence-table.md) significa che il Service Pack contiene tutte le modifiche in QFE1 e QFE2. In questo caso, QFE1 e QFE2 non vengono applicati quando viene applicato ServicePack1.

**Windows Installer 2.0:** Non supportato. Le versioni precedenti Windows Installer 3.0 possono installare una sola patch per transazione e le patch vengono applicate nella sequenza in cui vengono fornite. Per l'esempio precedente, se QFE2 viene applicato per primo e quindi QFE1, si tratta di due transazioni e le patch vengono applicate alla versione 1.0 dell'applicazione nella sequenza QFE2 seguita da QFE1. Se ServicePack1 viene applicato per primo, non è possibile applicare QFE1 o QFE2 in una transazione successiva perché ServicePack1 è un aggiornamento secondario che modifica la versione dell'applicazione. QFE1 e QFE2 possono essere applicati solo alla versione 1.0 dell'applicazione.

 

 



