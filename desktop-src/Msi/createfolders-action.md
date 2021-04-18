---
description: L'azione CreateFolders crea cartelle vuote per i componenti impostati per l'installazione.
ms.assetid: 3982eac8-8272-4fb4-870c-390a0b6bd9a1
title: Azione CreateFolders
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 349388bf07fe867fc2cd88df6b5c7a76d28a1bf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319440"
---
# <a name="createfolders-action"></a>Azione CreateFolders

L'azione CreateFolders crea cartelle vuote per i componenti impostati per l'installazione. Il programma di installazione crea cartelle per i componenti eseguiti localmente ed eseguiti dall'origine. Le cartelle appena create vengono registrate con l'identificatore del componente appropriato.

L'azione CreateFolders esegue una query sulla [tabella CreateFolder](createfolder-table.md) e sulla [tabella Component](component-table.md).

## <a name="sequence-restrictions"></a>Restrizioni sequenza

L'azione CreateFolders deve essere eseguita prima dell'azione [InstallFiles](installfiles-action.md) o prima di qualsiasi azione che aggiunga file alle cartelle.

## <a name="actiondata-messages"></a>Messaggi ActionData



| Campo | Descrizione della descrizione dei dati dell'azione |
|-------|----------------------------------------|
| \[1\] | Identificatore di directory della cartella.        |



 

## <a name="remarks"></a>Commenti

Il programma di installazione non rimuove automaticamente le cartelle create dall'azione CreateFolders durante una disinstallazione dell'applicazione. Il programma di installazione rimuove solo le cartelle se l' [azione RemoveFolders](removefolders-action.md) è inclusa nella sequenza di azione.

 

 



