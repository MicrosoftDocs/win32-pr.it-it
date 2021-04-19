---
description: Quando un'applicazione reindirizza una sessione, TAPI mantiene le informazioni di identificazione sul percorso che ha reindirizzato la sessione e il percorso a cui è stato reindirizzato.
ms.assetid: 08484b38-7c97-4acc-921e-0f566b2d3415
title: Identificazione Reindirizzamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8316b7d1566a24ead21f7b1fdf2d16b1c48a2b15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319879"
---
# <a name="redirect-identification"></a><span data-ttu-id="2ba63-103">Identificazione Reindirizzamento</span><span class="sxs-lookup"><span data-stu-id="2ba63-103">Redirect Identification</span></span>

<span data-ttu-id="2ba63-104">Quando un'applicazione [reindirizza](redirect-ovr.md) una sessione, TAPI mantiene le informazioni di identificazione sul percorso che ha reindirizzato la sessione e il percorso a cui è stato reindirizzato.</span><span class="sxs-lookup"><span data-stu-id="2ba63-104">When an application [redirects](redirect-ovr.md) a session, TAPI retains identification information about the location that redirected the session and the location to which it was redirected.</span></span>

<span data-ttu-id="2ba63-105">"Reindirizzamento" si riferisce al percorso che ha richiamato l'operazione di reindirizzamento.</span><span class="sxs-lookup"><span data-stu-id="2ba63-105">"Redirecting" refers to the location that invoked the redirect operation.</span></span> <span data-ttu-id="2ba63-106">"Reindirizzamento" identifica la nuova destinazione per la sessione.</span><span class="sxs-lookup"><span data-stu-id="2ba63-106">"Redirection" identifies the new destination for the session.</span></span>

<span data-ttu-id="2ba63-107">Non tutti i provider di servizi supportano l'utilizzo di queste informazioni.</span><span class="sxs-lookup"><span data-stu-id="2ba63-107">Not all service providers support use of this information.</span></span>

<span data-ttu-id="2ba63-108">\* \* TAPI 2. x: \* \*[**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **dwRedirectionIDSize**, **dwRedirectionIDOffset**, **dwRedirectionIDNameSize**, **dwRedirectionIDNameOffset**, **dwRedirectingIDSize**, **dwRedirectingIDOffset**, **dwRedirectingIDNameSize** e **dwRedirectingIDNameOffset** membri di [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo)</span><span class="sxs-lookup"><span data-stu-id="2ba63-108">\*\*TAPI 2.x:  \*\*[**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **dwRedirectionIDSize**, **dwRedirectionIDOffset**, **dwRedirectionIDNameSize**, **dwRedirectionIDNameOffset**, **dwRedirectingIDSize**, **dwRedirectingIDOffset**, **dwRedirectingIDNameSize**, and **dwRedirectingIDNameOffset** members of [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo)</span></span>

<span data-ttu-id="2ba63-109">\* \* TAPI 3. x: \* \*[**ITCallInfo:: Get \_ CallInfoString**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfostring)called with **the CIS \_ REDIRECTIONIDNAME**, **CIS \_ REDIRECTIONIDNUMBER**, **CIS \_ REDIRECTINGIDNAME** o **CIS \_ REDIRECTINGIDNUMBER** member of [**CALLINFO \_ String**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_string)</span><span class="sxs-lookup"><span data-stu-id="2ba63-109">\*\*TAPI 3.x:  \*\*[**ITCallInfo::get\_CallInfoString**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfostring)called with the **CIS\_REDIRECTIONIDNAME**, **CIS\_REDIRECTIONIDNUMBER**, **CIS\_REDIRECTINGIDNAME**, or **CIS\_REDIRECTINGIDNUMBER** member of [**CALLINFO\_STRING**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_string)</span></span>

 

 
