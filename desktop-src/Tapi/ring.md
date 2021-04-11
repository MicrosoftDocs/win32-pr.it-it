---
description: Un singolo telefono potrebbe essere in grado di squillare con diverse modalità di anello.
ms.assetid: c5ddcb3c-183c-4f97-9429-977d5cc32668
title: Anello
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f671aac6ead1938ff5b35ecb4996e4bc072a66d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967463"
---
# <a name="ring"></a>Anello

Un singolo telefono potrebbe essere in grado di squillare con diverse modalità di anello. Data la vasta gamma di modalità anello disponibili, le modalità suoneria vengono identificate tramite il numero di modalità anello. Un numero in modalità anello è compreso tra 0 e il numero di modalità suoneria disponibili meno uno.

Le funzioni che un'applicazione utilizzerebbe per controllare le modalità anello di un dispositivo telefonico sono [**phoneSetRing**](/windows/desktop/api/Tapi/nf-tapi-phonesetring), che squilla un dispositivo telefonico aperto in base a una determinata modalità di anello e [**phoneGetRing**](/windows/desktop/api/Tapi/nf-tapi-phonegetring), che restituisce la modalità suoneria corrente di un dispositivo telefonico aperto.

Quando la modalità suoneria di un dispositivo telefonico viene modificata, all'applicazione viene inviato un messaggio di [**\_ stato telefonico**](phone-state.md) per notificare all'applicazione la modifica dello stato. I parametri di questo messaggio forniscono un'indicazione della modifica.

 

 



