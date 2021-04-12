---
description: I dati delle chiamate sono un buffer di dimensioni variabili che può essere usato per accumulare informazioni su una sessione di comunicazione. Queste informazioni diventano disponibili per tutte le applicazioni che possiedono o monitorano la sessione.
ms.assetid: 8b7a674f-ba78-4830-bb20-7fa74e202a1a
title: Dati della chiamata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dedfd44a46518a58f3a3aeaec59326648669cb49
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344761"
---
# <a name="call-data"></a><span data-ttu-id="0c3e2-104">Dati della chiamata</span><span class="sxs-lookup"><span data-stu-id="0c3e2-104">Call Data</span></span>

<span data-ttu-id="0c3e2-105">I dati delle chiamate sono un buffer di dimensioni variabili che può essere usato per accumulare informazioni su una sessione di comunicazione.</span><span class="sxs-lookup"><span data-stu-id="0c3e2-105">Call data is a variably sized buffer that can be used to accumulate information about a communications session.</span></span> <span data-ttu-id="0c3e2-106">Queste informazioni diventano disponibili per tutte le applicazioni che possiedono o monitorano la sessione.</span><span class="sxs-lookup"><span data-stu-id="0c3e2-106">This information becomes available to all applications that own or monitor the session.</span></span>

<span data-ttu-id="0c3e2-107">Ad esempio, il gestore iniziale di una sessione in entrata potrebbe richiedere e immettere le informazioni sull'account client in un buffer dei dati di chiamata, quindi i gestori successivi non dovranno ripetere la richiesta.</span><span class="sxs-lookup"><span data-stu-id="0c3e2-107">For example, the initial handler of an incoming session might request and enter client account information into a call data buffer, and then subsequent handlers would not have to repeat the request.</span></span>

<span data-ttu-id="0c3e2-108">Non tutti i provider di servizi supportano l'utilizzo di queste informazioni.</span><span class="sxs-lookup"><span data-stu-id="0c3e2-108">Not all service providers support use of this information.</span></span>

<span data-ttu-id="0c3e2-109">**TAPI 2. x:** Vedere [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), [**lineSetCallData**](/windows/win32/api/tapi/nf-tapi-linesetcalldata) (**dwCallDataSize** e **DwCallDataOffset** members of [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo)), [**line \_ CALLINFO**](./line-callinfo.md) Message (*dwParam1* impostato su LINECALLINFOSTATE \_ CALLDATA).</span><span class="sxs-lookup"><span data-stu-id="0c3e2-109">**TAPI 2.x:** See [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), [**lineSetCallData**](/windows/win32/api/tapi/nf-tapi-linesetcalldata) (**dwCallDataSize** and **dwCallDataOffset** members of [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo)), [**LINE\_CALLINFO**](./line-callinfo.md) message (*dwParam1* set to LINECALLINFOSTATE\_CALLDATA).</span></span>

<span data-ttu-id="0c3e2-110">**TAPI 3. x:** Vedere [**ITCallInfo::p UT \_ CallInfoBuffer**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-put_callinfobuffer) (**CIB \_ CALLDATABUFFER** member of [**CALLINFO \_ buffer**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_buffer)); [**ITCallInfoChangeEvent:: Get \_ La cause**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfochangeevent-get_cause) restituisce il membro **\_ CALLDATA di CIC** di [**CALLINFOCHANGE \_**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfochange_cause).</span><span class="sxs-lookup"><span data-stu-id="0c3e2-110">**TAPI 3.x:** See [**ITCallInfo::put\_CallInfoBuffer**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-put_callinfobuffer) (**CIB\_CALLDATABUFFER** member of [**CALLINFO\_BUFFER**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_buffer)); [**ITCallInfoChangeEvent::get\_Cause**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfochangeevent-get_cause) returns the **CIC\_CALLDATA** member of [**CALLINFOCHANGE\_CAUSE**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfochange_cause).</span></span>

 

 
