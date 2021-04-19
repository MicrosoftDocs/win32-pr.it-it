---
description: I buffer specifici del dispositivo possono far parte di un'implementazione dei provider di servizi di operazioni estese. Il provider di servizi definisce il significato di questi buffer.
ms.assetid: 5783f892-ec11-4340-afad-44f2ef55fd18
title: Buffer specifico del dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 628ee93e4f88fc733e744b3c52af3c0a1c31ecf3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311906"
---
# <a name="device-specific-buffer"></a><span data-ttu-id="1d1d5-104">Buffer specifico del dispositivo</span><span class="sxs-lookup"><span data-stu-id="1d1d5-104">Device-specific Buffer</span></span>

<span data-ttu-id="1d1d5-105">I buffer specifici del dispositivo possono far parte dell'implementazione di un provider di servizi di operazioni estese.</span><span class="sxs-lookup"><span data-stu-id="1d1d5-105">Device-specific buffers may be part of a service provider's implementation of extended operations.</span></span> <span data-ttu-id="1d1d5-106">Il provider di servizi definisce il significato di questi buffer.</span><span class="sxs-lookup"><span data-stu-id="1d1d5-106">The service provider defines the meaning of these buffers.</span></span>

<span data-ttu-id="1d1d5-107">Non tutti i provider di servizi supportano l'utilizzo di queste informazioni.</span><span class="sxs-lookup"><span data-stu-id="1d1d5-107">Not all service providers support use of this information.</span></span>

<span data-ttu-id="1d1d5-108">**TAPI 2. x:** Vedere [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (**dwDevSpecificSize** and **dwDevSpecificOffset** members of [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo)).</span><span class="sxs-lookup"><span data-stu-id="1d1d5-108">**TAPI 2.x:** See [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (**dwDevSpecificSize** and **dwDevSpecificOffset** members of [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo)).</span></span>

<span data-ttu-id="1d1d5-109">**TAPI 3. x:** Vedere [**ITCallInfo:: GetCallInfoBuffer**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-getcallinfobuffer) (membro **CIB \_ DEVSPECIFICBUFFER** del [**\_ buffer CALLINFO**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_buffer)).</span><span class="sxs-lookup"><span data-stu-id="1d1d5-109">**TAPI 3.x:** See [**ITCallInfo::GetCallInfoBuffer**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-getcallinfobuffer) (**CIB\_DEVSPECIFICBUFFER** member of [**CALLINFO\_BUFFER**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_buffer)).</span></span>

 

 
