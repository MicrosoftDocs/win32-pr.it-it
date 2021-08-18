---
description: Le luci di un dispositivo telefonico possono essere accese in un'ampia gamma di modalità di illuminazione diverse.
ms.assetid: d8e8ef57-9faa-4122-b99a-3956362cd9d8
title: Lampade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 150e499dbd66ca772d35855c4cdb086bbb1ecc12617f55bcd33dccf8435e8771
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117762285"
---
# <a name="lamps"></a>Lampade

Le luci di un dispositivo telefonico possono essere accese in un'ampia gamma di modalità di illuminazione diverse. A differenza dei modelli di anello, le modalità lamp sono più uniformi tra i set di telefoni di fornitori diversi. Un set comune di modalità lamp è definito dall'API. Una lampadina identificata dall'identificatore del relativo pulsante lampo può essere accesa in una determinata modalità lamp. È anche possibile eseguire query su una lampadina per la modalità lamp corrente.

Le funzioni TAPI usate per le lampioni sono [**phoneSetLamp**](/windows/desktop/api/Tapi/nf-tapi-phonesetlamp), che accende una lampadina su un dispositivo telefonico aperto specificato in una determinata modalità di illuminazione lamp, e [**phoneGetLamp**](/windows/desktop/api/Tapi/nf-tapi-phonegetlamp), che restituisce la modalità lamp corrente della lampadina specificata.

Quando viene modificata una lampadina di un dispositivo telefonico, all'applicazione viene inviato un messaggio [**PHONE \_ STATE**](phone-state.md) per notificare all'applicazione la modifica dello stato. I parametri per questo messaggio forniscono un'indicazione della modifica.

 

 



