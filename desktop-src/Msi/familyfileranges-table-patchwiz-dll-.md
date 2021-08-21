---
description: La tabella FamilyFileRanges contiene informazioni su file specifici di un'immagine aggiornata con intervalli che non devono mai essere sovrascritti.
ms.assetid: 2e77605a-d909-4a17-977c-18281a96c36c
title: Tabella FamilyFileRanges (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b0559f4cea1061f9cf0c1438140e7abba8b00908233a1a1d608ae5dbd8b79ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118636898"
---
# <a name="familyfileranges-table-patchwizdll"></a>Tabella FamilyFileRanges (Patchwiz.dll)

La tabella FamilyFileRanges contiene informazioni su file specifici di un'immagine aggiornata con intervalli che non devono mai essere sovrascritti. Questa tabella è facoltativa nel database di creazione delle patch (file con estensione pcp) e viene usata dalla [funzione UiCreatePatchPackageEx.](uicreatepatchpackageex--patchwiz-dll-.md)

La tabella FamilyFileRanges include le colonne seguenti.



| Colonna        | Tipo | Chiave | Nullable |
|---------------|------|-----|----------|
| Famiglia        | text | S   | N        |
| FTK           | text | S   | N        |
| RetainOffsets | text |     | N        |
| RetainLengths | text |     | N        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="Family"></span><span id="family"></span><span id="FAMILY"></span>Famiglia
</dt> <dd>

Chiave esterna per la colonna Family della [tabella ImageFamilies (Patchwiz.dll).](imagefamilies-table-patchwiz-dll-.md)

</dd> <dt>

<span id="FTK"></span><span id="ftk"></span>FTK
</dt> <dd>

Chiave esterna nelle [tabelle File di](file-table.md) tutte le immagini aggiornate nella famiglia di immagini.

</dd> <dt>

<span id="RetainOffsets"></span><span id="retainoffsets"></span><span id="RETAINOFFSETS"></span>RetainOffsets
</dt> <dd>

Offset degli intervalli che non possono essere sovrascritti. Il valore in questo campo è un elenco dei numeri di offset dell'intervallo per gli intervalli che non devono essere sovrascritti nei file di destinazione. L'ordine e il numero degli intervalli nell'elenco devono corrispondere agli elementi nella colonna RetainLengths.

I valori possono essere decimali o esadecimali. [Patchwiz.dll](patchwiz-dll.md) considera il valore come esadecimale se è preceduto da "0x". Le colonne sono colonne stringa e Patchwiz.dll convertiranno i valori in ULONG.

</dd> <dt>

<span id="RetainLengths"></span><span id="retainlengths"></span><span id="RETAINLENGTHS"></span>RetainLengths
</dt> <dd>

Lunghezza in byte degli intervalli che non può essere sovrascritta. Il valore in questo campo è un elenco di numeri di lunghezza di intervallo per gli intervalli da conservare nei file di destinazione. L'ordine e il numero degli intervalli nell'elenco devono corrispondere agli elementi nella colonna RetainOffsets.

I valori possono essere decimali o esadecimali. [Patchwiz.dll](patchwiz-dll.md) considera il valore come esadecimale se è preceduto da "0x". Le colonne sono colonne stringa e Patchwiz.dll convertiranno i valori in ULONG.

</dd> </dl>

## <a name="remarks"></a>Commenti

Gli offset e le lunghezze immessi in RetainOffsets e RetainLengths non devono specificare intervalli sovrapposti.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Applicazione di patch alle aree selezionate di un file](patching-selected-regions-of-a-file.md)
</dt> </dl>

 

 



