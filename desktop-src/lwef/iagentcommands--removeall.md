---
title: IAgentCommands RemoveAll
description: IAgentCommands RemoveAll
ms.assetid: fab43363-6325-4566-b7bb-599591f67321
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8bd374b7c5767c416d2c3bb2281e651ba71acd8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103727039"
---
# <a name="iagentcommandsremoveall"></a>IAgentCommands:: RemoveAll

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT Remove();
```

Rimuove tutti i [**comandi**](/windows/desktop/lwef/the-command-object) da una raccolta di [**comandi**](/windows/desktop/lwef/the-commands-collection-object) .

-   Restituisce \_ OK per indicare che l'operazione è stata completata.

La rimozione di tutti i [**comandi**](/windows/desktop/lwef/the-command-object) da una raccolta di [**comandi**](/windows/desktop/lwef/the-commands-collection-object) li rimuove anche dal menu a comparsa e dalla **finestra comandi vocali** quando l'applicazione è di input-attivo. **RemoveAll** non rimuove le voci del server o di altri client.

## <a name="see-also"></a>Vedere anche

[**IAgentCommands:: Add**](iagentcommands--add.md), [**IAgentCommands:: Insert**](iagentcommands--insert.md), [**IAgentCommands:: Remove**](iagentcommands--remove.md)


 

 