---
description: La tabella IniFile contiene le .ini che l'applicazione deve impostare in un file .ini.
ms.assetid: fdb1a627-da6b-4da1-87a7-7f1c94d3836e
title: Tabella IniFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4cd12c02fa0123ac9e1a763b4e725681e6c6b1d51a331a1efea9916b5ac4cbd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118946568"
---
# <a name="inifile-table"></a>Tabella IniFile

La tabella IniFile contiene le .ini che l'applicazione deve impostare in un file .ini.

La tabella IniFile contiene le colonne seguenti.



| Colonna      | Tipo                         | Chiave | Nullable |
|-------------|------------------------------|-----|----------|
| IniFile     | [Identificatore](identifier.md) | S   | N        |
| FileName    | [FileName](text.md)         | N   | N        |
| Proprietà Dir | [Identificatore](identifier.md) | N   | S        |
| Sezione     | [Formattato](formatted.md)   | N   | N        |
| Chiave         | [Formattato](formatted.md)   | N   | N        |
| Valore       | [Formattato](formatted.md)   | N   | N        |
| Azione      | [Integer](integer.md)       | N   | N        |
| Componente\_ | [Identificatore](identifier.md) | N   | N        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="IniFile"></span><span id="inifile"></span><span id="INIFILE"></span>IniFile
</dt> <dd>

Chiave per questa tabella.

</dd> <dt>

<span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>Filename
</dt> <dd>

Nome localizzabile del file .ini in cui scrivere le informazioni.

</dd> <dt>

<span id="DirProperty"></span><span id="dirproperty"></span><span id="DIRPROPERTY"></span>Proprietà Dir
</dt> <dd>

Nome di una proprietà con un valore che viene risolto nel percorso completo della cartella contenente il .ini file. La proprietà può essere il nome di una directory nella tabella [Directory,](directory-table.md)una proprietà impostata dalla tabella [AppSearch](appsearch-table.md)o qualsiasi altra proprietà che rappresenta un percorso completo. Se questo campo viene lasciato vuoto, il file .ini viene creato nella cartella con il percorso completo specificato dalla [**proprietà WindowsFolder.**](windowsfolder.md)

</dd> <dt>

<span id="Section"></span><span id="section"></span><span id="SECTION"></span>Sezione
</dt> <dd>

Sezione del file .ini localizzabile.

</dd> <dt>

<span id="Key"></span><span id="key"></span><span id="KEY"></span>Chiave
</dt> <dd>

Chiave del file .ini localizzabile all'interno della sezione .

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valore
</dt> <dd>

Valore localizzabile da scrivere.

</dd> <dt>

<span id="Action"></span><span id="action"></span><span id="ACTION"></span>Azione
</dt> <dd>

Tipo di modifica da apportare.



| Costante                         | Valore esadecimale | Decimal | Modifica                                                                     |
|----------------------------------|-------------|---------|----------------------------------------------------------------------------------|
| **msidbIniFileActionAddLine**    | 0x000       | 0       | Crea o aggiorna una .ini corrente.                                                 |
| **msidbIniFileActionCreateLine** | 0x001       | 1       | Crea una .ini solo se la voce non esiste già.                   |
| **msidbIniFileActionAddTag**     | 0x003       | 3       | Crea una nuova voce o aggiunge un nuovo valore delimitato da virgole a una voce esistente. |



 

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_
</dt> <dd>

Chiave esterna nella prima colonna della tabella [Component](component-table.md) che fa riferimento al componente che controlla l'installazione .ini valore.

</dd> </dl>

## <a name="remarks"></a>Commenti

Le .ini file vengono scritte quando il componente corrispondente è stato selezionato per l'installazione come locale o l'esecuzione dall'origine.

A questa tabella viene fatto riferimento quando viene [eseguita l'azione WriteIniValues](writeinivalues-action.md) o [RemoveIniValues.](removeinivalues-action.md)

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE46](ice46.md)  
[ICE69](ice69.md)  
[ICE88](ice88.md)  
[ICE91](ice91.md)  
</dl>

 

 



