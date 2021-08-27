---
description: La tabella PatchSequence viene usata per generare la tabella MsiPatchSequence in una patch. La tabella richiede la versione di PATCHWIZ.DLL disponibile con Windows Installer&\# 160;3.0.
ms.assetid: bdeccb3b-57c0-4424-9602-348b8048fd46
title: Tabella PatchSequence (PATCHWIZ.DLL)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0281f9882a674b268466259c534eefaa468bacf0fa891dc3a385e4d580a1e8a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129181"
---
# <a name="patchsequence-table-patchwizdll"></a>Tabella PatchSequence (PATCHWIZ.DLL)

La tabella PatchSequence viene usata per generare la [tabella MsiPatchSequence](msipatchsequence-table.md) in una patch. La tabella richiede la versione [diPATCHWIZ.DLL](patchwiz-dll.md) disponibile con Windows Installer 3.0.

La tabella seguente identifica le colonne della tabella PatchSequence.



| Colonna      | Tipo       | Chiave | Nullable |
|-------------|------------|-----|----------|
| PatchFamily | Identificatore | S   | N        |
| Destinazione      | Testo       | S   | S        |
| Sequenza    | Versione    |     | S        |
| Sostituiscono   | Intero    |     | S        |



 

### <a name="columns"></a>Colonne

<dl> <dt>

<span id="PatchFamily"></span><span id="patchfamily"></span><span id="PATCHFAMILY"></span>PatchFamily
</dt> <dd>

Identificatore che indica le famiglie di sequenze a cui appartiene questa patch.

I valori nelle colonne Target e PatchFamily definiscono insieme la chiave primaria per la tabella. Una patch appartenente a più famiglie di sequenze o con sequenze diverse a seconda del codice prodotto della destinazione può avere una riga per ogni associazione. Questo valore viene usato per popolare la colonna PatchFamily della tabella [MsiPatchSequence](msipatchsequence-table.md) che appartiene alla patch.

</dd> <dt>

<span id="Target"></span><span id="target"></span><span id="TARGET"></span>bersaglio
</dt> <dd>

La colonna Target viene usata per filtrare PatchFamily in base al codice prodotto.

Un valore NULL in questa colonna indica che patchFamily si applica a tutte le destinazioni della patch. Se questa colonna contiene una chiave esterna per la tabella [TargetImages](targetimages-table-patchwiz-dll-.md), il codice prodotto dell'immagine specificata viene recuperato e usato per popolare il valore del codice prodotto nella riga della nuova patch della tabella [MsiPatchSequence](msipatchsequence-table.md). Se questa colonna contiene un GUID, il GUID viene usato per popolare il valore del codice prodotto della riga nella tabella MsiPatchSequence.

</dd> <dt>

<span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequenza
</dt> <dd>

Il valore nella colonna Sequenza viene usato per popolare la colonna Sequenza della tabella [MsiPatchSequence](msipatchsequence-table.md) del nuovo file di patch.

Se il valore è NULL, viene generato automaticamente un numero di sequenza.

</dd> <dt>

<span id="Supersede"></span><span id="supersede"></span><span id="SUPERSEDE"></span>Sostituiscono
</dt> <dd>

Il valore **msidbPatchSequenceSupersedeEarlier** o 1 in questo campo indica che [](small-updates.md) questa patch sostituisce gli aggiornamenti di piccole dimensioni precedenti nelle famiglie di sequenze a cui appartiene questa patch.

Il valore in questa colonna viene usato per impostare la colonna Attributes della nuova riga della patch nella [tabella MsiPatchSequence](msipatchsequence-table.md) .

</dd> </dl>

### <a name="remarks"></a>Commenti

Disponibile a partire da Windows Installer 3.0.

 

 



