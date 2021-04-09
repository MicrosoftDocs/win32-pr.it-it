---
description: La tabella FamilyFileRanges contiene informazioni su file specifici di un'immagine aggiornata con intervalli che non devono mai essere sovrascritti.
ms.assetid: 2e77605a-d909-4a17-977c-18281a96c36c
title: Tabella FamilyFileRanges (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2940d45d82efae3e61842ee0f6b4e46e3f77ef3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130678"
---
# <a name="familyfileranges-table-patchwizdll"></a>Tabella FamilyFileRanges (Patchwiz.dll)

La tabella FamilyFileRanges contiene informazioni su file specifici di un'immagine aggiornata con intervalli che non devono mai essere sovrascritti. Questa tabella è facoltativa nel database di creazione della patch (file con estensione PCP) e viene usata dalla funzione [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) .

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

Chiave esterna per la colonna Family della [tabella ImageFamilies (Patchwiz.dll)](imagefamilies-table-patchwiz-dll-.md).

</dd> <dt>

<span id="FTK"></span><span id="ftk"></span>FTK
</dt> <dd>

Chiave esterna nelle [tabelle di file](file-table.md) di tutte le immagini aggiornate nella famiglia di immagini.

</dd> <dt>

<span id="RetainOffsets"></span><span id="retainoffsets"></span><span id="RETAINOFFSETS"></span>RetainOffsets
</dt> <dd>

Offset degli intervalli che non possono essere sovrascritti. Il valore in questo campo è un elenco dei numeri di offset dell'intervallo per gli intervalli che non devono essere sovrascritti nei file di destinazione. L'ordine e il numero degli intervalli nell'elenco devono corrispondere agli elementi della colonna RetainLengths.

I valori possono essere decimali o esadecimali. [Patchwiz.dll](patchwiz-dll.md) considera il valore come esadecimale se è preceduto da "0x". Le colonne sono colonne stringa e Patchwiz.dll convertiranno i valori in ULONG.

</dd> <dt>

<span id="RetainLengths"></span><span id="retainlengths"></span><span id="RETAINLENGTHS"></span>RetainLengths
</dt> <dd>

Lunghezza in byte degli intervalli che non possono essere sovrascritti. Il valore in questo campo è un elenco di numeri di lunghezza intervallo per gli intervalli da mantenere nei file di destinazione. L'ordine e il numero degli intervalli nell'elenco devono corrispondere agli elementi della colonna RetainOffsets.

I valori possono essere decimali o esadecimali. [Patchwiz.dll](patchwiz-dll.md) considera il valore come esadecimale se è preceduto da "0x". Le colonne sono colonne stringa e Patchwiz.dll convertiranno i valori in ULONG.

</dd> </dl>

## <a name="remarks"></a>Commenti

Gli offset e le lunghezze immesse in RetainOffsets e RetainLengths non devono specificare intervalli sovrapposti.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Applicazione di patch alle aree selezionate di un file](patching-selected-regions-of-a-file.md)
</dt> </dl>

 

 



