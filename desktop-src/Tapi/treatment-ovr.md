---
description: Il trattamento si riferisce alla gestione di una sessione in ingresso a cui non è stata ancora fornita una risposta o che è stata messa in attesa, ad esempio la musica. \_Per un elenco di trattamenti definiti da TAPI, vedere costanti LINECALLTREATMENT.
ms.assetid: 0b8d1023-374a-4937-b39c-04043423eb47
title: Modalità di gestione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bbde0e602836b543e849afb3d56c33fd6df0a60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485581"
---
# <a name="treatment"></a><span data-ttu-id="10824-104">Modalità di gestione</span><span class="sxs-lookup"><span data-stu-id="10824-104">Treatment</span></span>

<span data-ttu-id="10824-105">Il trattamento si riferisce alla gestione di una sessione in ingresso a cui non è stata ancora fornita una risposta o che è stata messa in attesa, ad esempio la musica.</span><span class="sxs-lookup"><span data-stu-id="10824-105">Treatment refers to the handling of an incoming session that has not yet been answered or has been put on hold, such as music.</span></span> <span data-ttu-id="10824-106">Per un elenco di trattamenti definiti da TAPI, vedere [ \_ costanti LINECALLTREATMENT](./linecalltreatment--constants.md) .</span><span class="sxs-lookup"><span data-stu-id="10824-106">Please see [LINECALLTREATMENT\_ Constants](./linecalltreatment--constants.md) for a list of treatments defined by TAPI.</span></span>

<span data-ttu-id="10824-107">Non tutti i provider di servizi supportano l'utilizzo di queste informazioni.</span><span class="sxs-lookup"><span data-stu-id="10824-107">Not all service providers support use of this information.</span></span>

<span data-ttu-id="10824-108">**TAPI 2. x: **[**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (** membro dwCallTreatment** di *lpCallInfo*)</span><span class="sxs-lookup"><span data-stu-id="10824-108">**TAPI 2.x:  **[**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (** dwCallTreatment** member of *lpCallInfo*)</span></span>

<span data-ttu-id="10824-109">**TAPI 3. x: **[**ITCallInfo:: Get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) (** membro CIL \_ CALLTREATMENT** di [**CALLINFO \_ Long**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long))</span><span class="sxs-lookup"><span data-stu-id="10824-109">**TAPI 3.x:  **[**ITCallInfo::get\_CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) (** CIL\_CALLTREATMENT** member of [**CALLINFO\_LONG**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long))</span></span>

 

 
