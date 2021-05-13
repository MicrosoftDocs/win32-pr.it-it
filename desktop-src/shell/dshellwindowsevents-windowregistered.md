---
description: Chiamato quando una finestra viene registrata come finestra shell.
title: Metodo DShellWindowsEvents.WindowRegistered
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DShellWindowsEvents.WindowRegistered
api_type:
- COM
api_location:
- Shdocvw.dll
ms.assetid: 7faf758a-daa0-47f5-9f95-61fe3d8286ea
ms.openlocfilehash: 64bf83a88584c5d97994726696d4fb3a1e971bdf
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841452"
---
# <a name="dshellwindowseventswindowregistered-method"></a><span data-ttu-id="b1fc4-103">Metodo DShellWindowsEvents.WindowRegistered</span><span class="sxs-lookup"><span data-stu-id="b1fc4-103">DShellWindowsEvents.WindowRegistered method</span></span>

<span data-ttu-id="b1fc4-104">Chiamato quando una finestra viene registrata come finestra shell.</span><span class="sxs-lookup"><span data-stu-id="b1fc4-104">Called when a window is registered as a Shell window.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1fc4-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b1fc4-105">Syntax</span></span>


```JScript
DShellWindowsEvents.WindowRegistered(
  lCookie
)
```



## <a name="parameters"></a><span data-ttu-id="b1fc4-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b1fc4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1fc4-107">*lCookie* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="b1fc4-107">*lCookie* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1fc4-108">Tipo: **Integer**</span><span class="sxs-lookup"><span data-stu-id="b1fc4-108">Type: **Integer**</span></span>

<span data-ttu-id="b1fc4-109">Cookie che identifica la finestra registrata.</span><span class="sxs-lookup"><span data-stu-id="b1fc4-109">The cookie that identifies the window that was registered.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1fc4-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b1fc4-110">Return value</span></span>

<span data-ttu-id="b1fc4-111">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="b1fc4-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b1fc4-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="b1fc4-112">Remarks</span></span>

<span data-ttu-id="b1fc4-113">A una finestra viene concesso un cookie quando viene registrato come finestra shell.</span><span class="sxs-lookup"><span data-stu-id="b1fc4-113">A window is granted a cookie when it is registered as a Shell window.</span></span> <span data-ttu-id="b1fc4-114">Per altre informazioni, vedere [**Registrare**](/windows/desktop/api/Exdisp/nf-exdisp-ishellwindows-register).</span><span class="sxs-lookup"><span data-stu-id="b1fc4-114">For more information, see [**Register**](/windows/desktop/api/Exdisp/nf-exdisp-ishellwindows-register).</span></span>

## <a name="requirements"></a><span data-ttu-id="b1fc4-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b1fc4-115">Requirements</span></span>



| <span data-ttu-id="b1fc4-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="b1fc4-116">Requirement</span></span> | <span data-ttu-id="b1fc4-117">Valore</span><span class="sxs-lookup"><span data-stu-id="b1fc4-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1fc4-118">Prodotto</span><span class="sxs-lookup"><span data-stu-id="b1fc4-118">Product</span></span><br/> | <span data-ttu-id="b1fc4-119">Internet Explorer 5</span><span class="sxs-lookup"><span data-stu-id="b1fc4-119">Internet Explorer 5</span></span><br/>                                                                                           |
| <span data-ttu-id="b1fc4-120">DLL</span><span class="sxs-lookup"><span data-stu-id="b1fc4-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="b1fc4-121"><dt>Shdocvw.dll (versione 5.00.2014.0216 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="b1fc4-121"><dt>Shdocvw.dll (version 5.00.2014.0216 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1fc4-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b1fc4-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1fc4-123">**DShellWindowsEvents**</span><span class="sxs-lookup"><span data-stu-id="b1fc4-123">**DShellWindowsEvents**</span></span>](dshellwindowsevents.md)
</dt> <dt>

[<span data-ttu-id="b1fc4-124">**WindowRevoked**</span><span class="sxs-lookup"><span data-stu-id="b1fc4-124">**WindowRevoked**</span></span>](dshellwindowsevents-windowrevoked.md)
</dt> <dt>

[<span data-ttu-id="b1fc4-125">**Registrazione**</span><span class="sxs-lookup"><span data-stu-id="b1fc4-125">**Register**</span></span>](/windows/desktop/api/Exdisp/nf-exdisp-ishellwindows-register)
</dt> <dt>

[<span data-ttu-id="b1fc4-126">**RegisterPending**</span><span class="sxs-lookup"><span data-stu-id="b1fc4-126">**RegisterPending**</span></span>](/windows/desktop/api/Exdisp/nf-exdisp-ishellwindows-registerpending)
</dt> </dl>

 

 




