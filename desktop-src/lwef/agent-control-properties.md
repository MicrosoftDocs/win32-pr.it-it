---
title: Proprietà del controllo agente
description: Proprietà del controllo agente
ms.assetid: e6a5b2db-9abf-4988-be41-fc7f4530507f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f5e80b10469e7e256b1b2bf3bcf55fb5a8a08b5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044273"
---
# <a name="agent-control-properties"></a>Proprietà del controllo agente

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

Le proprietà seguenti sono accessibili direttamente dal controllo agente:

-   [**Connesso**](connected-property.md)
-   [**Nome**](name-property-a.md)
-   [**RaiseRequestErrors**](raiserequesterrors-property.md)

Inoltre, alcuni ambienti di programmazione possono assegnare proprietà aggiuntive in fase di progettazione o in fase di esecuzione. Ad esempio, Visual Basic aggiunge le proprietà Left, index, tag e top che definiscono la posizione del controllo in un form anche se il controllo non viene visualizzato nella pagina del form in fase di esecuzione.

La proprietà Suspended è ancora supportata per la compatibilità con le versioni precedenti, ma restituisce sempre **false** perché il server non supporta più lo stato Suspended.

 

 




