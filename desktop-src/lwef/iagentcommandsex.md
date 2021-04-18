---
title: IAgentCommandsEx
description: IAgentCommandsEx
ms.assetid: 6c354677-4cdb-4a74-9c41-2d0bf6f8dd55
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d16616ccb86bf109dad85a8ee2ac5d2bd009827
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299795"
---
# <a name="iagentcommandsex"></a>IAgentCommandsEx

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

[**IAgentCommandsEx**](iagentcommandex.md) definisce un'interfaccia che estende l'interfaccia [**IAgentCommands**](iagentcommands.md) .

**Metodi nell'ordine Vtable**



| Metodi IAgentCommandsEx                                                             | Descrizione                                                                                                   |
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [SetDefaultID](iagentcommandsex--setdefaultid.md)                                   | Imposta il comando predefinito per il menu di scelta rapida del carattere.                                                     |
| [GetDefaultID](iagentcommandsex--getdefaultid.md)                                   | Restituisce il comando predefinito per il menu di scelta rapida del carattere.                                                  |
| [**SetHelpContextID**](iagentcommandex--sethelpcontextid.md)                        | Imposta l'ID dell'argomento della Guida sensibile al contesto per un oggetto [**comando**](/windows/desktop/lwef/the-command-object) .                     |
| [**GetHelpContextID**](iagentcommandex--gethelpcontextid.md)                        | Restituisce l'ID dell'argomento della Guida sensibile al contesto per un oggetto [**comando**](/windows/desktop/lwef/the-command-object) .                  |
| [Sefontname](iagentcommandsex--setfontname.md)                                     | Imposta il tipo di carattere da utilizzare nel menu popup del carattere.                                                          |
| [GetFontName](iagentcommandsex--getfontname.md)                                     | Restituisce il tipo di carattere utilizzato nel menu a comparsa del carattere.                                                         |
| [SetFontSize](iagentcommandsex--setfontsize.md)                                     | Imposta la dimensione del carattere da utilizzare nel menu a comparsa del carattere.                                                     |
| [GetFontSize](iagentcommandsex--getfontsize.md)                                     | Restituisce la dimensione del carattere utilizzata nel menu popup del carattere.                                                    |
| [**SetVoiceCaption**](iagentcommandex--setvoicecaption.md)                          | Imposta la didascalia vocale per l'oggetto [**comando**](/windows/desktop/lwef/the-command-object) del carattere.                         |
| [**GetVoiceCaption**](iagentcommandex--getvoicecaption.md)                          | Restituisce la didascalia vocale per l'oggetto [**comando**](/windows/desktop/lwef/the-command-object) del carattere.                      |
| [AddEx](iagentcommandsex--addex.md)                                                 | Aggiunge un oggetto [**Command**](/windows/desktop/lwef/the-command-object) a una raccolta di [**comandi**](/windows/desktop/lwef/the-commands-collection-object) .    |
| [InsertEx](iagentcommandsex--insertex.md)                                           | Inserisce un oggetto [**Command**](/windows/desktop/lwef/the-command-object) in una raccolta di [**comandi**](/windows/desktop/lwef/the-commands-collection-object) . |
| [SetGlobalVoiceCommandsEnabled](iagentcommandsex--setglobalvoicecommandsenabled.md) | Abilita la grammatica vocale per i comandi globali dell'agente.                                                        |
| [GetGlobalVoiceCommandsEnabled](iagentcommandsex--getglobalvoicecommandsenabled.md) | Restituisce un valore che indica se la grammatica vocale per i comandi globali dell'agente è abilitata.                                     |



 

 

 