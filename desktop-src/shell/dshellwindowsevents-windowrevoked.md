---
description: Chiamato quando viene revocata la registrazione di una finestra della shell.
title: Metodo DShellWindowsEvents.WindowRevoked
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DShellWindowsEvents.WindowRevoked
api_type:
- COM
api_location:
- Shdocvw.dll
ms.assetid: 92e8653f-7f41-4e0b-97e5-429fddc51951
ms.openlocfilehash: 7ed78dcaa545b2321b04aff9ff2f4e711f93c992
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109843182"
---
# <a name="dshellwindowseventswindowrevoked-method"></a><span data-ttu-id="47776-103">Metodo DShellWindowsEvents.WindowRevoked</span><span class="sxs-lookup"><span data-stu-id="47776-103">DShellWindowsEvents.WindowRevoked method</span></span>

<span data-ttu-id="47776-104">Chiamato quando viene revocata la registrazione di una finestra della shell.</span><span class="sxs-lookup"><span data-stu-id="47776-104">Called when a Shell window's registration is revoked.</span></span>

## <a name="syntax"></a><span data-ttu-id="47776-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="47776-105">Syntax</span></span>


```JScript
DShellWindowsEvents.WindowRevoked(
  lCookie
)
```



## <a name="parameters"></a><span data-ttu-id="47776-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="47776-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="47776-107">*lCookie* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="47776-107">*lCookie* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47776-108">Tipo: **Integer**</span><span class="sxs-lookup"><span data-stu-id="47776-108">Type: **Integer**</span></span>

<span data-ttu-id="47776-109">Cookie che identifica la finestra revocata.</span><span class="sxs-lookup"><span data-stu-id="47776-109">The cookie that identifies the window that was revoked.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="47776-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="47776-110">Return value</span></span>

<span data-ttu-id="47776-111">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="47776-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="47776-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="47776-112">Remarks</span></span>

<span data-ttu-id="47776-113">A una finestra viene concesso un cookie quando viene registrata come finestra della shell.</span><span class="sxs-lookup"><span data-stu-id="47776-113">A window is granted a cookie when it is registered as a Shell window.</span></span> <span data-ttu-id="47776-114">Per altre informazioni, vedere [**Registrare**](/windows/desktop/api/Exdisp/nf-exdisp-ishellwindows-register).</span><span class="sxs-lookup"><span data-stu-id="47776-114">For more information, see [**Register**](/windows/desktop/api/Exdisp/nf-exdisp-ishellwindows-register).</span></span>

## <a name="requirements"></a><span data-ttu-id="47776-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="47776-115">Requirements</span></span>



| <span data-ttu-id="47776-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="47776-116">Requirement</span></span> | <span data-ttu-id="47776-117">Valore</span><span class="sxs-lookup"><span data-stu-id="47776-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="47776-118">Prodotto</span><span class="sxs-lookup"><span data-stu-id="47776-118">Product</span></span><br/> | <span data-ttu-id="47776-119">Internet Explorer 5</span><span class="sxs-lookup"><span data-stu-id="47776-119">Internet Explorer 5</span></span><br/>                                                                                           |
| <span data-ttu-id="47776-120">DLL</span><span class="sxs-lookup"><span data-stu-id="47776-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="47776-121"><dt>Shdocvw.dll (versione 5.00.2014.0216 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="47776-121"><dt>Shdocvw.dll (version 5.00.2014.0216 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="47776-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="47776-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47776-123">**DShellWindowsEvents**</span><span class="sxs-lookup"><span data-stu-id="47776-123">**DShellWindowsEvents**</span></span>](dshellwindowsevents.md)
</dt> <dt>

[<span data-ttu-id="47776-124">**WindowRegistered**</span><span class="sxs-lookup"><span data-stu-id="47776-124">**WindowRegistered**</span></span>](dshellwindowsevents-windowregistered.md)
</dt> <dt>

[<span data-ttu-id="47776-125">**Revoke**</span><span class="sxs-lookup"><span data-stu-id="47776-125">**Revoke**</span></span>](/windows/desktop/api/Exdisp/nf-exdisp-ishellwindows-revoke)
</dt> </dl>

 

 




