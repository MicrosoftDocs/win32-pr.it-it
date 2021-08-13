---
description: La tabella ExternalFiles contiene informazioni su file specifici che non fanno parte di un'immagine di destinazione normale.
ms.assetid: c75591c2-5266-4a99-8104-53815f6550e2
title: Tabella ExternalFiles (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2573556e8e4e00cf9004b83520468724ad1c959704cf8be32769a7ee41e24ebf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118636878"
---
# <a name="externalfiles-table-patchwizdll"></a>Tabella ExternalFiles (Patchwiz.dll)

La tabella ExternalFiles contiene informazioni su file specifici che non fanno parte di un'immagine di destinazione normale. Questi file possono essere presenti in prodotti aggiornati da un altro prodotto, aggiornamento o patch. Questa tabella è facoltativa nel database di creazione delle patch (file con estensione pcp) e viene usata dalla [funzione UiCreatePatchPackageEx.](uicreatepatchpackageex--patchwiz-dll-.md)

La tabella ExternalFiles include le colonne seguenti.



| Colonna        | Tipo    | Chiave | Nullable |
|---------------|---------|-----|----------|
| Famiglia        | text    | S   | N        |
| FTK           | text    | S   | N        |
| FilePath      | text    | S   | N        |
| Percorsi dei simboli   | text    |     | S        |
| IgnoreOffsets | text    |     | S        |
| IgnoreLengths | text    |     | S        |
| RetainOffsets | text    |     | N        |
| JSON         | numero intero |     | S        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="Family"></span><span id="family"></span><span id="FAMILY"></span>Famiglia
</dt> <dd>

Chiave esterna per la colonna Family della [tabella ImageFamilies (Patchwiz.dll).](imagefamilies-table-patchwiz-dll-.md)

</dd> <dt>

<span id="FTK"></span><span id="ftk"></span>FTK
</dt> <dd>

Chiave esterna nella [tabella File](file-table.md) del file .msi dell'immagine aggiornata.

</dd> <dt>

<span id="FilePath"></span><span id="filepath"></span><span id="FILEPATH"></span>Filepath
</dt> <dd>

Percorso completo del file esterno, incluso il nome del file. Il campo FilePath viene usato per individuare il file specificato nella colonna FTK.

</dd> <dt>

<span id="SymbolPaths"></span><span id="symbolpaths"></span><span id="SYMBOLPATHS"></span>Percorsi dei simboli
</dt> <dd>

Percorso completo in cui vengono cercati i file di simboli del file specificato nella colonna FTK.

</dd> <dt>

<span id="IgnoreOffsets"></span><span id="ignoreoffsets"></span><span id="IGNOREOFFSETS"></span>IgnoreOffsets
</dt> <dd>

Il valore in questo campo è un elenco delimitato da virgole di numeri di offset di intervallo per gli intervalli da ignorare nel file esterno. L'ordine e il numero degli intervalli nell'elenco devono corrispondere agli elementi nella colonna IgnoreLengths. Questa colonna è facoltativa.

I valori possono essere decimali o esadecimali. [Patchwiz.dll](patchwiz-dll.md) considera il valore come esadecimale se è preceduto da "0x". Le colonne sono colonne stringa e Patchwiz.dll convertiranno i valori in ULONG.

</dd> <dt>

<span id="IgnoreLengths"></span><span id="ignorelengths"></span><span id="IGNORELENGTHS"></span>IgnoreLengths
</dt> <dd>

Il valore in questo campo è un elenco delimitato da virgole di lunghezze di intervallo in byte per gli intervalli da ignorare nel file esterno. L'ordine e il numero degli intervalli nell'elenco devono corrispondere agli elementi nella colonna IgnoreOffsets. Questa colonna è facoltativa.

I valori possono essere decimali o esadecimali. [Patchwiz.dll](patchwiz-dll.md) considera il valore come esadecimale se è preceduto da "0x". Le colonne sono colonne stringa e Patchwiz.dll convertiranno i valori in ULONG.

</dd> <dt>

<span id="RetainOffsets"></span><span id="retainoffsets"></span><span id="RETAINOFFSETS"></span>RetainOffsets
</dt> <dd>

Il valore in questo campo è un elenco delimitato da virgole di numeri di offset di intervallo per gli intervalli da mantenere nel file esterno. L'ordine e il numero degli intervalli nell'elenco devono corrispondere agli elementi nella colonna RetainOffsets del record corrispondente nella tabella [FamilyFileRanges (Patchwiz.dll).](familyfileranges-table-patchwiz-dll-.md)

I valori possono essere decimali o esadecimali. [Patchwiz.dll](patchwiz-dll.md) considera il valore come esadecimale se è preceduto da "0x". Le colonne sono colonne stringa e Patchwiz.dll convertiranno i valori in ULONG.

</dd> <dt>

<span id="Order"></span><span id="order"></span><span id="ORDER"></span>Ordine
</dt> <dd>

Se vengono specificate due o più versioni per lo stesso file esterno, la tabella può contenere più record con valori corrispondenti nei campi FTK e Family. In questo caso, il campo Ordine può specificare l'ordine dei file esterni da usare durante la creazione della patch. L'ordine è dalla versione meno recente alla versione più recente.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa tabella accetta le variabili di ambiente come percorsi a partire dalla versione 4.0 di Patchwiz.dll.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Applicazione di patch alle aree selezionate di un file](patching-selected-regions-of-a-file.md)
</dt> </dl>

 

 



