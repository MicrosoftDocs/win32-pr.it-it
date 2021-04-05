---
description: Le lampade su un dispositivo telefonico possono essere accese in un'ampia gamma di diverse modalità di illuminazione.
ms.assetid: d8e8ef57-9faa-4122-b99a-3956362cd9d8
title: Lampade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e01005c282b7a86b4b8c8ee27348ba4cf8d43db9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058062"
---
# <a name="lamps"></a>Lampade

Le lampade su un dispositivo telefonico possono essere accese in un'ampia gamma di diverse modalità di illuminazione. A differenza dei modelli di suoneria, le modalità Lamp sono più uniformi tra set di telefoni di fornitori diversi. Un set comune di modalità lampada viene definito dall'API. Una lampada identificata dall'identificatore del pulsante della lampada può essere accesa in una determinata modalità lampada. È anche possibile eseguire una query su una lampada per la modalità lampada corrente.

Le funzioni TAPI usate per le lampade sono [**phoneSetLamp**](/windows/desktop/api/Tapi/nf-tapi-phonesetlamp), che illumina una lampada su un dispositivo telefonico aperto specificato in una determinata modalità di illuminazione LAMP e [**phoneGetLamp**](/windows/desktop/api/Tapi/nf-tapi-phonegetlamp), che restituisce la modalità corrente della lampada specificata.

Quando viene modificata una lampada di un dispositivo telefonico, all'applicazione viene inviato un messaggio di [**\_ stato telefonico**](phone-state.md) per notificare all'applicazione la modifica dello stato. I parametri di questo messaggio forniscono un'indicazione della modifica.

 

 



