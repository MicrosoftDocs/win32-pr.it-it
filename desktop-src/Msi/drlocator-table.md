---
description: La tabella DrLocator contiene le informazioni necessarie per trovare un file o una directory eseguendo una ricerca nell'albero di directory.
ms.assetid: 2b779ff7-f410-4af0-899d-4432b015d526
title: Tabella DrLocator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78df5a5af83a18a14027b88033e977b2c63d2027
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308193"
---
# <a name="drlocator-table"></a>Tabella DrLocator

La tabella DrLocator contiene le informazioni necessarie per trovare un file o una directory eseguendo una ricerca nell'albero di directory.

La tabella DrLocator include le colonne seguenti.



| Colonna      | Tipo                         | Chiave | Nullable |
|-------------|------------------------------|-----|----------|
| Firma\_ | [Identificatore](identifier.md) | S   | N        |
| Padre      | [Identificatore](identifier.md) | S   | S        |
| Percorso        | [AnyPath](anypath.md)       | S   | S        |
| Profondità       | [Integer](integer.md)       | N   | S        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Firma\_
</dt> <dd>

La \_ colonna Signature è una chiave esterna per la prima colonna della [tabella Signature](signature-table.md). Questo campo può rappresentare una firma del file univoca elencata nella tabella della firma. Se il valore in questa colonna è assente dalla tabella di firma, si presuppone che la ricerca sia per una directory a cui punta la tabella DrLocator.

</dd> <dt>

<span id="Parent"></span><span id="parent"></span><span id="PARENT"></span>Padre
</dt> <dd>

Questa colonna è la firma della directory padre del file o della directory nella \_ colonna firma. Se questo campo è null e la colonna Path non si espande in un percorso completo, viene eseguita la ricerca in tutte le unità fisse del sistema dell'utente usando il percorso.

Questo campo è una chiave in una delle tabelle seguenti: [RegLocator](reglocator-table.md), [IniLocator](inilocator-table.md), [CompLocator](complocator-table.md)o DrLocator.

</dd> <dt>

<span id="Path"></span><span id="path"></span><span id="PATH"></span>Percorso
</dt> <dd>

La colonna percorso contiene il percorso nel sistema dell'utente. Si tratta di un percorso completo o di un sottopercorso relativo sotto la directory specificata nella colonna padre. Vedere le restrizioni sul tipo di dati [AnyPath](anypath.md) .

</dd> <dt>

<span id="Depth"></span><span id="depth"></span><span id="DEPTH"></span>Profondità
</dt> <dd>

Profondità sotto il percorso in cui il programma di installazione cerca il file o la directory specificata nella \_ colonna Signature. Il valore utilizzato nel campo Depth è basato su zero. Se ad esempio il campo percorso è c:/Program Files/bin, la colonna Depth deve essere impostata su 0 o su un valore maggiore per rilevare un file che si trova all'interno del contenitore di cartelle. Se il campo Depth è vuoto, si presuppone che la profondità sia zero.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa tabella viene utilizzata con la [tabella AppSearch](appsearch-table.md).

Generalmente, le colonne della tabella non sono localizzate. Se un autore decide di cercare i prodotti in più lingue, è necessario che nella tabella sia inclusa una voce separata per ogni lingua.

Vedere [ricerca di applicazioni, file, voci del registro di sistema o voci di file ini esistenti](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md).

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE46](ice46.md)  
</dl>

 

 



