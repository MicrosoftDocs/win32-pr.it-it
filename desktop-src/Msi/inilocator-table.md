---
description: La tabella IniLocator include le informazioni necessarie per cercare un file o una directory usando un file ini o per cercare una particolare voce. ini. Il file ini deve essere presente nella directory predefinita di Microsoft Windows.
ms.assetid: 5a3c6077-34ef-48c8-b4e6-ecb1deb40f96
title: Tabella IniLocator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89583a2d69fd88dd4b5624920e2374aa7e203103
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310800"
---
# <a name="inilocator-table"></a>Tabella IniLocator

La tabella IniLocator include le informazioni necessarie per cercare un file o una directory usando un file ini o per cercare una particolare voce. ini. Il file ini deve essere presente nella directory predefinita di Microsoft Windows.

La tabella IniLocator include le colonne seguenti.



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

Chiave esterna nella prima colonna della [tabella della firma](signature-table.md). La firma \_ rappresenta una firma univoca ed è anche la chiave esterna nella colonna uno della tabella di firma. Se la firma è presente nella tabella della firma, la ricerca è relativa a un file. Se questa chiave non è presente nella tabella della firma e il valore della colonna del tipo è **msidbLocatorTypeRawValue**, la ricerca è relativa alla voce. ini specificata dalla tabella IniLocator. In caso contrario, la ricerca è relativa a una directory specificata dalla tabella IniLocator.

</dd> <dt>

<span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>FileName
</dt> <dd>

Nome del file ini.

</dd> <dt>

<span id="Section"></span><span id="section"></span><span id="SECTION"></span>Sezione
</dt> <dd>

Nome della sezione all'interno del file ini.

</dd> <dt>

<span id="Key"></span><span id="key"></span><span id="KEY"></span>Chiave
</dt> <dd>

Valore della chiave nella sezione.

</dd> <dt>

<span id="Field"></span><span id="field"></span><span id="FIELD"></span>Campo
</dt> <dd>

Campo nella riga ini. Se Field è null o 0, viene letta l'intera riga. Deve essere un numero non negativo.

</dd> <dt>

<span id="Type"></span><span id="type"></span><span id="TYPE"></span>Tipo
</dt> <dd>

Valore che determina se il valore ini è un percorso di file, un percorso di directory o un valore RAW. ini.

Nella tabella seguente sono elencati i valori validi. Se assente, Type è impostato su 1.



| Costante                      | Valore esadecimale | Decimal | Descrizione           |
|-------------------------------|-------------|---------|-----------------------|
| **msidbLocatorTypeDirectory** | 0x000       | 0       | Percorso della directory. |
| **msidbLocatorTypeFileName**  | 0x001       | 1       | Percorso del file.      |
| **msidbLocatorTypeRawValue**  | 0x002       | 2       | Valore RAW. ini.     |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa tabella viene utilizzata con la [tabella AppSearch](appsearch-table.md).

Generalmente, le colonne della tabella non sono localizzate. Se un autore decide di cercare i prodotti in più lingue, è possibile che nella tabella sia inclusa una voce separata per ogni lingua.

Il testo localizzato associato per la visualizzazione o la registrazione dello stato di avanzamento è specificato nella [tabella ActionText](actiontext-table.md).

Vedere [ricerca di applicazioni, file, voci del registro di sistema o voci di file ini esistenti](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md).

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
</dl>

 

 



