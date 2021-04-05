---
description: Quando si apre un dispositivo telefonico, l'applicazione può richiedere una delle due modalità operative.
ms.assetid: 2bb16fbe-883e-4734-a071-f14f5e5737e3
title: Modalità operative e privilegi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ba1cc01ed0552762ac3bc97449b1ae5a923cb10
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755119"
---
# <a name="operating-modes-and-privileges"></a>Modalità operative e privilegi

Quando si apre un dispositivo telefonico, l'applicazione può richiedere una delle due modalità operative. Queste modalità riflettono i privilegi richiesti dall'applicazione per il dispositivo:

-   L'apertura di un telefono per i privilegi di monitoraggio consente all'applicazione di determinare lo stato del dispositivo telefonico. I messaggi vengono inviati all'applicazione quando vengono rilevate modifiche allo stato sul dispositivo telefonico.
-   Un'applicazione che apre un dispositivo telefonico per i privilegi proprietario può utilizzare operazioni che modificano lo stato del dispositivo telefonico. Il privilegio proprietario include automaticamente anche i privilegi di monitoraggio completo. In qualsiasi momento, è possibile aprire un determinato dispositivo telefonico solo una volta per i privilegi di proprietario, ma più volte per i privilegi di monitoraggio. Tutte le operazioni di **telefonia** richiedono privilegi di proprietario, mentre tutte le operazioni **phoneGet** richiedono solo privilegi di monitoraggio.

 

 



