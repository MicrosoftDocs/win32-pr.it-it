---
description: La tabella CreateFolder contiene riferimenti a cartelle che devono essere create in modo esplicito per un determinato componente.
ms.assetid: b17b470b-6971-4124-8ec3-73914fdea95f
title: Tabella CreateFolder
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc286b32b48e0db9e5b991ab10af663c51538bf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232681"
---
# <a name="createfolder-table"></a>Tabella CreateFolder

La tabella CreateFolder contiene riferimenti a cartelle che devono essere create in modo esplicito per un determinato componente.

La tabella CreateFolder include le colonne seguenti.



| Colonna      | Tipo                         | Chiave | Nullable |
|-------------|------------------------------|-----|----------|
| Directory\_ | [Identificatore](identifier.md) | S   | N        |
| Componente\_ | [Identificatore](identifier.md) | S   | N        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="Directory_"></span><span id="directory_"></span><span id="DIRECTORY_"></span>Directory\_
</dt> <dd>

Chiave esterna nella prima colonna della tabella di [directory](directory-table.md).

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_
</dt> <dd>

Chiave esterna nella prima colonna della tabella dei [componenti](component-table.md).

</dd> </dl>

## <a name="remarks"></a>Commenti

Le cartelle in questa tabella vengono create quando viene installato il componente. Si è tentato di rimuovere queste cartelle solo quando il componente è stato disinstallato o spostato nell'origine. Non viene attivata alcuna rimozione automatica se le cartelle diventano vuote. Al contrario, le cartelle create dal programma di installazione ma non elencate in questa tabella vengono rimosse quando diventano vuote.

Poiché le cartelle create dal programma di installazione vengono eliminate quando diventano vuote, è necessario creare una voce nella tabella CreateFolder per installare un componente costituito da una cartella vuota.

Questa tabella viene definita quando viene chiamata l'azione [CreateFolders](createfolders-action.md) o [RemoveFolders](removefolders-action.md) .

Per informazioni su come proteggere una cartella, vedere la [tabella MsiLockPermissionsEx](msilockpermissionsex-table.md) e la [tabella LockPermissions](lockpermissions-table.md).

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE18](ice18.md)  
[ICE32](ice32.md)  
[ICE55](ice55.md)  
</dl>

 

 



