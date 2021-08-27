---
title: IAgentUserInput
description: IAgentUserInput
ms.assetid: 59ce7337-6031-4449-8b29-fd0c6737c3e8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c58ed14c9097a4bd5d3d743a5c026f3e13d6d5ed29a73edb619dd0b2e8bdae17
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120114651"
---
# <a name="iagentuserinput"></a>IAgentUserInput

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

Quando il server invia una notifica al client attivo di input con [**IAgentNotifySink::Command,**](iagentnotifysink--command.md)restituisce informazioni tramite [**l'oggetto IAgentUserInput.**](/windows/desktop/lwef/iagentuserinput) **IAgentUserInput definisce** un'interfaccia che consente alle applicazioni di eseguire query su questi valori.

**Metodi nell'ordine Vtable**



| Metodi IAgentUserInput                                         | Descrizione                                                                                                                              |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetCount**](iagentuserinput--getcount.md)                   | Restituisce il numero di alternative di comando restituite in un [**evento Command.**](command-event.md)                                         |
| [**GetItemID**](iagentuserinput--getitemid.md)                 | Restituisce l'ID per un'alternativa [**command**](command-event.md) specifica.                                                              |
| [**GetItemConfidence**](iagentuserinput--getitemconfidence.md) | Restituisce il valore della proprietà [**Confidence per**](confidence-property.md) un'alternativa [**Command**](command-event.md) specifica. |
| [**GetItemText**](iagentuserinput--getitemtext.md)             | Restituisce il valore di [**Testo vocale**](voice-property.md) per un'alternativa [**command**](command-event.md) specifica.                   |
| [**GetAllItemData**](iagentuserinput--getallitemdata.md)       | Restituisce i dati per tutte [**le alternative command.**](command-event.md)                                                                  |



 

 

 