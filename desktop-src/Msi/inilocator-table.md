---
description: La tabella IniLocator contiene le informazioni necessarie per cercare un file o una directory usando un file .ini o per cercare una voce di .ini specifica. Il .ini file deve essere presente nella directory predefinita di Microsoft Windows.
ms.assetid: 5a3c6077-34ef-48c8-b4e6-ecb1deb40f96
title: Tabella IniLocator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5fae106340a953c59358c7c4108991d1510d49ea6d8940bcef72c538b7165ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118946541"
---
# <a name="inilocator-table"></a>Tabella IniLocator

La tabella IniLocator contiene le informazioni necessarie per cercare un file o una directory usando un file .ini o per cercare una voce di .ini specifica. Il .ini file deve essere presente nella directory predefinita di Microsoft Windows.

La tabella IniLocator contiene le colonne seguenti.



| Colonna      | Tipo                         | Chiave | Nullable |
|-------------|------------------------------|-----|----------|
| Firma\_ | [Identificatore](identifier.md) | S   | N        |
| FileName    | [FileName](text.md)         | N   | N        |
| Sezione     | [Text](text.md)             | N   | N        |
| Chiave         | [Text](text.md)             | N   | N        |
| Campo       | [Integer](integer.md)       | N   | Y        |
| Tipo        | [Integer](integer.md)       | N   | S        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Firma\_
</dt> <dd>

Chiave esterna nella prima colonna della [tabella Signature](signature-table.md). La firma \_ rappresenta una firma univoca ed è anche la chiave esterna nella colonna uno della tabella Signature. Se questa firma è presente nella tabella Firma, la ricerca è per un file. Se questa chiave non è presente nella tabella Signature e il valore della colonna Type è **msidbLocatorTypeRawValue,** la ricerca è relativa alla voce .ini specificata dalla tabella IniLocator. In caso contrario, la ricerca è per una directory specificata dalla tabella IniLocator.

</dd> <dt>

<span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>Filename
</dt> <dd>

Nome .ini file.

</dd> <dt>

<span id="Section"></span><span id="section"></span><span id="SECTION"></span>Sezione
</dt> <dd>

Nome della sezione all'interno .ini file.

</dd> <dt>

<span id="Key"></span><span id="key"></span><span id="KEY"></span>Chiave
</dt> <dd>

Valore della chiave all'interno della sezione .

</dd> <dt>

<span id="Field"></span><span id="field"></span><span id="FIELD"></span>Campo
</dt> <dd>

Campo nella riga .ini riga. Se Field è Null o 0, viene letta l'intera riga. Deve essere un numero non negativo.

</dd> <dt>

<span id="Type"></span><span id="type"></span><span id="TYPE"></span>digitare
</dt> <dd>

Valore che determina se il valore .ini è un percorso di file, un percorso di directory o un valore .ini non elaborato.

Nella tabella seguente sono elencati i valori validi. Se assente, Type è impostato su 1.



| Costante                      | Valore esadecimale | Decimal | Descrizione           |
|-------------------------------|-------------|---------|-----------------------|
| **msidbLocatorTypeDirectory** | 0x000       | 0       | Percorso della directory. |
| **msidbLocatorTypeFileName**  | 0x001       | 1       | Percorso del file.      |
| **msidbLocatorTypeRawValue**  | 0x002       | 2       | Valore di .ini non elaborato.     |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa tabella viene usata con la [tabella AppSearch](appsearch-table.md).

Le colonne di questa tabella in genere non sono localizzate. Se un autore decide di cercare i prodotti in più lingue, nella tabella può essere inclusa una voce separata per ogni lingua.

Il testo localizzato associato per la visualizzazione o la registrazione dello stato di avanzamento viene specificato nella [tabella ActionText](actiontext-table.md).

Vedere [Ricerca di applicazioni, file, voci del Registro di sistema](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md)o .ini file esistenti.

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
</dl>

 

 



