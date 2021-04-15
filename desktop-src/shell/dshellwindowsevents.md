---
description: Riceve gli eventi di registrazione della finestra IShellWindows.
ms.assetid: c340296d-f8eb-43a1-809d-912ea7412fe2
title: Oggetto DShellWindowsEvents (Exdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DShellWindowsEvents
api_type:
- COM
api_location:
- Shdocvw.dll
ms.openlocfilehash: 7df1571556b5f2942f181b4c88b22ff3bc83f273
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "104983014"
---
# <a name="dshellwindowsevents-object"></a><span data-ttu-id="9ca03-103">Oggetto DShellWindowsEvents</span><span class="sxs-lookup"><span data-stu-id="9ca03-103">DShellWindowsEvents object</span></span>

<span data-ttu-id="9ca03-104">Riceve gli eventi di registrazione della finestra [**ishellwindows**](/windows/desktop/api/Exdisp/nn-exdisp-ishellwindows) .</span><span class="sxs-lookup"><span data-stu-id="9ca03-104">Receives [**IShellWindows**](/windows/desktop/api/Exdisp/nn-exdisp-ishellwindows) window registration events.</span></span>

## <a name="members"></a><span data-ttu-id="9ca03-105">Membri</span><span class="sxs-lookup"><span data-stu-id="9ca03-105">Members</span></span>

<span data-ttu-id="9ca03-106">L'oggetto **dshellwindowsevents** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="9ca03-106">The **DShellWindowsEvents** object has these types of members:</span></span>

-   [<span data-ttu-id="9ca03-107">Metodi</span><span class="sxs-lookup"><span data-stu-id="9ca03-107">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="9ca03-108">Metodi</span><span class="sxs-lookup"><span data-stu-id="9ca03-108">Methods</span></span>

<span data-ttu-id="9ca03-109">L'oggetto **dshellwindowsevents** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="9ca03-109">The **DShellWindowsEvents** object has these methods.</span></span>



| <span data-ttu-id="9ca03-110">Metodo</span><span class="sxs-lookup"><span data-stu-id="9ca03-110">Method</span></span>                                                           | <span data-ttu-id="9ca03-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9ca03-111">Description</span></span>                                                       |
|:-----------------------------------------------------------------|:------------------------------------------------------------------|
| [<span data-ttu-id="9ca03-112">**WindowRegistered**</span><span class="sxs-lookup"><span data-stu-id="9ca03-112">**WindowRegistered**</span></span>](dshellwindowsevents-windowregistered.md) | <span data-ttu-id="9ca03-113">Chiamato quando una finestra viene registrata come finestra della shell.</span><span class="sxs-lookup"><span data-stu-id="9ca03-113">Called when a window is registered as a Shell window.</span></span> <br/> |
| [<span data-ttu-id="9ca03-114">**WindowRevoked**</span><span class="sxs-lookup"><span data-stu-id="9ca03-114">**WindowRevoked**</span></span>](dshellwindowsevents-windowrevoked.md)       | <span data-ttu-id="9ca03-115">Chiamato quando viene revocata la registrazione di una finestra della shell.</span><span class="sxs-lookup"><span data-stu-id="9ca03-115">Called when a Shell window's registration is revoked.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="9ca03-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="9ca03-116">Remarks</span></span>

<span data-ttu-id="9ca03-117">Usare **dshellwindowsevents** per monitorare la registrazione o la revoca di una finestra della shell.</span><span class="sxs-lookup"><span data-stu-id="9ca03-117">Use **DShellWindowsEvents** to monitor when a Shell window is registered or revoked.</span></span> <span data-ttu-id="9ca03-118">Per ulteriori informazioni, vedere [**ishellwindows**](/windows/desktop/api/Exdisp/nn-exdisp-ishellwindows).</span><span class="sxs-lookup"><span data-stu-id="9ca03-118">For more information, see [**IShellWindows**](/windows/desktop/api/Exdisp/nn-exdisp-ishellwindows).</span></span>

## <a name="requirements"></a><span data-ttu-id="9ca03-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9ca03-119">Requirements</span></span>



| <span data-ttu-id="9ca03-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="9ca03-120">Requirement</span></span> | <span data-ttu-id="9ca03-121">Valore</span><span class="sxs-lookup"><span data-stu-id="9ca03-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ca03-122">Prodotto</span><span class="sxs-lookup"><span data-stu-id="9ca03-122">Product</span></span><br/> | <span data-ttu-id="9ca03-123">Internet Explorer 5</span><span class="sxs-lookup"><span data-stu-id="9ca03-123">Internet Explorer 5</span></span><br/>                                                                                           |
| <span data-ttu-id="9ca03-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9ca03-124">Header</span></span><br/>  | <dl> <span data-ttu-id="9ca03-125"><dt>Exdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="9ca03-125"><dt>Exdisp.h</dt></span></span> </dl>                                      |
| <span data-ttu-id="9ca03-126">DLL</span><span class="sxs-lookup"><span data-stu-id="9ca03-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="9ca03-127"><dt>Shdocvw.dll (versione 5.00.2014.0216 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="9ca03-127"><dt>Shdocvw.dll (version 5.00.2014.0216 or later)</dt></span></span> </dl> |
| <span data-ttu-id="9ca03-128">IID</span><span class="sxs-lookup"><span data-stu-id="9ca03-128">IID</span></span><br/>     | <span data-ttu-id="9ca03-129">\_ISHELLWINDOWS IID</span><span class="sxs-lookup"><span data-stu-id="9ca03-129">IID\_IShellWindows</span></span><br/>                                                                                            |



## <a name="see-also"></a><span data-ttu-id="9ca03-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9ca03-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ca03-131">**ShellWindows**</span><span class="sxs-lookup"><span data-stu-id="9ca03-131">**ShellWindows**</span></span>](shellwindows.md)
</dt> </dl>

 

 




