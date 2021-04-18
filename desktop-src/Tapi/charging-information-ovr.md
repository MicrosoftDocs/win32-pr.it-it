---
description: Le informazioni di ricarica sono specifiche dello standard ISDN Q. 931. Per informazioni sul significato e sull'uso di questi dati, fare riferimento alla documentazione del provider di servizi.
ms.assetid: 5032e2cb-486a-4667-9873-bf88365f12cf
title: Informazioni di ricarica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14d988ec34e901a94e27156f321436b59714cffb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308314"
---
# <a name="charging-information"></a><span data-ttu-id="86746-104">Informazioni di ricarica</span><span class="sxs-lookup"><span data-stu-id="86746-104">Charging Information</span></span>

<span data-ttu-id="86746-105">Le informazioni di ricarica sono specifiche dello standard ISDN Q. 931.</span><span class="sxs-lookup"><span data-stu-id="86746-105">Charging information is specific to the ISDN Q.931 standard.</span></span> <span data-ttu-id="86746-106">Per informazioni sul significato e sull'uso di questi dati, vedere la documentazione del provider di servizi.</span><span class="sxs-lookup"><span data-stu-id="86746-106">Please refer to your service provider's documentation on the meaning and use of this data.</span></span>

<span data-ttu-id="86746-107">Non tutti i provider di servizi supportano l'utilizzo di queste informazioni.</span><span class="sxs-lookup"><span data-stu-id="86746-107">Not all service providers support use of this information.</span></span>

<span data-ttu-id="86746-108">**TAPI 2. x:** Vedere [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (**dwChargingInfoSize** and **dwChargingInfoOffset** members of *lpCallInfo*).</span><span class="sxs-lookup"><span data-stu-id="86746-108">**TAPI 2.x:** See [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (**dwChargingInfoSize** and **dwChargingInfoOffset** members of *lpCallInfo*).</span></span>

<span data-ttu-id="86746-109">**TAPI 3. x:** Vedere [**ITCallInfo:: Get \_ CallInfoBuffer**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfobuffer) (**CIB \_ CHARGINGINFOBUFFER** member of [**CALLINFO \_ buffer**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_buffer)).</span><span class="sxs-lookup"><span data-stu-id="86746-109">**TAPI 3.x:** See [**ITCallInfo::get\_CallInfoBuffer**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfobuffer) (**CIB\_CHARGINGINFOBUFFER** member of [**CALLINFO\_BUFFER**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_buffer)).</span></span>

 

 
