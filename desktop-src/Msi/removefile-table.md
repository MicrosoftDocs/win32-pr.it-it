---
description: La tabella RemoveFile contiene un elenco di file che devono essere rimossi dall'azione RemoveFiles. L'impostazione della colonna FileName di questa tabella su Null supporta la rimozione di cartelle vuote.
ms.assetid: 8b3cb0e3-ccc0-4030-8f57-aa124c3b5588
title: Tabella RemoveFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12cf63e9b7616eb033a696da2ad29cb4310e6dc0dc56279ef465c3c549cb5437
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082601"
---
# <a name="removefile-table"></a>Tabella RemoveFile

La tabella RemoveFile contiene un elenco di file che devono essere rimossi [dall'azione RemoveFiles](removefiles-action.md). L'impostazione della colonna FileName di questa tabella su Null supporta la rimozione di cartelle vuote.

La tabella RemoveFile include le colonne seguenti.



| Colonna      | Tipo                                     | Chiave | Nullable |
|-------------|------------------------------------------|-----|----------|
| FileKey     | [Identificatore](identifier.md)             | S   | N        |
| Componente\_ | [Identificatore](identifier.md)             | N   | N        |
| FileName    | [WildCardFilename](wildcardfilename.md) | N   | S        |
| DirProperty | [Identificatore](identifier.md)             | N   | N        |
| InstallMode | [Integer](integer.md)                   | N   | N        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="FileKey"></span><span id="filekey"></span><span id="FILEKEY"></span>FileKey
</dt> <dd>

Chiave primaria usata per identificare questa voce di tabella specifica.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_
</dt> <dd>

Chiave esterna della prima colonna della [tabella Component](component-table.md). Questo campo fa riferimento al componente che controlla il file da rimuovere.

</dd> <dt>

<span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>Filename
</dt> <dd>

Questa colonna contiene il nome localizzabile del file da rimuovere. Se questa colonna è Null, la cartella specificata verrà rimossa se è vuota. Tutti i file che corrispondono al carattere jolly verranno rimossi dalla directory specificata.

</dd> <dt>

<span id="DirProperty"></span><span id="dirproperty"></span><span id="DIRPROPERTY"></span>DirProperty
</dt> <dd>

Nome di una proprietà il cui valore viene risolto nel percorso completo della cartella del file da rimuovere. La proprietà può essere il nome di una directory nella tabella [Directory](directory-table.md), una proprietà impostata dalla tabella [AppSearch](appsearch-table.md)o qualsiasi altra proprietà che rappresenta un percorso completo.

</dd> <dt>

<span id="InstallMode"></span><span id="installmode"></span><span id="INSTALLMODE"></span>InstallMode
</dt> <dd>

Deve essere uno dei valori seguenti.



| Costante                                | Valore esadecimale | Decimal | Descrizione                                                                                                   |
|-----------------------------------------|-------------|---------|---------------------------------------------------------------------------------------------------------------|
| **msidbRemoveFileInstallModeOnInstall** | 0x001       | 1       | Rimuovere solo quando viene installato il componente associato (msiInstallStateLocal o msiInstallStateSource). |
| **msidbRemoveFileInstallModeOnRemove**  | 0x002       | 2       | Rimuovere solo quando il componente associato viene rimosso (msiInstallStateAbsent).                           |
| **msidbRemoveFileInstallModeOnBoth**    | 0x003       | 3       | Rimuovere in uno dei casi precedenti.                                                                          |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

I riferimenti ai file in questa tabella vengono elaborati [dall'azione RemoveFiles](removefiles-action.md).

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE18](ice18.md)  
[ICE32](ice32.md)  
[ICE45](ice45.md)  
[ICE64](ice64.md)  
</dl>

 

 



