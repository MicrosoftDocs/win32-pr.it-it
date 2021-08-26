---
description: La tabella AppSearch contiene le proprietà necessarie per cercare un file con una firma di file specifica. La tabella AppSearch può essere usata anche per impostare una proprietà sul valore esistente di un registro o .ini voce del file.
ms.assetid: d560096f-6baa-4fea-8786-f4e3d5ee6bf4
title: Tabella AppSearch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 450ab07a397366ca01e664b88321942e4f6a7800cd9e04c4d0cbbe048eed8b87
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120045651"
---
# <a name="appsearch-table"></a>Tabella AppSearch

La tabella AppSearch contiene le proprietà necessarie per cercare un file con una firma di file specifica. La tabella AppSearch può essere usata anche per impostare una proprietà sul valore esistente di un registro o .ini voce del file.

La tabella AppSearch include le colonne seguenti.



| Colonna      | Tipo                         | Chiave | Nullable |
|-------------|------------------------------|-----|----------|
| Proprietà    | [Identificatore](identifier.md) | S   | N        |
| Firma\_ | [Identificatore](identifier.md) | S   | N        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Proprietà
</dt> <dd>

[L'esecuzione dell'azione AppSearch](appsearch-action.md) imposta questa proprietà sul percorso del file indicato dalla colonna \_ Firma. Questa proprietà viene impostata se la firma del file esiste nel computer dell'utente. Le proprietà usate in questa colonna devono essere [proprietà](public-properties.md) pubbliche e avere un identificatore che non contiene lettere minuscole.

La proprietà elencata nel campo Proprietà può essere inizializzata nella [tabella Proprietà](property-table.md) o da una riga di comando. Se [l'azione AppSearch](appsearch-action.md) individua la firma, il programma di installazione esegue l'override del valore della proprietà inizializzata con il valore trovato. Se la firma non viene trovata, viene usato il valore iniziale della proprietà. Se la proprietà non è mai stata inizializzata, la proprietà verrà impostata solo se viene trovata la firma. In caso contrario, la proprietà non è definita.

</dd> <dt>

<span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Firma\_
</dt> <dd>

La colonna Firma contiene un identificatore univoco denominato firma ed è anche una chiave esterna nelle tabelle \_ [RegLocator](reglocator-table.md), [IniLocator](inilocator-table.md), [CompLocator](complocator-table.md) [e DrLocator.](drlocator-table.md) Quando si cerca un file, anche il valore in questa colonna deve essere una chiave esterna nella [tabella Signature.](signature-table.md) Se il valore in questa colonna non è elencato nella tabella Firma, il programma di installazione determina che la ricerca è una directory.

</dd> </dl>

## <a name="remarks"></a>Commenti

[L'azione AppSearch](appsearch-action.md) nelle [*tabelle di sequenza*](s-gly.md) elabora le informazioni in questa tabella. Per informazioni sull'uso *delle tabelle di sequenza,* vedere [Uso di una tabella di sequenza](using-a-sequence-table.md).

[L'azione AppSearch](appsearch-action.md) cerca le firme usando prima la tabella [CompLocator,](complocator-table.md) la seconda tabella [RegLocator,](reglocator-table.md) la terza [tabella IniLocator](inilocator-table.md) e infine la [tabella DrLocator.](drlocator-table.md) Le firme di file sono elencate nella [tabella](signature-table.md) Firma. Una firma non presente nella tabella Signature indica una directory e l'azione imposta la proprietà sul percorso della directory per tale firma.

Vedere [Ricerca di applicazioni, file, voci del Registro di sistema](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md)o .ini file esistenti .

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE52](ice52.md)  
[ICE88](ice88.md)  
</dl>

 

 



