---
description: La tabella AppSearch contiene le proprietà necessarie per cercare un file con una particolare firma del file. La tabella AppSearch può essere utilizzata anche per impostare una proprietà sul valore esistente di una voce del registro di sistema o di un file ini.
ms.assetid: d560096f-6baa-4fea-8786-f4e3d5ee6bf4
title: Tabella AppSearch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9419a768a51364b4f22444288e6728a87289aa0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227211"
---
# <a name="appsearch-table"></a>Tabella AppSearch

La tabella AppSearch contiene le proprietà necessarie per cercare un file con una particolare firma del file. La tabella AppSearch può essere utilizzata anche per impostare una proprietà sul valore esistente di una voce del registro di sistema o di un file ini.

La tabella AppSearch include le colonne seguenti.



| Colonna      | Tipo                         | Chiave | Nullable |
|-------------|------------------------------|-----|----------|
| Proprietà    | [Identificatore](identifier.md) | S   | N        |
| Firma\_ | [Identificatore](identifier.md) | S   | N        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Proprietà
</dt> <dd>

Eseguendo l'azione [AppSearch](appsearch-action.md) , questa proprietà viene impostata sul percorso del file indicato dalla colonna Signature \_ . Questa proprietà viene impostata se la firma del file esiste nel computer dell'utente. Le proprietà usate in questa colonna devono essere proprietà [pubbliche](public-properties.md) e avere un identificatore che non contiene lettere minuscole.

La proprietà elencata nel campo della proprietà può essere inizializzata nella tabella delle [Proprietà](property-table.md) o da una riga di comando. Se l'azione [AppSearch](appsearch-action.md) individua la firma, il programma di installazione esegue l'override del valore della proprietà inizializzata con il valore trovato. Se la firma non viene trovata, viene usato il valore iniziale della proprietà. Se la proprietà non è mai stata inizializzata, la proprietà verrà impostata solo se la firma viene trovata. In caso contrario, la proprietà non è definita.

</dd> <dt>

<span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Firma\_
</dt> <dd>

La colonna della firma \_ contiene un identificatore univoco denominato firma ed è anche una chiave esterna nelle tabelle [RegLocator](reglocator-table.md), [IniLocator](inilocator-table.md), [CompLocator](complocator-table.md)e [DrLocator](drlocator-table.md) . Quando si cerca un file, anche il valore in questa colonna deve essere una chiave esterna nella tabella della [firma](signature-table.md) . Se il valore di questa colonna non è elencato nella tabella della firma, il programma di installazione determina che la ricerca è relativa a una directory.

</dd> </dl>

## <a name="remarks"></a>Commenti

L'azione [AppSearch](appsearch-action.md) nelle [*tabelle Sequence*](s-gly.md) elabora le informazioni contenute in questa tabella. Per informazioni sull'utilizzo di *tabelle di sequenza*, vedere [utilizzo di una tabella di sequenza](using-a-sequence-table.md).

L'azione [AppSearch](appsearch-action.md) Cerca le firme usando prima la tabella [CompLocator](complocator-table.md) , il secondo della tabella [RegLocator](reglocator-table.md) , la terza tabella [IniLocator](inilocator-table.md) e infine la tabella [DrLocator](drlocator-table.md) . Le firme dei file sono elencate nella tabella della [firma](signature-table.md) . Una firma che non è presente nella tabella delle firme indica una directory e l'azione imposta la proprietà sul percorso di directory per la firma.

Vedere [ricerca di applicazioni, file, voci del registro di sistema o voci di file ini esistenti](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md).

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE52](ice52.md)  
[ICE88](ice88.md)  
</dl>

 

 



