---
title: IAgent
description: IAgent
ms.assetid: 35b12006-a938-450c-969a-7b73a3768a4d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3931c277fbe4a5943ef5881da12cf3669b2e8894c95052f61bc8411e21c7ae3c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118751426"
---
# <a name="iagent"></a>IAgent

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

**IAgent** definisce un'interfaccia che consente alle applicazioni di caricare caratteri, ricevere eventi e controllare lo stato corrente del server Microsoft Agent. Queste funzioni sono disponibili anche da [**IAgentEx.**](iagentex.md)

Il metodo GetSuspended incluso nelle versioni precedenti è obsoleto e restituisce **False** per compatibilità con le versioni precedenti.

**Metodi nell'ordine Vtable**



| Metodi IAgent                               | Descrizione                                                   |
|----------------------------------------------|---------------------------------------------------------------|
| [**Caricamento**](load-method.md)                  | Carica il file di dati di un carattere.                                |
| [**Scaricare**](unload-method.md)              | Scarica il file di dati di un carattere.                              |
| [**Registrazione**](iagent--register.md)         | Registra un sink di notifica per il client.                 |
| [**Unegister**](iagent--unregister.md)      | Annulla la registrazione del sink di notifica di un client.                     |
| [**GetCharacter**](iagent--getcharacter.md) | Restituisce l'interfaccia IAgentCharacter per un carattere caricato. |



 

 

 




