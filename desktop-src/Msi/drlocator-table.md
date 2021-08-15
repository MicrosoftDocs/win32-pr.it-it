---
description: La tabella DrLocator contiene le informazioni necessarie per trovare un file o una directory eseguendo una ricerca nell'albero di directory.
ms.assetid: 2b779ff7-f410-4af0-899d-4432b015d526
title: Tabella DrLocator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe1765c7b8f5c38d5701c4c401eb333c7db6a7c403689b8c3100d55b5e51e28e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118378325"
---
# <a name="drlocator-table"></a>Tabella DrLocator

La tabella DrLocator contiene le informazioni necessarie per trovare un file o una directory eseguendo una ricerca nell'albero di directory.

La tabella DrLocator contiene le colonne seguenti.



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

La colonna \_ Signature è una chiave esterna per la prima colonna della tabella [Signature](signature-table.md). Questo campo può rappresentare una firma di file univoca elencata nella tabella Firma. Se il valore in questa colonna non è presente nella tabella Signature, si presuppone che la ricerca sia per una directory a cui punta la tabella DrLocator.

</dd> <dt>

<span id="Parent"></span><span id="parent"></span><span id="PARENT"></span>genitore
</dt> <dd>

Questa colonna è la firma della directory padre del file o della directory nella colonna \_ Firma . Se questo campo è Null e la colonna Percorso non si espande fino a un percorso completo, la ricerca viene verificata in tutte le unità fisse del sistema dell'utente usando il percorso .

Questo campo è una chiave in una delle tabelle seguenti: [RegLocator](reglocator-table.md), [IniLocator](inilocator-table.md), [CompLocator](complocator-table.md)o DrLocator .

</dd> <dt>

<span id="Path"></span><span id="path"></span><span id="PATH"></span>Percorso
</dt> <dd>

La colonna Path contiene il percorso nel sistema dell'utente. Si tratta di un percorso completo o di un sottopercorso relativo sotto la directory specificata nella colonna Padre . Vedere le restrizioni sul tipo [di dati AnyPath.](anypath.md)

</dd> <dt>

<span id="Depth"></span><span id="depth"></span><span id="DEPTH"></span>Profondità
</dt> <dd>

Profondità sotto il percorso in cui il programma di installazione cerca il file o la directory specificata nella colonna \_ Firma. Il valore usato nel campo Depth è basato su zero. Ad esempio, se il campo Percorso è c:/Programmi/bin, la colonna Profondità deve essere impostata su 0 o superiore per rilevare un file che si trova all'interno del bin della cartella. Se il campo Profondità è vuoto, si presuppone che la profondità sia zero.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa tabella viene usata con la [tabella AppSearch](appsearch-table.md).

Le colonne di questa tabella in genere non sono localizzate. Se un autore decide di cercare prodotti in più lingue, nella tabella deve essere inclusa una voce separata per ogni lingua.

Vedere [Ricerca di applicazioni, file, voci del Registro di sistema](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md)o .ini file esistenti.

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE46](ice46.md)  
</dl>

 

 



