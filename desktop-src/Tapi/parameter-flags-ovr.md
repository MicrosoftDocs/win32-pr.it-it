---
description: I flag di parametro forniscono informazioni su diversi flag di stato relativi a una sessione di comunicazione, ad esempio se l'identificazione del chiamante deve essere bloccata. \_Per un elenco di flag definiti da TAPI, vedere costanti LINECALLPARAMFLAGS.
ms.assetid: 30511328-a310-42b7-a81e-3ef2abf586ed
title: Flag di parametro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3adcb8b430045dc41afea4e7f55e5fa4458530b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311886"
---
# <a name="parameter-flags"></a><span data-ttu-id="0f304-104">Flag di parametro</span><span class="sxs-lookup"><span data-stu-id="0f304-104">Parameter Flags</span></span>

<span data-ttu-id="0f304-105">I flag di parametro forniscono informazioni su diversi flag di stato relativi a una sessione di comunicazione, ad esempio se l'identificazione del chiamante deve essere bloccata.</span><span class="sxs-lookup"><span data-stu-id="0f304-105">Parameter flags supply information on a variety of status flags concerning a communications session, such as whether caller identification should be blocked.</span></span> <span data-ttu-id="0f304-106">Per un elenco di flag definiti da TAPI, vedere [ \_ costanti LINECALLPARAMFLAGS](./linecallparamflags--constants.md) .</span><span class="sxs-lookup"><span data-stu-id="0f304-106">See [LINECALLPARAMFLAGS\_ Constants](./linecallparamflags--constants.md) for a list of flags defined by TAPI.</span></span>

<span data-ttu-id="0f304-107">Non tutti i provider di servizi supportano l'utilizzo di queste informazioni.</span><span class="sxs-lookup"><span data-stu-id="0f304-107">Not all service providers support use of this information.</span></span>

<span data-ttu-id="0f304-108">**TAPI 2. x:** Vedere [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (membro **dwCallParamFlags** di *lpCallInfo*).</span><span class="sxs-lookup"><span data-stu-id="0f304-108">**TAPI 2.x:** See [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (**dwCallParamFlags** member of *lpCallInfo*).</span></span>

<span data-ttu-id="0f304-109">**TAPI 3. x:** Vedere [**ITCallInfo:: Get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) (**CIL \_ CALLPARAMSFLAGS** member of [**CALLINFO \_ Long**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)).</span><span class="sxs-lookup"><span data-stu-id="0f304-109">**TAPI 3.x:** See [**ITCallInfo::get\_CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) (**CIL\_CALLPARAMSFLAGS** member of [**CALLINFO\_LONG**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)).</span></span>

 

 
