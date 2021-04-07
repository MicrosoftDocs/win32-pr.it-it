---
description: La rete di modalità di trasferimento asincrona (ATM) sta emergendo nel mainstream del computer e il supporto per ATM è stato aggiunto a molte parti del sistema operativo.
ms.assetid: 0ca0ecf3-2b67-4925-a6fc-3edfaad2c0e2
title: Qualità del servizio (API di telefonia)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6525ced0b29d35482244c3c37f8382edbfcb9fd6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884013"
---
# <a name="quality-of-service-telephony-api"></a><span data-ttu-id="48356-103">Qualità del servizio (API di telefonia)</span><span class="sxs-lookup"><span data-stu-id="48356-103">Quality of Service (Telephony API)</span></span>

<span data-ttu-id="48356-104">La rete di modalità di trasferimento asincrona (ATM) sta emergendo nel mainstream del computer e il supporto per ATM è stato aggiunto a molte parti del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="48356-104">Asynchronous Transfer Mode (ATM) networking is emerging into the mainstream of computing, and support for ATM has been added to many parts of the operating system.</span></span> <span data-ttu-id="48356-105">TAPI supporta anche gli attributi chiave per stabilire chiamate sulle funzionalità ATM.</span><span class="sxs-lookup"><span data-stu-id="48356-105">TAPI also supports key attributes of establishing calls on ATM facilities.</span></span> <span data-ttu-id="48356-106">Il più importante di questi aspetti dal punto di vista dell'applicazione è la possibilità di richiedere, negoziare, rinegoziare e ricevere indicazioni sui parametri di qualità del servizio (QOS) sulle chiamate in ingresso e in uscita.</span><span class="sxs-lookup"><span data-stu-id="48356-106">The most important of these from an application perspective is the ability to request, negotiate, renegotiate, and receive indications of Quality of Service (QOS) parameters on incoming and outgoing calls.</span></span>

<span data-ttu-id="48356-107">Le informazioni QOS in TAPI vengono scambiate tra le applicazioni e i provider di servizi in strutture [**FLOWSPEC**](/windows/desktop/api/qos/ns-qos-flowspec) definite in Windows sockets 2,0.</span><span class="sxs-lookup"><span data-stu-id="48356-107">QOS information in TAPI is exchanged between applications and service providers in [**FLOWSPEC**](/windows/desktop/api/qos/ns-qos-flowspec) structures that are defined in Windows Sockets 2.0.</span></span>

<span data-ttu-id="48356-108">Le applicazioni richiedono QOS per le chiamate in uscita impostando i valori delle informazioni di sessione prima di avviare una sessione di comunicazione.</span><span class="sxs-lookup"><span data-stu-id="48356-108">Applications request QOS on outgoing calls by setting session information values prior to starting a communications session.</span></span> <span data-ttu-id="48356-109">Il provider di servizi tenterà di fornire il QOS specificato e non riuscirà a eseguire la chiamata.</span><span class="sxs-lookup"><span data-stu-id="48356-109">The service provider will try to provide the specified QOS, and fail the call if it cannot.</span></span> <span data-ttu-id="48356-110">L'applicazione può quindi modificare i parametri e ripetere la chiamata.</span><span class="sxs-lookup"><span data-stu-id="48356-110">The application can then adjust its parameters and try the call again.</span></span> <span data-ttu-id="48356-111">Dopo che è stata stabilita una chiamata, un'applicazione può richiedere una modifica nel QOS.</span><span class="sxs-lookup"><span data-stu-id="48356-111">After a call is established, an application can request a change in the QOS.</span></span>

<span data-ttu-id="48356-112">TAPI fornisce notifiche degli eventi al proprietario o al monitoraggio delle applicazioni in caso di modifica dei livelli QOS.</span><span class="sxs-lookup"><span data-stu-id="48356-112">TAPI provides event notifications to owner or monitor applications if there is any change in QOS levels.</span></span>

<span data-ttu-id="48356-113">Il supporto per QOS non è limitato ai trasporti ATM; qualsiasi provider di servizi può implementare le funzionalità QOS.</span><span class="sxs-lookup"><span data-stu-id="48356-113">Support for QOS is not restricted to ATM transports; any service provider can implement QOS features.</span></span>

<span data-ttu-id="48356-114">Non tutti i provider di servizi supportano l'utilizzo di queste informazioni.</span><span class="sxs-lookup"><span data-stu-id="48356-114">Not all service providers support use of this information.</span></span>

<span data-ttu-id="48356-115">\* \* TAPI 2. x: \* \*[**lineSetCallQualityOfService**](/windows/win32/api/tapi/nf-tapi-linesetcallqualityofservice), [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **dwSendingFlowspecSize**, **DwSendingFlowspecOffset**, **dwReceivingFlowspecSize** e **dwReceivingFlowspecOffset** membri di [**LINECALLPARAMS**](/windows/win32/api/tapi/ns-tapi-linecallparams)</span><span class="sxs-lookup"><span data-stu-id="48356-115">\*\*TAPI 2.x:  \*\*[**lineSetCallQualityOfService**](/windows/win32/api/tapi/nf-tapi-linesetcallqualityofservice), [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **dwSendingFlowspecSize**, **dwSendingFlowspecOffset**, **dwReceivingFlowspecSize**, and **dwReceivingFlowspecOffset** members of [**LINECALLPARAMS**](/windows/win32/api/tapi/ns-tapi-linecallparams)</span></span>

<span data-ttu-id="48356-116">\* \* TAPI 3. x: \* \*[**ITBasicCallControl:: SetQOS**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-setqos), [**ITQOSEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itqosevent)</span><span class="sxs-lookup"><span data-stu-id="48356-116">\*\*TAPI 3.x:  \*\*[**ITBasicCallControl::SetQOS**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-setqos), [**ITQOSEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itqosevent)</span></span>

 

 
