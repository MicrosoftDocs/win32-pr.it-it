---
title: Assegnazione di identificatori di richiesta
description: Un'applicazione WinSNMP può chiamare la funzione SnmpCreatePdu o la funzione SnmpSetPduData per assegnare un identificatore di richiesta generato dall'applicazione a una PDU. L'applicazione deve passare il valore nel \_ parametro ID richiesta.
ms.assetid: 72559054-982f-4c2b-83d2-268f130f6ea2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 753f0ec1f5f3ca4347b6344aa111b91e735f06ba
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707318"
---
# <a name="assigning-request-identifiers"></a><span data-ttu-id="2e610-104">Assegnazione di identificatori di richiesta</span><span class="sxs-lookup"><span data-stu-id="2e610-104">Assigning Request Identifiers</span></span>

<span data-ttu-id="2e610-105">Un'applicazione WinSNMP può chiamare la funzione [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) o la funzione [**SnmpSetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) per assegnare un identificatore di richiesta generato dall'applicazione a una PDU.</span><span class="sxs-lookup"><span data-stu-id="2e610-105">A WinSNMP application can call the [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) function or the [**SnmpSetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) function to assign an application-generated request identifier to a PDU.</span></span> <span data-ttu-id="2e610-106">L'applicazione deve passare il valore nel parametro *\_ ID richiesta* .</span><span class="sxs-lookup"><span data-stu-id="2e610-106">The application must pass the value in the *request\_id* parameter.</span></span>

<span data-ttu-id="2e610-107">Un'applicazione può richiedere che l'implementazione di Microsoft WinSNMP generi e assegni un identificatore di richiesta a una PDU passando zero nel *parametro \_ ID della richiesta* della funzione [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) .</span><span class="sxs-lookup"><span data-stu-id="2e610-107">An application can request that the Microsoft WinSNMP implementation generate and assign a request identifier to a PDU by passing zero in the *request\_id* parameter of the [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) function.</span></span> <span data-ttu-id="2e610-108">L'applicazione può recuperare l'identificatore della richiesta assegnato con una chiamata alla funzione [**SnmpGetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetpdudata) .</span><span class="sxs-lookup"><span data-stu-id="2e610-108">The application can retrieve the assigned request identifier with a call to the [**SnmpGetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetpdudata) function.</span></span>

<span data-ttu-id="2e610-109">Per assegnare un identificatore della richiesta uguale a un valore specifico, incluso zero, l'applicazione deve passare tale valore nel *parametro \_ ID richiesta* della funzione [**SnmpSetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) .</span><span class="sxs-lookup"><span data-stu-id="2e610-109">To assign a request identifier equal to a specific value, including zero, the application must pass that value in the *request\_id* parameter of the [**SnmpSetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) function.</span></span>

<span data-ttu-id="2e610-110">Quando l'implementazione esegue i criteri di ritrasmissione dell'applicazione, include il campo **\_ ID richiesta** della PDU originale in ogni messaggio SNMP ritrasmesso.</span><span class="sxs-lookup"><span data-stu-id="2e610-110">When the implementation executes the application's retransmission policy, it includes the **request\_id** field of the original PDU in each retransmitted SNMP message.</span></span> <span data-ttu-id="2e610-111">Per ulteriori informazioni, vedere [informazioni sulla ritrasmissione](about-retransmission.md) e [la gestione dei criteri di ritrasmissione](managing-the-retransmission-policy.md).</span><span class="sxs-lookup"><span data-stu-id="2e610-111">For more information, see [About Retransmission](about-retransmission.md) and [Managing the Retransmission Policy](managing-the-retransmission-policy.md).</span></span>

> [!Note]  
> <span data-ttu-id="2e610-112">Quando l'implementazione riceve trap da un'entità SNMPv1, assegna un valore diverso da zero al campo **\_ ID richiesta** della PDU.</span><span class="sxs-lookup"><span data-stu-id="2e610-112">When the implementation receives traps from an SNMPv1 entity, it assigns a non-zero value to the **request\_id** field of the PDU.</span></span> <span data-ttu-id="2e610-113">Questo valore può duplicare un identificatore di richiesta utilizzato dall'applicazione in un PDU della richiesta.</span><span class="sxs-lookup"><span data-stu-id="2e610-113">This value may duplicate a request identifier used by the application in a request PDU.</span></span> <span data-ttu-id="2e610-114">Le applicazioni devono verificare la duplicazione.</span><span class="sxs-lookup"><span data-stu-id="2e610-114">Applications must check for duplication.</span></span>

 

 

 




