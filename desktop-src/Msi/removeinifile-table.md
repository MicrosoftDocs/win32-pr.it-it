---
description: La tabella RemoveIniFile contiene le informazioni che un'applicazione deve eliminare da un file ini.
ms.assetid: 702cf86e-02f4-4ea7-8573-b500ac550aae
title: Tabella RemoveIniFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b57b4ba6f2c42ee636f1b9e21e798e27665f102a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318650"
---
# <a name="removeinifile-table"></a>Tabella RemoveIniFile

La tabella RemoveIniFile contiene le informazioni che un'applicazione deve eliminare da un file ini.

La tabella RemoveIniFile include le colonne seguenti.



| Colonna        | Tipo                         | Chiave | Nullable |
|---------------|------------------------------|-----|----------|
| RemoveIniFile | [Identificatore](identifier.md) | S   | N        |
| FileName      | [FileName](text.md)         | N   | N        |
| DirProperty   | [Identificatore](identifier.md) | N   | S        |
| Sezione       | [Formattato](formatted.md)   | N   | N        |
| Chiave           | [Formattato](formatted.md)   | N   | N        |
| Valore         | [Formattato](formatted.md)   | N   | S        |
| Azione        | [Integer](integer.md)       | N   | N        |
| Componente\_   | [Identificatore](identifier.md) | N   | N        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="RemoveIniFile"></span><span id="removeinifile"></span><span id="REMOVEINIFILE"></span>RemoveIniFile
</dt> <dd>

Chiave per questa tabella.

</dd> <dt>

<span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>FileName
</dt> <dd>

Nome del file ini in cui eliminare le informazioni.

</dd> <dt>

<span id="DirProperty"></span><span id="dirproperty"></span><span id="DIRPROPERTY"></span>DirProperty
</dt> <dd>

Nome di una proprietà il cui valore si presuppone venga risolto nel percorso completo della cartella del file ini da rimuovere. La proprietà può essere il nome di una directory nella [tabella di directory](directory-table.md), una proprietà impostata dalla [tabella AppSearch](appsearch-table.md)o qualsiasi altra proprietà che rappresenta un percorso completo.

</dd> <dt>

<span id="Section"></span><span id="section"></span><span id="SECTION"></span>Sezione
</dt> <dd>

Sezione del file con estensione ini localizzabile.

</dd> <dt>

<span id="Key"></span><span id="key"></span><span id="KEY"></span>Chiave
</dt> <dd>

Chiave del file. ini localizzabile sotto la sezione.

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valore
</dt> <dd>

Valore localizzabile da eliminare. Il valore è obbligatorio quando l'azione è 4.

</dd> <dt>

<span id="Action"></span><span id="action"></span><span id="ACTION"></span>Azione
</dt> <dd>

Tipo di modifica da apportare.



| Costante                         | Valore esadecimale | Decimal | Significato                          |
|----------------------------------|-------------|---------|----------------------------------|
| **msidbIniFileActionRemoveLine** | 0x002       | 2       | Elimina la voce. ini.              |
| **msidbIniFileActionRemoveTag**  | 0x004       | 4       | Elimina un tag da una voce. ini. |



 

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_
</dt> <dd>

Chiave esterna nella prima colonna della [tabella dei componenti](component-table.md) che fa riferimento al componente che controlla l'eliminazione del valore ini.

</dd> </dl>

## <a name="remarks"></a>Commenti

Le informazioni sul file ini vengono eliminate quando il componente corrispondente è stato selezionato per l'installazione, localmente o eseguito dall'origine.

Questa tabella viene definita quando viene eseguita l' [azione RemoveIniValues](removeinivalues-action.md) .

Se la \_ colonna directory è specificata come null, il percorso del file ini è il percorso standard di Windows ini, che è la directory di Windows per impostazione predefinita.

La rimozione dell'ultimo valore da una sezione comporta l'eliminazione di tale sezione. Non esiste un altro modo per eliminare un'intera sezione diversa dalla rimozione di tutti i relativi valori.

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE40](ice40.md)  
[ICE46](ice46.md)  
[ICE69](ice69.md)  
</dl>

 

 



