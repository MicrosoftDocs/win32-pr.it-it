---
description: Il buffer di compatibilità è specifico dello standard ISDN Q. 931. Per informazioni sul significato e sull'uso di questi dati, fare riferimento alla documentazione del provider di servizi.
ms.assetid: c4c87ca8-fbae-4275-9b69-7b32daf4c18f
title: Buffer di compatibilità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8669e32cd47978c10e2f5abdbe076bcf08ba1862
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308311"
---
# <a name="compatibility-buffer"></a><span data-ttu-id="dbda4-104">Buffer di compatibilità</span><span class="sxs-lookup"><span data-stu-id="dbda4-104">Compatibility Buffer</span></span>

<span data-ttu-id="dbda4-105">Il buffer di compatibilità è specifico dello standard ISDN Q. 931.</span><span class="sxs-lookup"><span data-stu-id="dbda4-105">The compatibility buffer is specific to the ISDN Q.931 standard.</span></span> <span data-ttu-id="dbda4-106">Per informazioni sul significato e sull'uso di questi dati, vedere la documentazione del provider di servizi.</span><span class="sxs-lookup"><span data-stu-id="dbda4-106">Please refer to your service provider's documentation on the meaning and use of this data.</span></span>

<span data-ttu-id="dbda4-107">Non tutti i provider di servizi supportano l'utilizzo di queste informazioni.</span><span class="sxs-lookup"><span data-stu-id="dbda4-107">Not all service providers support use of this information.</span></span>

<span data-ttu-id="dbda4-108">**TAPI 2. x:** Vedere [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (**dwHighLevelCompSize**, **dwHighLevelCompOffset**, **dwLowLevelCompSize** e **dwLowLevelCompOffset** membri di *lpCallInfo*).</span><span class="sxs-lookup"><span data-stu-id="dbda4-108">**TAPI 2.x:** See [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (**dwHighLevelCompSize**, **dwHighLevelCompOffset**, **dwLowLevelCompSize**, and **dwLowLevelCompOffset** members of *lpCallInfo*).</span></span>

<span data-ttu-id="dbda4-109">**TAPI 3. x:** Vedere [**ITCallInfo:: Get \_ CallInfoBuffer**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfobuffer) (**CIB \_ HIGHLEVELCOMPATIBILITYBUFFER** e **CIB \_** LOWLEVELCOMPATIBILITYBUFFER member of [**CALLINFO \_ buffer**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_buffer)).</span><span class="sxs-lookup"><span data-stu-id="dbda4-109">**TAPI 3.x:** See [**ITCallInfo::get\_CallInfoBuffer**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfobuffer) (**CIB\_HIGHLEVELCOMPATIBILITYBUFFER** and **CIB\_LOWLEVELCOMPATIBILITYBUFFER** member of [**CALLINFO\_BUFFER**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_buffer)).</span></span>

 

 
