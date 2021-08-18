---
description: La tabella CreateFolder contiene riferimenti a cartelle che devono essere create in modo esplicito per un determinato componente.
ms.assetid: b17b470b-6971-4124-8ec3-73914fdea95f
title: Tabella CreateFolder
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c4cb926f6df388241a9c779328346a6e1bfb9fba4b365afce778c6e0b7a2548
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120045091"
---
# <a name="createfolder-table"></a>Tabella CreateFolder

La tabella CreateFolder contiene riferimenti a cartelle che devono essere create in modo esplicito per un determinato componente.

La tabella CreateFolder contiene le colonne seguenti.



| Colonna      | Tipo                         | Chiave | Nullable |
|-------------|------------------------------|-----|----------|
| Directory\_ | [Identificatore](identifier.md) | S   | N        |
| Componente\_ | [Identificatore](identifier.md) | S   | N        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="Directory_"></span><span id="directory_"></span><span id="DIRECTORY_"></span>Directory\_
</dt> <dd>

Chiave esterna nella prima colonna della [tabella Directory](directory-table.md).

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_
</dt> <dd>

Chiave esterna nella prima colonna della tabella [Component](component-table.md).

</dd> </dl>

## <a name="remarks"></a>Commenti

Le cartelle in questa tabella vengono create quando il componente viene installato. Viene effettuato un tentativo di rimuovere queste cartelle solo quando il componente viene disinstallato o spostato nell'esecuzione dall'origine. Se le cartelle diventano vuote, non viene attivata alcuna rimozione automatica. Al contrario, le cartelle create dal programma di installazione ma non elencate in questa tabella vengono rimosse quando diventano vuote.

Poiché le cartelle create dal programma di installazione vengono eliminate quando diventano vuote, è necessario creare una voce nella tabella CreateFolder per installare un componente costituito da una cartella vuota.

Questa tabella viene indicata quando viene chiamata [l'azione CreateFolders](createfolders-action.md) o [l'azione RemoveFolders.](removefolders-action.md)

Per informazioni su come proteggere una cartella, vedere La [tabella MsiLockPermissionsEx e](msilockpermissionsex-table.md) [la tabella LockPermissions.](lockpermissions-table.md)

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE18](ice18.md)  
[ICE32](ice32.md)  
[ICE55](ice55.md)  
</dl>

 

 



