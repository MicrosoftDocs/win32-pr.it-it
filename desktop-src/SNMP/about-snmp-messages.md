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
# <a name="about-snmp-messages"></a><span data-ttu-id="fc83a-103">Informazioni sui messaggi SNMP</span><span class="sxs-lookup"><span data-stu-id="fc83a-103">About SNMP Messages</span></span>

<span data-ttu-id="fc83a-104">Il Simple Network Management Protocol utilizza messaggi per comunicare e scambiare informazioni tra entità SNMP remote.</span><span class="sxs-lookup"><span data-stu-id="fc83a-104">The Simple Network Management Protocol uses messages to communicate and exchange information between remote SNMP entities.</span></span> <span data-ttu-id="fc83a-105">I messaggi SNMP contengono unità dati di protocollo (PDU) e altri elementi dell'intestazione del messaggio definiti dalla relativa RFC.</span><span class="sxs-lookup"><span data-stu-id="fc83a-105">SNMP messages contain protocol data units (PDUs) plus additional message header elements defined by the relevant RFC.</span></span> <span data-ttu-id="fc83a-106">Una PDU è un pacchetto di dati che contiene i componenti dei dati SNMP (o i campi).</span><span class="sxs-lookup"><span data-stu-id="fc83a-106">A PDU is a data packet that contains SNMP data components (or fields).</span></span>

<span data-ttu-id="fc83a-107">Il formato di un messaggio SNMP è identico sia per SNMPv1 che per SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="fc83a-107">The format of an SNMP message is the same for both SNMPv1 and SNMPv2C.</span></span> <span data-ttu-id="fc83a-108">Tuttavia, SNMPv2C supporta i tipi PDU aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="fc83a-108">However, SNMPv2C supports additional PDU types.</span></span> <span data-ttu-id="fc83a-109">Supporta, ad esempio, il tipo di richiesta [ \_ \_ GetBulk SNMP PDU](snmp-variable-types-and-request-pdu-types.md) , che consente a un'applicazione di recuperare in modo efficiente blocchi di dati di grandi dimensioni da entità di destinazione.</span><span class="sxs-lookup"><span data-stu-id="fc83a-109">For example, it supports the [SNMP\_PDU\_GETBULK](snmp-variable-types-and-request-pdu-types.md) request type, which enables an application to efficiently retrieve large blocks of data from target entities.</span></span>

 

 




