---
description: L'azione RemoveFolders rimuove tutte le cartelle collegate ai componenti impostati per la rimozione o l'esecuzione dall'origine. Queste cartelle vengono rimosse solo se sono vuote. Se una cartella viene rimossa, viene annullata la registrazione con l'identificatore del componente appropriato.
ms.assetid: 0f68458e-ae9a-4ca5-bc60-06d4de91e2e9
title: Azione RemoveFolders
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b476de044ef48b50120575a8d6991d27bf063dec37a026a2f5d2ea0e604abee0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082541"
---
# <a name="removefolders-action"></a>Azione RemoveFolders

L'azione RemoveFolders rimuove tutte le cartelle collegate ai componenti impostati per la rimozione o l'esecuzione dall'origine. Queste cartelle vengono rimosse solo se sono vuote. Se una cartella viene rimossa, viene annullata la registrazione con l'identificatore del componente appropriato.

## <a name="sequence-restrictions"></a>Restrizioni relative alle sequenze

L'azione RemoveFolders deve essere eseguita dopo [l'azione RemoveFiles](removefiles-action.md) o qualsiasi azione che può rimuovere file dalle cartelle.

## <a name="actiondata-messages"></a>Messaggi ActionData



| Campo | Descrizione dei dati dell'azione    |
|-------|-------------------------------|
| \[1\] | Identificatore della cartella rimossa. |



 

## <a name="remarks"></a>Commenti

Il programma di installazione non rimuove automaticamente le cartelle create [dall'azione CreateFolders](createfolders-action.md) durante una disinstallazione dell'applicazione. È necessario indicare al programma di installazione di rimuovere queste cartelle mediante la creazione dell'azione RemoveFolders nella sequenza di azioni.

Per specificare il nome e il percorso della cartella, usare la colonna Directory \_ della [tabella CreateFolder](createfolder-table.md). Si presuppone che ogni nome di cartella nella tabella CreateFolder sia una proprietà che definisce il percorso della cartella.

Per specificare il componente proprietario della cartella, usare la colonna ComponentId della [tabella Component](component-table.md).

 

 



