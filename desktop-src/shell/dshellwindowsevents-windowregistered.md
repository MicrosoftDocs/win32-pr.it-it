---
description: Chiamato quando una finestra viene registrata come finestra della shell.
title: DShellWindowsEvents. WindowRegistered, metodo
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
ms.openlocfilehash: b12ed98c6b2a11e5886ed9e76d324a1a6842cda8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "104983067"
---
# <a name="dshellwindowseventswindowregistered-method"></a><span data-ttu-id="01e48-103">DShellWindowsEvents. WindowRegistered, metodo</span><span class="sxs-lookup"><span data-stu-id="01e48-103">DShellWindowsEvents.WindowRegistered method</span></span>

<span data-ttu-id="01e48-104">Chiamato quando una finestra viene registrata come finestra della shell.</span><span class="sxs-lookup"><span data-stu-id="01e48-104">Called when a window is registered as a Shell window.</span></span>

## <a name="syntax"></a><span data-ttu-id="01e48-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="01e48-105">Syntax</span></span>


```JScript
DShellWindowsEvents.WindowRegistered(
  lCookie
)
```



## <a name="parameters"></a><span data-ttu-id="01e48-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="01e48-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01e48-107">*lCookie* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="01e48-107">*lCookie* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01e48-108">Tipo: **Integer**</span><span class="sxs-lookup"><span data-stu-id="01e48-108">Type: **Integer**</span></span>

<span data-ttu-id="01e48-109">Cookie che identifica la finestra registrata.</span><span class="sxs-lookup"><span data-stu-id="01e48-109">The cookie that identifies the window that was registered.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01e48-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="01e48-110">Return value</span></span>

<span data-ttu-id="01e48-111">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="01e48-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="01e48-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="01e48-112">Remarks</span></span>

<span data-ttu-id="01e48-113">A una finestra viene concesso un cookie quando viene registrato come finestra della shell.</span><span class="sxs-lookup"><span data-stu-id="01e48-113">A window is granted a cookie when it is registered as a Shell window.</span></span> <span data-ttu-id="01e48-114">Per ulteriori informazioni, vedere [**Register**](/windows/desktop/api/Exdisp/nf-exdisp-ishellwindows-register).</span><span class="sxs-lookup"><span data-stu-id="01e48-114">For more information, see [**Register**](/windows/desktop/api/Exdisp/nf-exdisp-ishellwindows-register).</span></span>

## <a name="requirements"></a><span data-ttu-id="01e48-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="01e48-115">Requirements</span></span>



| <span data-ttu-id="01e48-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="01e48-116">Requirement</span></span> | <span data-ttu-id="01e48-117">Valore</span><span class="sxs-lookup"><span data-stu-id="01e48-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01e48-118">Prodotto</span><span class="sxs-lookup"><span data-stu-id="01e48-118">Product</span></span><br/> | <span data-ttu-id="01e48-119">Internet Explorer 5</span><span class="sxs-lookup"><span data-stu-id="01e48-119">Internet Explorer 5</span></span><br/>                                                                                           |
| <span data-ttu-id="01e48-120">DLL</span><span class="sxs-lookup"><span data-stu-id="01e48-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="01e48-121"><dt>Shdocvw.dll (versione 5.00.2014.0216 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="01e48-121"><dt>Shdocvw.dll (version 5.00.2014.0216 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01e48-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="01e48-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01e48-123">**DShellWindowsEvents**</span><span class="sxs-lookup"><span data-stu-id="01e48-123">**DShellWindowsEvents**</span></span>](dshellwindowsevents.md)
</dt> <dt>

[<span data-ttu-id="01e48-124">**WindowRevoked**</span><span class="sxs-lookup"><span data-stu-id="01e48-124">**WindowRevoked**</span></span>](dshellwindowsevents-windowrevoked.md)
</dt> <dt>

[<span data-ttu-id="01e48-125">**Registrazione**</span><span class="sxs-lookup"><span data-stu-id="01e48-125">**Register**</span></span>](/windows/desktop/api/Exdisp/nf-exdisp-ishellwindows-register)
</dt> <dt>

[<span data-ttu-id="01e48-126">**RegisterPending**</span><span class="sxs-lookup"><span data-stu-id="01e48-126">**RegisterPending**</span></span>](/windows/desktop/api/Exdisp/nf-exdisp-ishellwindows-registerpending)
</dt> </dl>

 

 




