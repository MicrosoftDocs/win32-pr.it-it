---
description: Le informazioni specifiche dell'applicazione consentono alle applicazioni di passare le altre informazioni relative a una sessione tramite TAPI. Queste informazioni non vengono interpretate da TAPI e l'utilizzo è interamente definito dalle applicazioni.
ms.assetid: e72e4164-3578-4e18-aea0-09d47d385b57
title: Informazioni specifiche dell'applicazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bf4a10413f914eb0bb2da763022f1946811ce12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319885"
---
# <a name="application-specific-information"></a><span data-ttu-id="7eda4-104">Informazioni specifiche dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="7eda4-104">Application-specific Information</span></span>

<span data-ttu-id="7eda4-105">Le informazioni specifiche dell'applicazione consentono alle applicazioni di passare le altre informazioni relative a una sessione tramite TAPI.</span><span class="sxs-lookup"><span data-stu-id="7eda4-105">Application-specific information allows applications to pass each other information concerning a session through TAPI.</span></span> <span data-ttu-id="7eda4-106">Queste informazioni non vengono interpretate da TAPI e l'utilizzo è interamente definito dalle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="7eda4-106">This information is not interpreted by TAPI and usage is entirely defined by the applications.</span></span>

<span data-ttu-id="7eda4-107">Quando le informazioni specifiche dell'applicazione vengono modificate da un'applicazione, TAPI invia tutte le altre applicazioni con privilegi di monitoraggio o di proprietario nella sessione, un evento che indica che si è verificata una modifica.</span><span class="sxs-lookup"><span data-stu-id="7eda4-107">When application-specific information is changed by one application, TAPI sends all other applications with monitor or owner privileges on the session an event indicating that a change has occurred.</span></span>

<span data-ttu-id="7eda4-108">Non tutti i provider di servizi supportano l'utilizzo di queste informazioni.</span><span class="sxs-lookup"><span data-stu-id="7eda4-108">Not all service providers support use of this information.</span></span>

<span data-ttu-id="7eda4-109">**TAPI 2. x:** Vedere [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (membro *dwAppSpecific* di *lpCallInfo*), [**lineSetAppSpecific**](/windows/win32/api/tapi/nf-tapi-linesetappspecific), [**riga \_ CALLINFO**](./line-callinfo.md) Message (*dwParam1* impostato su LINECALLINFOSTATE \_ APPSPECIFIC).</span><span class="sxs-lookup"><span data-stu-id="7eda4-109">**TAPI 2.x:** See [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (*dwAppSpecific* member of *lpCallInfo*), [**lineSetAppSpecific**](/windows/win32/api/tapi/nf-tapi-linesetappspecific), [**LINE\_CALLINFO**](./line-callinfo.md) message (*dwParam1* set to LINECALLINFOSTATE\_APPSPECIFIC).</span></span>

<span data-ttu-id="7eda4-110">**TAPI 3. x:** Vedere [**ITCallInfo:: Get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong), [**ITCallInfo::p UT \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-put_callinfolong) (**CIL \_ APPSPECIFIC** membro of [**CALLINFO \_ Long**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)).</span><span class="sxs-lookup"><span data-stu-id="7eda4-110">**TAPI 3.x:** See [**ITCallInfo::get\_CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong), [**ITCallInfo::put\_CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-put_callinfolong) (**CIL\_APPSPECIFIC** member of [**CALLINFO\_LONG**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)).</span></span>

 

 
