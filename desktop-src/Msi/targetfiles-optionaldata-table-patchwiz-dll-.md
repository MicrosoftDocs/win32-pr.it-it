---
description: La \_ tabella TargetFiles OptionalData contiene informazioni su file specifici in un'immagine di destinazione. Questa tabella è facoltativa nel database di creazione della patch (file con estensione PCP) e viene usata dalla funzione UiCreatePatchPackageEx.
ms.assetid: 577b1674-1e44-42e1-b011-c0fb561b514c
title: Tabella TargetFiles_OptionalData (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 859ac2e03f68c28eff5ebf7f5afa2bf53ab69299
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967900"
---
# <a name="targetfiles_optionaldata-table-patchwizdll"></a>\_Tabella TargetFiles OptionalData (Patchwiz.dll)

La \_ tabella TargetFiles OptionalData contiene informazioni su file specifici in un'immagine di destinazione. Questa tabella è facoltativa nel database di creazione della patch (file con estensione PCP) e viene usata dalla funzione [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) .

La \_ tabella OptionalData di TargetFiles include le colonne seguenti.



| Colonna        | Tipo | Chiave | Nullable |
|---------------|------|-----|----------|
| Destinazione        | text | S   | N        |
| FTK           | text | S   | N        |
| SymbolPaths   | text |     | S        |
| IgnoreOffsets | text |     | S        |
| IgnoreLengths | text |     | S        |
| RetainOffsets | text |     | S        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="Target"></span><span id="target"></span><span id="TARGET"></span>Destinazione
</dt> <dd>

Chiave esterna per la colonna di destinazione della [tabella TargetImages (Patchwiz.dll)](targetimages-table-patchwiz-dll-.md).

</dd> <dt>

<span id="FTK"></span><span id="ftk"></span>FTK
</dt> <dd>

Chiave esterna nella [tabella file](file-table.md) dell'immagine di destinazione.

</dd> <dt>

<span id="SymbolPaths"></span><span id="symbolpaths"></span><span id="SYMBOLPATHS"></span>SymbolPaths
</dt> <dd>

Il valore in questo campo viene aggiunto all'elenco delimitato da punti e virgola di cartelle nella colonna SymbolPaths della [tabella TargetImages (Patchwiz.dll)](targetimages-table-patchwiz-dll-.md) al momento della generazione della patch e può essere usato per aggiungere i file di simboli per un file specifico.

</dd> <dt>

<span id="IgnoreOffsets"></span><span id="ignoreoffsets"></span><span id="IGNOREOFFSETS"></span>IgnoreOffsets
</dt> <dd>

Il valore in questo campo è un elenco delimitato da virgole di numeri di offset intervallo per gli intervalli da ignorare nel file di destinazione. L'ordine e il numero degli intervalli nell'elenco devono corrispondere agli elementi della colonna IgnoreLengths. Questa colonna è facoltativa.

I valori possono essere decimali o esadecimali. [Patchwiz.dll](patchwiz-dll.md) considera il valore come esadecimale se è preceduto da "0x". Le colonne sono colonne stringa e Patchwiz.dll convertiranno i valori in ULONG.

</dd> <dt>

<span id="IgnoreLengths"></span><span id="ignorelengths"></span><span id="IGNORELENGTHS"></span>IgnoreLengths
</dt> <dd>

Il valore in questo campo è un elenco delimitato da virgole di lunghezze di intervallo in byte per gli intervalli da ignorare nel file di destinazione. L'ordine e il numero degli intervalli nell'elenco devono corrispondere agli elementi della colonna IgnoreOffsets. Questa colonna è facoltativa.

I valori possono essere decimali o esadecimali. [Patchwiz.dll](patchwiz-dll.md) considera il valore come esadecimale se è preceduto da "0x". Le colonne sono colonne stringa e Patchwiz.dll convertiranno i valori in ULONG.

</dd> <dt>

<span id="RetainOffsets"></span><span id="retainoffsets"></span><span id="RETAINOFFSETS"></span>RetainOffsets
</dt> <dd>

Il valore in questo campo è un elenco delimitato da virgole di numeri di offset intervallo per gli intervalli da conservare nel file di destinazione. L'ordine e il numero degli intervalli nell'elenco devono corrispondere agli elementi della colonna RetainOffsets del record corrispondente nella [tabella FamilyFileRanges (Patchwiz.dll)](familyfileranges-table-patchwiz-dll-.md)

I valori possono essere decimali o esadecimali. [Patchwiz.dll](patchwiz-dll.md) considera il valore come esadecimale se è preceduto da "0x". Le colonne sono colonne stringa e Patchwiz.dll convertiranno i valori in ULONG.

</dd> </dl>

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Applicazione di patch alle aree selezionate di un file](patching-selected-regions-of-a-file.md)
</dt> </dl>

 

 



