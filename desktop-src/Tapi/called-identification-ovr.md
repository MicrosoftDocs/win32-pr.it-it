---
description: Identificazione chiamata identifica l'indirizzo di destinazione originale per una sessione. In situazioni in cui una sessione è stata reindirizzata, inoltrata o trasferita, questo sarà diverso dall'identificazione connessa.
ms.assetid: a03286eb-83a9-4170-b514-e8899fd04c74
title: Identificazione chiamata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63f862d18fb3deb661cb8379c90a4b3e70caab1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883238"
---
# <a name="called-identification"></a><span data-ttu-id="0eb0d-104">Identificazione chiamata</span><span class="sxs-lookup"><span data-stu-id="0eb0d-104">Called Identification</span></span>

<span data-ttu-id="0eb0d-105">Identificazione chiamata identifica l'indirizzo di destinazione originale per una sessione.</span><span class="sxs-lookup"><span data-stu-id="0eb0d-105">Called identification identifies the original destination address for a session.</span></span> <span data-ttu-id="0eb0d-106">In situazioni in cui una sessione è stata reindirizzata, inoltrata o trasferita, questo sarà diverso dall' [Identificazione connessa](connected-identification-ovr.md).</span><span class="sxs-lookup"><span data-stu-id="0eb0d-106">In situations where a session was redirected, forwarded, or transferred, this will be different than the [connected identification](connected-identification-ovr.md).</span></span>

<span data-ttu-id="0eb0d-107">Non tutti i provider di servizi supportano l'utilizzo di queste informazioni.</span><span class="sxs-lookup"><span data-stu-id="0eb0d-107">Not all service providers support use of this information.</span></span>

<span data-ttu-id="0eb0d-108">**TAPI 2. x:** Vedere [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (**dwCalledIDFlags**, **dwCalledIDSize**, **dwCalledIDOffset**, **dwCalledIDNameSize**, **dwCalledIDNameOffset** e **dwCalledIDAddressType** membri di *lpCallInfo*).</span><span class="sxs-lookup"><span data-stu-id="0eb0d-108">**TAPI 2.x:** See [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (**dwCalledIDFlags**, **dwCalledIDSize**, **dwCalledIDOffset**, **dwCalledIDNameSize**, **dwCalledIDNameOffset**, and **dwCalledIDAddressType** members of *lpCallInfo*).</span></span>

<span data-ttu-id="0eb0d-109">**TAPI 3. x:** Vedere [**ITCallInfo:: Get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) (**CIL \_ CALLEDIDADDRESSTYPE** membro of [**CALLINFO \_ Long**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)), [**ITCallInfo:: Get \_ CallInfoString**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfostring) (**CIS \_ CALLEDIDNAME** e **CIS \_ CALLEDIDNAME** members of [**CALLINFO \_ String**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_string)).</span><span class="sxs-lookup"><span data-stu-id="0eb0d-109">**TAPI 3.x:** See [**ITCallInfo::get\_CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) (**CIL\_CALLEDIDADDRESSTYPE** member of [**CALLINFO\_LONG**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)), [**ITCallInfo::get\_CallInfoString**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfostring) (**CIS\_CALLEDIDNAME** and **CIS\_CALLEDIDNAME** members of [**CALLINFO\_STRING**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_string)).</span></span>

 

 
