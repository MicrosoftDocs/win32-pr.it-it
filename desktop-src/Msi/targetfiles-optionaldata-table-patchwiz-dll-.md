---
description: La tabella TargetFiles \_ OptionalData contiene informazioni su file specifici in un'immagine di destinazione. Questa tabella è facoltativa nel database di creazione delle patch (file con estensione pcp) e viene usata dalla funzione UiCreatePatchPackageEx.
ms.assetid: 577b1674-1e44-42e1-b011-c0fb561b514c
title: TargetFiles_OptionalData tabella (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5664e2e21968cb3fee5ce3d606dd07008f2436c4b649a7bcefeebd77df9cf6f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118623736"
---
# <a name="targetfiles_optionaldata-table-patchwizdll"></a>Tabella \_ OptionalData TargetFiles (Patchwiz.dll)

La tabella TargetFiles \_ OptionalData contiene informazioni su file specifici in un'immagine di destinazione. Questa tabella è facoltativa nel database di creazione delle patch (file con estensione pcp) e viene usata dalla [funzione UiCreatePatchPackageEx.](uicreatepatchpackageex--patchwiz-dll-.md)

La tabella TargetFiles \_ OptionalData contiene le colonne seguenti.



| Colonna        | Tipo | Chiave | Nullable |
|---------------|------|-----|----------|
| Destinazione        | text | S   | N        |
| FTK           | text | S   | N        |
| Percorsi dei simboli   | text |     | S        |
| IgnoreOffsets | text |     | S        |
| IgnoreLengths | text |     | S        |
| RetainOffsets | text |     | S        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="Target"></span><span id="target"></span><span id="TARGET"></span>bersaglio
</dt> <dd>

Chiave esterna per la colonna Target della [tabella TargetImages (Patchwiz.dll).](targetimages-table-patchwiz-dll-.md)

</dd> <dt>

<span id="FTK"></span><span id="ftk"></span>FTK
</dt> <dd>

Chiave esterna nella tabella [File dell'immagine](file-table.md) di destinazione.

</dd> <dt>

<span id="SymbolPaths"></span><span id="symbolpaths"></span><span id="SYMBOLPATHS"></span>Percorsi dei simboli
</dt> <dd>

Il valore in questo campo viene aggiunto all'elenco delimitato da punto e virgola delle cartelle nella colonna SymbolPaths della tabella [TargetImages (Patchwiz.dll)](targetimages-table-patchwiz-dll-.md) quando viene generata la patch e può essere usato per aggiungere file di simboli per un file specifico.

</dd> <dt>

<span id="IgnoreOffsets"></span><span id="ignoreoffsets"></span><span id="IGNOREOFFSETS"></span>IgnoreOffsets
</dt> <dd>

Il valore in questo campo è un elenco delimitato da virgole di numeri di offset di intervallo per gli intervalli da ignorare nel file di destinazione. L'ordine e il numero degli intervalli nell'elenco devono corrispondere agli elementi nella colonna IgnoreLengths. Questa colonna è facoltativa.

I valori possono essere decimali o esadecimali. [Patchwiz.dll](patchwiz-dll.md) considera il valore come esadecimale se è preceduto da "0x". Le colonne sono colonne stringa e Patchwiz.dll convertiranno i valori in ULONG.

</dd> <dt>

<span id="IgnoreLengths"></span><span id="ignorelengths"></span><span id="IGNORELENGTHS"></span>IgnoreLengths
</dt> <dd>

Il valore in questo campo è un elenco delimitato da virgole di lunghezze di intervallo in byte per gli intervalli da ignorare nel file di destinazione. L'ordine e il numero degli intervalli nell'elenco devono corrispondere agli elementi nella colonna IgnoreOffsets. Questa colonna è facoltativa.

I valori possono essere decimali o esadecimali. [Patchwiz.dll](patchwiz-dll.md) considera il valore come esadecimale se è preceduto da "0x". Le colonne sono colonne stringa e Patchwiz.dll convertiranno i valori in ULONG.

</dd> <dt>

<span id="RetainOffsets"></span><span id="retainoffsets"></span><span id="RETAINOFFSETS"></span>RetainOffsets
</dt> <dd>

Il valore in questo campo è un elenco delimitato da virgole di numeri di offset di intervallo per gli intervalli da mantenere nel file di destinazione. L'ordine e il numero degli intervalli nell'elenco devono corrispondere agli elementi nella colonna RetainOffsets del record corrispondente nella tabella [FamilyFileRanges (Patchwiz.dll)](familyfileranges-table-patchwiz-dll-.md)

I valori possono essere decimali o esadecimali. [Patchwiz.dll](patchwiz-dll.md) considera il valore come esadecimale se è preceduto da "0x". Le colonne sono colonne stringa e Patchwiz.dll convertiranno i valori in ULONG.

</dd> </dl>

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Applicazione di patch alle aree selezionate di un file](patching-selected-regions-of-a-file.md)
</dt> </dl>

 

 



