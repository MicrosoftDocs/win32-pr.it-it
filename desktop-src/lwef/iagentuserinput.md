---
title: IAgentUserInput
description: IAgentUserInput
ms.assetid: 59ce7337-6031-4449-8b29-fd0c6737c3e8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b37d195d6b5d1294c071a1b73d1da95548cb7a0
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104398945"
---
# <a name="iagentuserinput"></a>IAgentUserInput

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

Quando il server invia una notifica al client di input attivo con [**IAgentNotifySink:: Command**](iagentnotifysink--command.md), restituisce informazioni tramite l'oggetto [**IAgentUserInput**](/windows/desktop/lwef/iagentuserinput) . **IAgentUserInput** definisce un'interfaccia che consente alle applicazioni di eseguire query su questi valori.

**Metodi nell'ordine Vtable**



| Metodi IAgentUserInput                                         | Descrizione                                                                                                                              |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetCount**](iagentuserinput--getcount.md)                   | Restituisce il numero di alternative del comando restituite in un evento di [**comando**](command-event.md) .                                         |
| [**GetItemID**](iagentuserinput--getitemid.md)                 | Restituisce l'ID per un'alternativa del [**comando**](command-event.md) specifica.                                                              |
| [**GetItemConfidence**](iagentuserinput--getitemconfidence.md) | Restituisce il valore della proprietà [**confidenza**](confidence-property.md) per un'alternativa del [**comando**](command-event.md) specifica. |
| [**GetItemText**](iagentuserinput--getitemtext.md)             | Restituisce il valore del testo [**vocale**](voice-property.md) per un'alternativa del [**comando**](command-event.md) specifica.                   |
| [**GetAllItemData**](iagentuserinput--getallitemdata.md)       | Restituisce i dati per tutte le alternative dei [**comandi**](command-event.md) .                                                                  |



 

 

 