---
description: L'azione CreateFolders crea cartelle vuote per i componenti impostati per l'installazione.
ms.assetid: 3982eac8-8272-4fb4-870c-390a0b6bd9a1
title: Azione CreateFolders
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61182143488627c4724e470bf7f5158ed524cb4bc344c972c6744d14f773f6cd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105271"
---
# <a name="createfolders-action"></a>Azione CreateFolders

L'azione CreateFolders crea cartelle vuote per i componenti impostati per l'installazione. Il programma di installazione crea cartelle sia per i componenti che vengono eseguiti in locale che dall'origine. Le cartelle appena create vengono registrate con l'identificatore del componente appropriato.

L'azione CreateFolders esegue una query [sulla tabella CreateFolder](createfolder-table.md) e [sulla tabella Component](component-table.md).

## <a name="sequence-restrictions"></a>Restrizioni di sequenza

L'azione CreateFolders deve essere eseguita prima [dell'azione InstallFiles](installfiles-action.md) o prima di qualsiasi azione che aggiunge file alle cartelle.

## <a name="actiondata-messages"></a>Messaggi ActionData



| Campo | Descrizione della descrizione dei dati dell'azione |
|-------|----------------------------------------|
| \[1\] | Identificatore di directory della cartella.        |



 

## <a name="remarks"></a>Commenti

Il programma di installazione non rimuove automaticamente le cartelle create dall'azione CreateFolders durante una disinstallazione dell'applicazione. Il programma di installazione rimuove le cartelle solo [se l'azione RemoveFolders](removefolders-action.md) è inclusa nella sequenza di azioni.

 

 



