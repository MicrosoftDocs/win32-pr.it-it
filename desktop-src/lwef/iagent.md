---
title: IAgent
description: IAgent
ms.assetid: 35b12006-a938-450c-969a-7b73a3768a4d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12900a4288b9917d695dd25d4b81362b67c93587
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330020"
---
# <a name="iagent"></a>IAgent

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

**IAgent** definisce un'interfaccia che consente alle applicazioni di caricare caratteri, ricevere eventi e controllare lo stato corrente del server Microsoft Agent. Queste funzioni sono disponibili anche da [**IAgentEx**](iagentex.md).

Il metodo getsuspended incluso nelle versioni precedenti è obsoleto e restituisce **false** per compatibilità con le versioni precedenti.

**Metodi nell'ordine Vtable**



| Metodi IAgent                               | Descrizione                                                   |
|----------------------------------------------|---------------------------------------------------------------|
| [**Caricamento**](load-method.md)                  | Carica un file di dati del carattere.                                |
| [**Scaricare**](unload-method.md)              | Scarica il file di dati di un carattere.                              |
| [**Registrazione**](iagent--register.md)         | Registra un sink di notifica per il client.                 |
| [**Unegister**](iagent--unregister.md)      | Annulla la registrazione di un sink di notifica del client.                     |
| [**Getcharacter**](iagent--getcharacter.md) | Restituisce l'interfaccia IAgentCharacter per un carattere caricato. |



 

 

 




