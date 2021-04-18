---
description: L'ID di chiamata differisce dall'identificatore di sessione in due modi principali a cui il provider di servizi lo assegna ed è lo stesso per tutte le applicazioni che gestiscono la sessione.
ms.assetid: c9d0d43b-3053-4e3e-b442-57942f3448df
title: ID chiamata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef571b55f653cb9c7bc1d61cdc8a3f71e91ba8f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312732"
---
# <a name="call-id"></a><span data-ttu-id="508cf-103">ID chiamata</span><span class="sxs-lookup"><span data-stu-id="508cf-103">Call ID</span></span>

<span data-ttu-id="508cf-104">L'ID di chiamata differisce dall' [identificatore di sessione](session-identifier-ovr.md) in due modi principali: il provider di servizi lo assegna ed è lo stesso per tutte le applicazioni che gestiscono la sessione.</span><span class="sxs-lookup"><span data-stu-id="508cf-104">The Call ID differs from the [Session Identifier](session-identifier-ovr.md) in two primary ways: the service provider assigns it, and it is the same for every application that handles the session.</span></span> <span data-ttu-id="508cf-105">Non può essere usato per la comunicazione ordinaria con TAPI per le operazioni di sessione perché non corrisponde a una particolare applicazione.</span><span class="sxs-lookup"><span data-stu-id="508cf-105">It cannot be used for ordinary communication with TAPI concerning session operations because it does not match to a particular application.</span></span>

<span data-ttu-id="508cf-106">L'ID chiamata viene usato nelle operazioni, ad esempio determinare se un gruppo di ID di sessione fa effettivamente riferimento a una chiamata, come nel caso di una conferenza o per le comunicazioni con un'altra applicazione.</span><span class="sxs-lookup"><span data-stu-id="508cf-106">The Call ID is used in operations such as determining whether a group of session IDs actually refer to one call, as is the case for a conference, or for communications with another application.</span></span>

<span data-ttu-id="508cf-107">Non tutti i provider di servizi supportano l'utilizzo di queste informazioni.</span><span class="sxs-lookup"><span data-stu-id="508cf-107">Not all service providers support use of this information.</span></span>

<span data-ttu-id="508cf-108">**TAPI 2. x:** Vedere [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (membro **dwCallID** di [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo)).</span><span class="sxs-lookup"><span data-stu-id="508cf-108">**TAPI 2.x:** See [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (**dwCallID** member of [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo)).</span></span>

<span data-ttu-id="508cf-109">**TAPI 3. x:** Vedere [**ITCallInfo:: Get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) (**CIL \_ CALLID** member of [**CALLINFO \_ Long**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)).</span><span class="sxs-lookup"><span data-stu-id="508cf-109">**TAPI 3.x:** See [**ITCallInfo::get\_CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) (**CIL\_CALLID** member of [**CALLINFO\_LONG**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)).</span></span>

 

 
