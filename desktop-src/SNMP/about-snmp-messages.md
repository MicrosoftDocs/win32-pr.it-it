---
title: Informazioni sui messaggi SNMP
description: Il Simple Network Management Protocol usa i messaggi per comunicare e scambiare informazioni tra entità SNMP remote.
ms.assetid: 9ba4b854-fc02-40c1-a92f-7c102c900e95
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e90c8e6aba33384ddaf16fbe847f20488f0be4d584c70563a34d052a37e80a23
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009949"
---
# <a name="about-snmp-messages"></a>Informazioni sui messaggi SNMP

Il Simple Network Management Protocol usa i messaggi per comunicare e scambiare informazioni tra entità SNMP remote. I messaggi SNMP contengono unità dati del protocollo (PTU) più elementi di intestazione dei messaggi aggiuntivi definiti dalla RFC pertinente. Una PDU è un pacchetto di dati che contiene componenti di dati SNMP (o campi).

Il formato di un messaggio SNMP è lo stesso sia per SNMPv1 che per SNMPv2C. Tuttavia, SNMPv2C supporta tipi di PDU aggiuntivi. Ad esempio, supporta il tipo di richiesta [SNMP \_ PDU \_ GETBULK,](snmp-variable-types-and-request-pdu-types.md) che consente a un'applicazione di recuperare in modo efficiente grandi blocchi di dati dalle entità di destinazione.

 

 




