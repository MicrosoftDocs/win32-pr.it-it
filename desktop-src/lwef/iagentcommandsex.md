---
title: IAgentCommandsEx
description: IAgentCommandsEx
ms.assetid: 6c354677-4cdb-4a74-9c41-2d0bf6f8dd55
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ff4ff8e6dc87eb1a5fa5c3e79fe26b00d8bd3c8eb18a5fc6ca7cac22d3dfd07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976261"
---
# <a name="iagentcommandsex"></a>IAgentCommandsEx

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

[**IAgentCommandsEx definisce**](iagentcommandex.md) un'interfaccia che estende [**l'interfaccia IAgentCommands.**](iagentcommands.md)

**Metodi nell'ordine Vtable**



| Metodi IAgentCommandsEx                                                             | Descrizione                                                                                                   |
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [SetDefaultID](iagentcommandsex--setdefaultid.md)                                   | Imposta il comando predefinito per il menu a comparsa del carattere.                                                     |
| [GetDefaultID](iagentcommandsex--getdefaultid.md)                                   | Restituisce il comando predefinito per il menu a comparsa del carattere.                                                  |
| [**SetHelpContextID**](iagentcommandex--sethelpcontextid.md)                        | Imposta l'ID dell'argomento della Guida sensibile al contesto per un [**oggetto**](/windows/desktop/lwef/the-command-object) Command.                     |
| [**GetHelpContextID**](iagentcommandex--gethelpcontextid.md)                        | Restituisce l'ID dell'argomento della Guida sensibile al contesto per un [**oggetto**](/windows/desktop/lwef/the-command-object) Command.                  |
| [SetFontName](iagentcommandsex--setfontname.md)                                     | Imposta il tipo di carattere da usare nel menu a comparsa del carattere.                                                          |
| [GetFontName](iagentcommandsex--getfontname.md)                                     | Restituisce il tipo di carattere utilizzato nel menu a comparsa del carattere.                                                         |
| [SetFontSize](iagentcommandsex--setfontsize.md)                                     | Imposta le dimensioni del carattere da usare nel menu a comparsa del carattere.                                                     |
| [GetFontSize](iagentcommandsex--getfontsize.md)                                     | Restituisce la dimensione del carattere utilizzata nel menu a comparsa del carattere.                                                    |
| [**SetVoiceCaption**](iagentcommandex--setvoicecaption.md)                          | Imposta la didascalia vocale per l'oggetto [**Command del**](/windows/desktop/lwef/the-command-object) carattere.                         |
| [**GetVoiceCaption**](iagentcommandex--getvoicecaption.md)                          | Restituisce la didascalia vocale per l'oggetto [**Command del**](/windows/desktop/lwef/the-command-object) carattere.                      |
| [AddEx](iagentcommandsex--addex.md)                                                 | Aggiunge un [**oggetto Command**](/windows/desktop/lwef/the-command-object) a una [**raccolta Commands.**](/windows/desktop/lwef/the-commands-collection-object)    |
| [InsertEx](iagentcommandsex--insertex.md)                                           | Inserisce un [**oggetto Command**](/windows/desktop/lwef/the-command-object) in una [**raccolta Commands.**](/windows/desktop/lwef/the-commands-collection-object) |
| [SetGlobalVoiceCommandsEnabled](iagentcommandsex--setglobalvoicecommandsenabled.md) | Abilita la grammatica vocale per i comandi globali di Agent.                                                        |
| [GetGlobalVoiceCommandsEnabled](iagentcommandsex--getglobalvoicecommandsenabled.md) | Restituisce un valore che indica se la grammatica vocale per i comandi globali di Agent è abilitata.                                     |



 

 

 