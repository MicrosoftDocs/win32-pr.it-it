---
description: Un singolo telefono può essere in grado di eseguire il ring con modalità anello diverse.
ms.assetid: c5ddcb3c-183c-4f97-9429-977d5cc32668
title: Anello
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5d183c217447ca02bf5ee0c535360eecaea1f3c209cdb813ad58b77268f234d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119773361"
---
# <a name="ring"></a>Anello

Un singolo telefono può essere in grado di eseguire il ring con modalità anello diverse. Data l'ampia gamma di modalità anello disponibili, le modalità anello vengono identificate tramite il relativo numero di modalità anello. Un numero di modalità anello è compreso tra zero e il numero di modalità anello disponibili meno uno.

Le funzioni usate da un'applicazione per controllare le modalità anello di un dispositivo telefono sono [**phoneSetRing**](/windows/desktop/api/Tapi/nf-tapi-phonesetring), che chiama un dispositivo telefono aperto in base a una determinata modalità anello, e [**phoneGetRing**](/windows/desktop/api/Tapi/nf-tapi-phonegetring), che restituisce la modalità anello corrente di un dispositivo telefono aperto.

Quando viene modificata la modalità anello di un dispositivo telefono, viene inviato un messaggio [**PHONE \_ STATE**](phone-state.md) all'applicazione per notificare all'applicazione la modifica dello stato. I parametri di questo messaggio forniscono un'indicazione della modifica.

 

 



