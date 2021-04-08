---
description: L'identificazione del chiamante fornisce informazioni sulla parte chiamante quando riceve una sessione in ingresso. In genere, un'applicazione utilizza questi dati come parte di un messaggio di stato per un utente.
ms.assetid: aaaa5eae-e917-44a7-b9c5-97ca2d9a4eec
title: Identificazione del chiamante
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93513e3d94fac9c550b23651b3987bc794905beb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883237"
---
# <a name="caller-identification"></a><span data-ttu-id="b68a8-104">Identificazione del chiamante</span><span class="sxs-lookup"><span data-stu-id="b68a8-104">Caller Identification</span></span>

<span data-ttu-id="b68a8-105">L'identificazione del chiamante fornisce informazioni sulla parte chiamante quando riceve una sessione in ingresso.</span><span class="sxs-lookup"><span data-stu-id="b68a8-105">Caller identification provides information on the calling party when receiving an incoming session.</span></span> <span data-ttu-id="b68a8-106">In genere, un'applicazione utilizza questi dati come parte di un messaggio di stato per un utente.</span><span class="sxs-lookup"><span data-stu-id="b68a8-106">An application typically uses this data as part of a status message to a user.</span></span>

<span data-ttu-id="b68a8-107">Queste informazioni non sono sempre disponibili immediatamente.</span><span class="sxs-lookup"><span data-stu-id="b68a8-107">This information is not always available immediately.</span></span> <span data-ttu-id="b68a8-108">Un'applicazione che vuole usare queste informazioni e ha verificato che il provider di servizi la supporti, deve verificare più volte prima di presumere che le informazioni non siano disponibili.</span><span class="sxs-lookup"><span data-stu-id="b68a8-108">An application that wants to use this information and has verified that the service provider supports it should check several times before assuming that the information is not available.</span></span>

<span data-ttu-id="b68a8-109">Non tutti i provider di servizi supportano l'utilizzo di queste informazioni.</span><span class="sxs-lookup"><span data-stu-id="b68a8-109">Not all service providers support use of this information.</span></span>

<span data-ttu-id="b68a8-110">**TAPI 2. x:** Vedere [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (**dwCallerIDFlags**, **dwCallerIDSize**, **dwCallerIDOffset**, **dwCallerIDNameSize**, **dwCallerIDNameOffset** e **dwCallerIDAddressType** membri di *lpCallInfo*).</span><span class="sxs-lookup"><span data-stu-id="b68a8-110">**TAPI 2.x:** See [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (**dwCallerIDFlags**, **dwCallerIDSize**, **dwCallerIDOffset**, **dwCallerIDNameSize**, **dwCallerIDNameOffset**, and **dwCallerIDAddressType** members of *lpCallInfo*).</span></span>

<span data-ttu-id="b68a8-111">**TAPI 3. x:** Vedere [**ITCallInfo:: Get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) (**CIL \_ CALLERIDADDRESSTYPE** membro of [**CALLINFO \_ Long**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)), [**ITCallInfo:: Get \_ CallInfoString**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfostring) (**CIS \_ CALLERIDNAME** e **CIS \_ CALLERIDNAME** members of [**CALLINFO \_ String**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_string)).</span><span class="sxs-lookup"><span data-stu-id="b68a8-111">**TAPI 3.x:** See [**ITCallInfo::get\_CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) (**CIL\_CALLERIDADDRESSTYPE** member of [**CALLINFO\_LONG**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)), [**ITCallInfo::get\_CallInfoString**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfostring) (**CIS\_CALLERIDNAME** and **CIS\_CALLERIDNAME** members of [**CALLINFO\_STRING**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_string)).</span></span>

 

 
