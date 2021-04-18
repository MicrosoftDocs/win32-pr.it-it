---
title: Selezione di oggetti non necessari
description: Se si usa ispeziona per esaminare un semplice controllo, ad esempio un pulsante OK nell'accessorio Microsoft WordPad, è possibile osservare che questi oggetti finestra padre contengono anche diversi oggetti figlio invisibili.
ms.assetid: 30884e11-cc73-4bb8-9d9e-b9f1b53c4193
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb341881ee2ea503b1f74643723a1f90c8e5d1d5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297901"
---
# <a name="screening-out-unnecessary-objects"></a>Selezione di oggetti non necessari

Se si usa [ispeziona](inspect-objects.md) per esaminare un semplice controllo, ad esempio un pulsante OK nell'accessorio Microsoft WordPad, è possibile osservare che questi oggetti finestra padre contengono anche diversi oggetti figlio invisibili. Questi oggetti invisibili hanno lo stesso nome della classe finestra del controllo e hanno la [proprietà state](state-property.md) del [**sistema di stato \_ \_ invisibile**](object-state-constants.md). Nella tabella seguente sono elencati gli oggetti figlio invisibili creati da Microsoft Active Accessibility per il controllo.



| Nome          | Ruolo                                                                  | ChildCount |
|---------------|-----------------------------------------------------------------------|------------|
| Sistema      | [**\_barra dei \_ menu sistema ruolo**](object-roles.md)     | 0          |
| nessuno          | [**barra di titolo \_ sistema ruolo \_**](object-roles.md)   | 5          |
| Applicazione | [**\_barra dei \_ menu sistema ruolo**](object-roles.md)     | 0          |
| Verticale    | [**\_barra di \_ scorrimento sistema ruolo**](object-roles.md) | 5          |
| Orizzontale  | [**\_barra di \_ scorrimento sistema ruolo**](object-roles.md) | 5          |
| "Casella dimensioni"    | [**\_grip sistema \_ ruolo**](object-roles.md)           | 0          |



 

Gli sviluppatori client devono identificare e filtrare gli oggetti finestra padre e gli oggetti figlio invisibili perché non forniscono informazioni significative agli utenti finali.

 

 




