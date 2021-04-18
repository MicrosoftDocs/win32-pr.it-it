---
description: Nell'esempio seguente viene illustrato come è possibile utilizzare Windows Installer 3,0 e versioni successive per applicare le patch nell'ordine in cui vengono create.
ms.assetid: 98771652-cec2-4371-8132-a741cf8431fb
title: Esempio di applicazione di patch multipla
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2d10274531ac4906ef61a49caee9ccbcde98bbb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310516"
---
# <a name="multiple-patching-example"></a>Esempio di applicazione di patch multipla

Nell'esempio seguente viene illustrato come è possibile utilizzare Windows Installer 3,0 e versioni successive per applicare le patch nell'ordine in cui vengono create.

## <a name="example"></a>Esempio

In questo esempio sono presenti tre patch, QFE1, QFE2 e ServicePack1, ognuno con una tabella [MsiPatchSequence](msipatchsequence-table.md) . Queste patch sono state create per essere applicate alla versione 1,0 dell'applicazione.



| Nome patch   | Tipo di patch    | Numero sequenza |
|--------------|---------------|-----------------|
| QFE1         | Aggiornamento ridotto  | 1.1.0           |
| QFE2         | Aggiornamento ridotto  | 1.2.0           |
| ServicePack1 | Aggiornamento secondario | 1.3.0           |



 

La tabella [MsiPatchSequence](msipatchsequence-table.md) di ogni patch ha un solo record che contiene la famiglia di patch, il codice prodotto e il numero di sequenza. Le tre patch sono tutte applicate allo stesso prodotto e appartengono alla stessa famiglia di patch, denominata AppPatch. Nessuna delle patch ha l'attributo **msidbPatchSequenceSupersedeEarlier** .

[Tabella MsiPatchSequence](msipatchsequence-table.md) per l'aggiornamento di QFE1 [small](small-updates.md). 

| PatchFamily | ProductCode                            | Sequenza | Attributi |
|-------------|----------------------------------------|----------|------------|
| AppPatch    | {18A9233C-0B34-4127-A966-C257386270BC} | 1.1.0    |            |



 

[Tabella MsiPatchSequence](msipatchsequence-table.md) per l'aggiornamento di QFE2 [small](small-updates.md). 

| PatchFamily | ProductCode                            | Sequenza | Attributi |
|-------------|----------------------------------------|----------|------------|
| AppPatch    | {18A9233C-0B34-4127-A966-C257386270BC} | 1.2.0    |            |



 

[Tabella MsiPatchSequence](msipatchsequence-table.md) per l' [aggiornamento](minor-upgrades.md)di Servicepack1 minor. 

| PatchFamily | ProductCode                            | Sequenza | Attributi |
|-------------|----------------------------------------|----------|------------|
| AppPatch    | {18A9233C-0B34-4127-A966-C257386270BC} | 1.3.0    |            |



 

Se un utente installa la versione 1,0 del prodotto e quindi applica QFE2, quindi in un secondo momento decide di applicare QFE1, Windows Installer garantisce che la sequenza effettiva di applicazione patch al prodotto sia QFE1 applicata prima di QFE2. Se l'utente applica ServicePack1, applica QFE2 e QFE1 insieme in un secondo momento, Windows Installer garantisce che la sequenza effettiva di applicazione patch al prodotto sia QFE1 avanti rispetto a QFE2 e Ahead ServicePack1.

Se ServicePack1 ha **msidbPatchSequenceSupersedeEarlier** impostato nella colonna Attributes della relativa tabella [MsiPatchSequence](msipatchsequence-table.md) , significa che il Service Pack contiene tutte le modifiche apportate a QFE1 e QFE2. In questo caso, QFE1 e QFE2 non vengono applicati quando viene applicato ServicePack1.

**Windows Installer 2,0:** Non supportato. Le versioni precedenti a Windows Installer 3,0 possono installare solo una patch per ogni transazione e le patch vengono applicate nella sequenza specificata. Per l'esempio precedente, se QFE2 viene applicato per primo e viene applicato QFE1, ovvero due transazioni, le patch vengono applicate alla versione 1,0 dell'applicazione nella sequenza QFE2 seguita da QFE1. Se ServicePack1 viene applicato per primo, non è possibile applicare QFE1 o QFE2 in una transazione successiva, perché ServicePack1 è un aggiornamento secondario che modifica la versione dell'applicazione. QFE1 e QFE2 possono essere applicati solo alla versione 1,0 dell'applicazione.

 

 



