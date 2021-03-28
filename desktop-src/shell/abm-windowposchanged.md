---
description: Notifica al sistema la modifica della posizione di un AppBar. Un AppBar deve chiamare questo messaggio in risposta al messaggio WM \_ WINDOWPOSCHANGED.
ms.assetid: 8ca51f5f-b6cf-4f2c-98f4-69c992679320
title: Messaggio ABM_WINDOWPOSCHANGED (Shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29c8ea6fab6960678ad030a0c1817ad5f8aaae29
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484396"
---
# <a name="abm_windowposchanged-message"></a><span data-ttu-id="03f45-104">\_Messaggio WINDOWPOSCHANGED ABM</span><span class="sxs-lookup"><span data-stu-id="03f45-104">ABM\_WINDOWPOSCHANGED message</span></span>

<span data-ttu-id="03f45-105">Notifica al sistema la modifica della posizione di un AppBar.</span><span class="sxs-lookup"><span data-stu-id="03f45-105">Notifies the system when an appbar's position has changed.</span></span> <span data-ttu-id="03f45-106">Un AppBar deve chiamare questo messaggio in risposta al messaggio [**WM \_ WINDOWPOSCHANGED**](/windows/desktop/winmsg/wm-windowposchanged) .</span><span class="sxs-lookup"><span data-stu-id="03f45-106">An appbar should call this message in response to the [**WM\_WINDOWPOSCHANGED**](/windows/desktop/winmsg/wm-windowposchanged) message.</span></span>


```C++
SHAppBarMessage(ABM_WINDOWPOSCHANGED, pabd); 
```



## <a name="parameters"></a><span data-ttu-id="03f45-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="03f45-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03f45-108">*pabd*</span><span class="sxs-lookup"><span data-stu-id="03f45-108">*pabd*</span></span> 
</dt> <dd>

<span data-ttu-id="03f45-109">Puntatore a una struttura [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) che identifica il AppBar da attivare.</span><span class="sxs-lookup"><span data-stu-id="03f45-109">A pointer to an [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure that identifies the appbar to activate.</span></span> <span data-ttu-id="03f45-110">Quando si invia questo messaggio, è necessario specificare i membri **cbSize** e **HWND** . tutti gli altri membri vengono ignorati.</span><span class="sxs-lookup"><span data-stu-id="03f45-110">You must specify the **cbSize** and **hWnd** members when sending this message; all other members are ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="03f45-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="03f45-111">Return value</span></span>

<span data-ttu-id="03f45-112">Restituisce sempre **true**.</span><span class="sxs-lookup"><span data-stu-id="03f45-112">Always returns **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="03f45-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="03f45-113">Remarks</span></span>

<span data-ttu-id="03f45-114">Questo messaggio viene ignorato se il membro **HWND** della struttura a cui punta *pabd* identifica un AppBar di Nascondi automaticamente.</span><span class="sxs-lookup"><span data-stu-id="03f45-114">This message is ignored if the **hWnd** member of the structure pointed to by *pabd* identifies an autohide appbar.</span></span>

## <a name="requirements"></a><span data-ttu-id="03f45-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="03f45-115">Requirements</span></span>



| <span data-ttu-id="03f45-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="03f45-116">Requirement</span></span> | <span data-ttu-id="03f45-117">Valore</span><span class="sxs-lookup"><span data-stu-id="03f45-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="03f45-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="03f45-118">Minimum supported client</span></span><br/> | <span data-ttu-id="03f45-119">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="03f45-119">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="03f45-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="03f45-120">Minimum supported server</span></span><br/> | <span data-ttu-id="03f45-121">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="03f45-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="03f45-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="03f45-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="03f45-123"><dt>Shellapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="03f45-123"><dt>Shellapi.h</dt></span></span> </dl> |



 

