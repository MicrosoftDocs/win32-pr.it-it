---
description: L'applicazione può richiedere una delle due modalità operative all'apertura di un dispositivo telefonico.
ms.assetid: 2bb16fbe-883e-4734-a071-f14f5e5737e3
title: Modalità operative e privilegi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44f7d3c1f6b7049c3986b96734a537906dc62166c48d62e549684cdaa6d35ba2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012471"
---
# <a name="operating-modes-and-privileges"></a>Modalità operative e privilegi

L'applicazione può richiedere una delle due modalità operative all'apertura di un dispositivo telefonico. Queste modalità riflettono i privilegi che l'applicazione richiede per il dispositivo:

-   L'apertura di un telefono per i privilegi di monitoraggio consente all'applicazione di determinare lo stato del dispositivo telefonico. I messaggi vengono inviati all'applicazione quando viene rilevato un cambiamento di stato nel dispositivo telefonico.
-   Un'applicazione che apre un dispositivo telefonico per i privilegi di proprietario può usare operazioni che modificano lo stato del dispositivo. Il privilegio proprietario include automaticamente anche i privilegi di monitoraggio completo. In qualsiasi momento, un determinato dispositivo telefonico può essere aperto una sola volta per i privilegi di proprietario, ma più volte per i privilegi di monitoraggio. Tutte **le operazioni phoneSet** richiedono privilegi di proprietario, mentre tutte **le operazioni phoneGet** richiedono solo privilegi di monitoraggio.

 

 



