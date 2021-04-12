---
description: L'azione RemoveFolders rimuove tutte le cartelle collegate ai componenti impostati per la rimozione o l'esecuzione dall'origine. Queste cartelle vengono rimosse solo se sono vuote. Se una cartella viene rimossa, viene annullata la registrazione con l'identificatore del componente appropriato.
ms.assetid: 0f68458e-ae9a-4ca5-bc60-06d4de91e2e9
title: Azione RemoveFolders
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69648fbae333f0e7b989f2e989f0982d49736317
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232439"
---
# <a name="removefolders-action"></a>Azione RemoveFolders

L'azione RemoveFolders rimuove tutte le cartelle collegate ai componenti impostati per la rimozione o l'esecuzione dall'origine. Queste cartelle vengono rimosse solo se sono vuote. Se una cartella viene rimossa, viene annullata la registrazione con l'identificatore del componente appropriato.

## <a name="sequence-restrictions"></a>Restrizioni sequenza

L'azione RemoveFolders deve provenire dopo l'azione [RemoveFiles](removefiles-action.md) o qualsiasi azione che potrebbe rimuovere file dalle cartelle.

## <a name="actiondata-messages"></a>Messaggi ActionData



| Campo | Descrizione dei dati dell'azione    |
|-------|-------------------------------|
| \[1\] | Identificatore della cartella rimossa. |



 

## <a name="remarks"></a>Commenti

Il programma di installazione non rimuove automaticamente le cartelle create dall' [azione CreateFolders](createfolders-action.md) durante una disinstallazione dell'applicazione. È necessario indicare al programma di installazione di rimuovere queste cartelle creando l'azione RemoveFolders nella sequenza di azione.

Per specificare il nome e il percorso della cartella, utilizzare la \_ colonna directory della [tabella CreateFolder](createfolder-table.md). Si presuppone che ogni nome di cartella nella tabella CreateFolder sia una proprietà che definisce il percorso della cartella.

Per specificare il componente proprietario della cartella, utilizzare la colonna ComponentId della [tabella Component](component-table.md).

 

 



