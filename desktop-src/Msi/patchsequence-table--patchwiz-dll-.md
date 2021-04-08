---
description: La tabella PatchSequence viene utilizzata per generare la tabella MsiPatchSequence in una patch. La tabella richiede la versione di PATCHWIZ.DLL disponibile con Windows Installer&\# 160; 3.0.
ms.assetid: bdeccb3b-57c0-4424-9602-348b8048fd46
title: Tabella PatchSequence (PATCHWIZ.DLL)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 382e940d3c0cb6c7be2c8360ab98f2afaf13c799
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885490"
---
# <a name="patchsequence-table-patchwizdll"></a>Tabella PatchSequence (PATCHWIZ.DLL)

La tabella PatchSequence viene utilizzata per generare la [tabella MsiPatchSequence](msipatchsequence-table.md) in una patch. La tabella richiede la versione di [PATCHWIZ.DLL](patchwiz-dll.md) disponibile con Windows Installer 3,0.

Nella tabella seguente vengono identificate le colonne della tabella PatchSequence.



| Colonna      | Tipo       | Chiave | Nullable |
|-------------|------------|-----|----------|
| PatchFamily | Identificatore | S   | N        |
| Destinazione      | Testo       | S   | S        |
| Sequenza    | Versione    |     | S        |
| Sostituire   | Integer    |     | S        |



 

### <a name="columns"></a>Colonne

<dl> <dt>

<span id="PatchFamily"></span><span id="patchfamily"></span><span id="PATCHFAMILY"></span>PatchFamily
</dt> <dd>

Identificatore che indica le famiglie di sequenze a cui appartiene questa patch.

I valori nelle colonne target e PatchFamily definiscono la chiave primaria per la tabella. Una patch che appartiene a più famiglie di sequenze o ha sequenze diverse a seconda del codice prodotto della destinazione, può avere una riga per ogni associazione. Questo valore viene usato per popolare la colonna PatchFamily della [tabella MsiPatchSequence](msipatchsequence-table.md) che appartiene alla patch.

</dd> <dt>

<span id="Target"></span><span id="target"></span><span id="TARGET"></span>Destinazione
</dt> <dd>

La colonna di destinazione viene utilizzata per filtrare il PatchFamily in base al codice del prodotto.

Un valore NULL in questa colonna indica che questo PatchFamily si applica a tutte le destinazioni della patch. Se questa colonna contiene una chiave esterna per la [tabella TargetImages](targetimages-table-patchwiz-dll-.md), il codice prodotto dell'immagine specificata viene recuperato e utilizzato per popolare il valore del codice prodotto nella riga della nuova patch della [tabella MsiPatchSequence](msipatchsequence-table.md). Se questa colonna contiene un GUID, il GUID viene utilizzato per popolare il valore del codice prodotto della riga nella tabella MsiPatchSequence.

</dd> <dt>

<span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequenza
</dt> <dd>

Il valore nella colonna sequenza viene utilizzato per popolare la colonna sequenza della [tabella MsiPatchSequence](msipatchsequence-table.md) del nuovo file di patch.

Se il valore è NULL, viene generato automaticamente un numero di sequenza.

</dd> <dt>

<span id="Supersede"></span><span id="supersede"></span><span id="SUPERSEDE"></span>Sostituire
</dt> <dd>

Il valore **msidbPatchSequenceSupersedeEarlier** o 1 in questo campo indica che questa patch sostituisce [gli aggiornamenti più](small-updates.md) recenti nelle famiglie di sequenze a cui appartiene questa patch.

Il valore in questa colonna viene usato per impostare la colonna attributi della riga della nuova patch nella [tabella MsiPatchSequence](msipatchsequence-table.md) .

</dd> </dl>

### <a name="remarks"></a>Commenti

Disponibile a partire da Windows Installer 3,0.

 

 



