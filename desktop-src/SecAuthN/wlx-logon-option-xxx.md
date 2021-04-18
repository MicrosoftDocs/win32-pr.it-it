---
description: I valori vengono usati dal parametro dwOptions di WlxLoggedOutSAS.
ms.assetid: a146427b-f3f1-4221-b2eb-ee7da451314a
title: WLX_LOGON_OPTION_XXX (Winwlx. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fa8909f562b87eb3a8147b0684d9676b9ac55d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347136"
---
# <a name="wlx_logon_option_xxx"></a><span data-ttu-id="7814b-103">\_opzione di accesso wlx \_ \_ xxx</span><span class="sxs-lookup"><span data-stu-id="7814b-103">WLX\_LOGON\_OPTION\_XXX</span></span>

<span data-ttu-id="7814b-104">\[L' \_ \_ opzione di accesso wlx \_ xxx Constant non è più disponibile per l'uso a partire da Windows Server 2008 e Windows Vista.\]</span><span class="sxs-lookup"><span data-stu-id="7814b-104">\[The WLX\_LOGON\_OPTION\_XXX constant is no longer available for use as of Windows Server 2008 and Windows Vista.\]</span></span>

<span data-ttu-id="7814b-105">I **valori \_ \_ \_ xxx dell'opzione di accesso wlx** vengono usati dal parametro *dwOptions* di [**WlxLoggedOutSAS**](/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedoutsas).</span><span class="sxs-lookup"><span data-stu-id="7814b-105">The **WLX\_LOGON\_OPTION\_XXX** values are used by the *dwOptions* parameter of [**WlxLoggedOutSAS**](/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedoutsas).</span></span>

> [!Note]  
> <span data-ttu-id="7814b-106">Le DLL GINA vengono ignorate in Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="7814b-106">GINA DLLs are ignored in Windows Vista.</span></span>

 

<span data-ttu-id="7814b-107">Una volta eseguito correttamente l'accesso, la DLL GINA può usare questo valore per specificare l'opzione seguente.</span><span class="sxs-lookup"><span data-stu-id="7814b-107">Upon a successful logon, your GINA DLL can use this value to specify the following option.</span></span>



| <span data-ttu-id="7814b-108">Costante</span><span class="sxs-lookup"><span data-stu-id="7814b-108">Constant</span></span>                                                                                                                                                                                          | <span data-ttu-id="7814b-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7814b-109">Description</span></span>                                                                                                                                                                      |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WLX_LOGON_OPT_NO_PROFILE"></span><span id="wlx_logon_opt_no_profile"></span><dl> <span data-ttu-id="7814b-110"><dt>**\_ \_ \_ nessun profilo di accesso \_ a wlx**</dt></span><span class="sxs-lookup"><span data-stu-id="7814b-110"><dt>**WLX\_LOGON\_OPT\_NO\_PROFILE**</dt></span></span> </dl> | <span data-ttu-id="7814b-111">Specifica che Winlogon non deve caricare un profilo per l'utente connesso.</span><span class="sxs-lookup"><span data-stu-id="7814b-111">Specifies that Winlogon must not load a profile for the logged-on user.</span></span> <span data-ttu-id="7814b-112">In questo caso, la DLL GINA caricherà il profilo o l'utente non necessita di un profilo.</span><span class="sxs-lookup"><span data-stu-id="7814b-112">In this case, either your GINA DLL will load the profile or the user does not need a profile.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="7814b-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7814b-113">Requirements</span></span>



| <span data-ttu-id="7814b-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="7814b-114">Requirement</span></span> | <span data-ttu-id="7814b-115">Valore</span><span class="sxs-lookup"><span data-stu-id="7814b-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="7814b-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7814b-116">Minimum supported client</span></span><br/> | <span data-ttu-id="7814b-117">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="7814b-117">Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="7814b-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7814b-118">Minimum supported server</span></span><br/> | <span data-ttu-id="7814b-119">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7814b-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="7814b-120">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="7814b-120">End of client support</span></span><br/>    | <span data-ttu-id="7814b-121">Windows XP</span><span class="sxs-lookup"><span data-stu-id="7814b-121">Windows XP</span></span><br/>                                                               |
| <span data-ttu-id="7814b-122">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="7814b-122">End of server support</span></span><br/>    | <span data-ttu-id="7814b-123">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7814b-123">Windows Server 2003</span></span><br/>                                                      |
| <span data-ttu-id="7814b-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7814b-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="7814b-125"><dt>Winwlx. h</dt></span><span class="sxs-lookup"><span data-stu-id="7814b-125"><dt>Winwlx.h</dt></span></span> </dl> |



 

 




