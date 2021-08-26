---
description: La tabella RemoveIniFile contiene le informazioni che un'applicazione deve eliminare da .ini file.
ms.assetid: 702cf86e-02f4-4ea7-8573-b500ac550aae
title: Tabella RemoveIniFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6aca38f320a8cb548faf00d284cff4c934e127a44cbaf7ca5b96013fac80d63
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120074581"
---
# <a name="removeinifile-table"></a>Tabella RemoveIniFile

La tabella RemoveIniFile contiene le informazioni che un'applicazione deve eliminare da .ini file.

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

<span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>Filename
</dt> <dd>

Nome .ini file in cui eliminare le informazioni.

</dd> <dt>

<span id="DirProperty"></span><span id="dirproperty"></span><span id="DIRPROPERTY"></span>DirProperty
</dt> <dd>

Nome di una proprietà il cui valore viene risolto nel percorso completo della cartella .ini file da rimuovere. La proprietà può essere il nome di una directory nella tabella [Directory](directory-table.md), una proprietà impostata dalla tabella [AppSearch](appsearch-table.md)o qualsiasi altra proprietà che rappresenta un percorso completo.

</dd> <dt>

<span id="Section"></span><span id="section"></span><span id="SECTION"></span>Sezione
</dt> <dd>

Sezione del file .ini localizzabile.

</dd> <dt>

<span id="Key"></span><span id="key"></span><span id="KEY"></span>Chiave
</dt> <dd>

Chiave del file .ini localizzabile sotto la sezione .

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valore
</dt> <dd>

Valore localizzabile da eliminare. Il valore è obbligatorio quando Action è 4.

</dd> <dt>

<span id="Action"></span><span id="action"></span><span id="ACTION"></span>Azione
</dt> <dd>

Tipo di modifica da apportare.



| Costante                         | Valore esadecimale | Decimal | Significato                          |
|----------------------------------|-------------|---------|----------------------------------|
| **msidbIniFileActionRemoveLine** | 0x002       | 2       | Elimina .ini voce.              |
| **msidbIniFileActionRemoveTag**  | 0x004       | 4       | Elimina un tag da una .ini voce. |



 

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_
</dt> <dd>

Chiave esterna nella prima colonna della tabella [Componente che](component-table.md) fa riferimento al componente che controlla l'eliminazione .ini valore.

</dd> </dl>

## <a name="remarks"></a>Commenti

Le .ini file vengono eliminate quando il componente corrispondente è stato selezionato per l'installazione, in locale o in esecuzione dall'origine.

Questa tabella viene definita quando viene eseguita [l'azione RemoveIniValues.](removeinivalues-action.md)

Se la colonna Directory viene specificata come Null, il percorso del file ini è il percorso Windows ini standard, ovvero la directory Windows \_ predefinita.

La rimozione dell'ultimo valore da una sezione elimina tale sezione. Non esiste altro modo per eliminare un'intera sezione oltre alla rimozione di tutti i relativi valori.

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE40](ice40.md)  
[ICE46](ice46.md)  
[ICE69](ice69.md)  
</dl>

 

 



