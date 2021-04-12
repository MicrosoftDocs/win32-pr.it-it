---
title: Informazioni sui messaggi SNMP
description: Il Simple Network Management Protocol utilizza messaggi per comunicare e scambiare informazioni tra entità SNMP remote.
ms.assetid: 9ba4b854-fc02-40c1-a92f-7c102c900e95
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a0426bf44d976ddf9e2eafe2093dcea94956cb4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395595"
---
# <a name="about-snmp-messages"></a>Informazioni sui messaggi SNMP

Il Simple Network Management Protocol utilizza messaggi per comunicare e scambiare informazioni tra entità SNMP remote. I messaggi SNMP contengono unità dati di protocollo (PDU) e altri elementi dell'intestazione del messaggio definiti dalla relativa RFC. Una PDU è un pacchetto di dati che contiene i componenti dei dati SNMP (o i campi).

Il formato di un messaggio SNMP è identico sia per SNMPv1 che per SNMPv2C. Tuttavia, SNMPv2C supporta i tipi PDU aggiuntivi. Supporta, ad esempio, il tipo di richiesta [ \_ \_ GetBulk SNMP PDU](snmp-variable-types-and-request-pdu-types.md) , che consente a un'applicazione di recuperare in modo efficiente blocchi di dati di grandi dimensioni da entità di destinazione.

 

 




