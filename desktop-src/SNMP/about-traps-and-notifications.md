---
title: Informazioni su trap e notifiche
description: Un tipo di messaggio che un'applicazione dell'agente SNMP può inviare a un'applicazione WinSNMP è un messaggio asincrono che informa l'applicazione di un evento significativo.
ms.assetid: 5249c5a5-9260-4a67-b00f-a12214012bb3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2bacc6a92de2cb5a12aaf09f5caa629f28338f9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856193"
---
# <a name="about-traps-and-notifications"></a><span data-ttu-id="c89f3-103">Informazioni su trap e notifiche</span><span class="sxs-lookup"><span data-stu-id="c89f3-103">About Traps and Notifications</span></span>

<span data-ttu-id="c89f3-104">Un tipo di messaggio che un'applicazione dell'agente SNMP può inviare a un'applicazione WinSNMP è un messaggio asincrono che informa l'applicazione di un evento significativo.</span><span class="sxs-lookup"><span data-stu-id="c89f3-104">One type of message an SNMP agent application can send to a WinSNMP application is an asynchronous message that informs the application of a significant event.</span></span> <span data-ttu-id="c89f3-105">Un esempio di un evento significativo è quando un collegamento di rete viene arrestato o quando si verifica un errore di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="c89f3-105">An example of a significant event is when a network link shuts down or when an authentication failure occurs.</span></span>

<span data-ttu-id="c89f3-106">Questi tipi di messaggi sono denominati trap in SNMPv1 e notifiche in SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="c89f3-106">These types of messages are called traps under SNMPv1 and notifications under SNMPv2C.</span></span> <span data-ttu-id="c89f3-107">L'implementazione di Microsoft WinSNMP converte sempre i trap SNMPv1 nel formato SNMPv2C, come definito da RFC 1908.</span><span class="sxs-lookup"><span data-stu-id="c89f3-107">The Microsoft WinSNMP implementation always translates SNMPv1 traps to the SNMPv2C format, as defined by RFC 1908.</span></span>

<span data-ttu-id="c89f3-108">Quando si chiama la funzione [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) per creare una PDU trap, è possibile creare solo una PDU trap SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="c89f3-108">When you call the [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) function to create a trap PDU, you can create only an SNMPv2C trap PDU.</span></span> <span data-ttu-id="c89f3-109">L'unico tipo di Trap PDU che è possibile aggiornare con una chiamata alla funzione [**SnmpSetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) è una PDU trap SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="c89f3-109">The only type of trap PDU you can update with a call to the [**SnmpSetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) function is an SNMPv2C trap PDU.</span></span>

<span data-ttu-id="c89f3-110">Per ulteriori informazioni, vedere gli argomenti seguenti.</span><span class="sxs-lookup"><span data-stu-id="c89f3-110">For more information, see the following topics.</span></span>



| <span data-ttu-id="c89f3-111">Argomento</span><span class="sxs-lookup"><span data-stu-id="c89f3-111">Topic</span></span>                                                                                    | <span data-ttu-id="c89f3-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c89f3-112">Description</span></span> |
|------------------------------------------------------------------------------------------|-------------|
| [<span data-ttu-id="c89f3-113">Conversione di trap da SNMPv1 a SNMPv2C</span><span class="sxs-lookup"><span data-stu-id="c89f3-113">Translating Traps from SNMPv1 to SNMPv2C</span></span>](translating-traps-from-snmpv1-to-snmpv2c.md) |             |
| [<span data-ttu-id="c89f3-114">Formati trap</span><span class="sxs-lookup"><span data-stu-id="c89f3-114">Trap Formats</span></span>](trap-formats.md)                                                         |             |



 

 

 




