---
description: Le possibili cause di una sessione in ingresso, ad esempio quella di trasferimento, sono elencate nelle \_ costanti LINECALLREASON.
ms.assetid: 94cc1a79-7ce4-47ec-bdd8-ee7f0d9f48ed
title: Motivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79b3bfbbaded05853b447d1291a150113c75bbc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316026"
---
# <a name="reason"></a><span data-ttu-id="96d9e-103">Motivo</span><span class="sxs-lookup"><span data-stu-id="96d9e-103">Reason</span></span>

<span data-ttu-id="96d9e-104">Le possibili cause di una sessione in ingresso, ad esempio quella di trasferimento, sono elencate nelle [ \_ costanti LINECALLREASON](./linecallreason--constants.md).</span><span class="sxs-lookup"><span data-stu-id="96d9e-104">The possible reasons for an incoming session, such as that it was transferred, are listed in the [LINECALLREASON\_ Constants](./linecallreason--constants.md).</span></span>

<span data-ttu-id="96d9e-105">Non tutti i provider di servizi supportano l'utilizzo di queste informazioni.</span><span class="sxs-lookup"><span data-stu-id="96d9e-105">Not all service providers support use of this information.</span></span>

<span data-ttu-id="96d9e-106">**TAPI 2. x: **[**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (** membro dwReason** di *lpCallInfo*)</span><span class="sxs-lookup"><span data-stu-id="96d9e-106">**TAPI 2.x:  **[**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (** dwReason** member of *lpCallInfo*)</span></span>

<span data-ttu-id="96d9e-107">**TAPI 3. x: **[**ITCallInfo:: Get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) (** membro del \_ motivo CIL** di [**CALLINFO \_ Long**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long))</span><span class="sxs-lookup"><span data-stu-id="96d9e-107">**TAPI 3.x:  **[**ITCallInfo::get\_CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) (** CIL\_REASON** member of [**CALLINFO\_LONG**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long))</span></span>

 

 
