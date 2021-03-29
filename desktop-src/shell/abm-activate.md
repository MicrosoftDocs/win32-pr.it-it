---
description: Notifica al sistema che è stato attivato un AppBar. Un AppBar deve chiamare questo messaggio in risposta al messaggio di \_ attivazione WM.
ms.assetid: 16011302-7c2d-4c34-9953-51cceb96e4b3
title: Messaggio ABM_ACTIVATE (Shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94a44bcc33efcd3d1a9af5e7e2abca33893e9fe9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128482"
---
# <a name="abm_activate-message"></a><span data-ttu-id="5bc17-104">Messaggio di attivazione di ABM \_</span><span class="sxs-lookup"><span data-stu-id="5bc17-104">ABM\_ACTIVATE message</span></span>

<span data-ttu-id="5bc17-105">Notifica al sistema che è stato attivato un AppBar.</span><span class="sxs-lookup"><span data-stu-id="5bc17-105">Notifies the system that an appbar has been activated.</span></span> <span data-ttu-id="5bc17-106">Un AppBar deve chiamare questo messaggio in risposta al messaggio [**di \_ attivazione WM**](/windows/desktop/inputdev/wm-activate) .</span><span class="sxs-lookup"><span data-stu-id="5bc17-106">An appbar should call this message in response to the [**WM\_ACTIVATE**](/windows/desktop/inputdev/wm-activate) message.</span></span>


```C++

SHAppBarMessage(ABM_ACTIVATE, pabd); 

            
```



## <a name="parameters"></a><span data-ttu-id="5bc17-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="5bc17-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5bc17-108">*pabd*</span><span class="sxs-lookup"><span data-stu-id="5bc17-108">*pabd*</span></span> 
</dt> <dd>

<span data-ttu-id="5bc17-109">Puntatore a una struttura [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) che identifica il AppBar da attivare.</span><span class="sxs-lookup"><span data-stu-id="5bc17-109">A pointer to an [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure that identifies the appbar to activate.</span></span> <span data-ttu-id="5bc17-110">Quando si invia questo messaggio, è necessario specificare i membri **cbSize** e **HWND** . tutti gli altri membri vengono ignorati.</span><span class="sxs-lookup"><span data-stu-id="5bc17-110">You must specify the **cbSize** and **hWnd** members when sending this message; all other members are ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5bc17-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5bc17-111">Return value</span></span>

<span data-ttu-id="5bc17-112">Restituisce sempre **true**.</span><span class="sxs-lookup"><span data-stu-id="5bc17-112">Always returns **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="5bc17-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="5bc17-113">Remarks</span></span>

<span data-ttu-id="5bc17-114">Questo messaggio viene ignorato se il membro **HWND** della struttura a cui punta *pabd* identifica un AppBar di Nascondi automaticamente.</span><span class="sxs-lookup"><span data-stu-id="5bc17-114">This message is ignored if the **hWnd** member of the structure pointed to by *pabd* identifies an autohide appbar.</span></span> <span data-ttu-id="5bc17-115">Il sistema imposta automaticamente lo z-order per Nascondi automaticamente AppBar.</span><span class="sxs-lookup"><span data-stu-id="5bc17-115">The system automatically sets the z-order for autohide appbars.</span></span>

## <a name="requirements"></a><span data-ttu-id="5bc17-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5bc17-116">Requirements</span></span>



| <span data-ttu-id="5bc17-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="5bc17-117">Requirement</span></span> | <span data-ttu-id="5bc17-118">Valore</span><span class="sxs-lookup"><span data-stu-id="5bc17-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5bc17-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5bc17-119">Minimum supported client</span></span><br/> | <span data-ttu-id="5bc17-120">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="5bc17-120">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="5bc17-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5bc17-121">Minimum supported server</span></span><br/> | <span data-ttu-id="5bc17-122">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="5bc17-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5bc17-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5bc17-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="5bc17-124"><dt>Shellapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="5bc17-124"><dt>Shellapi.h</dt></span></span> </dl> |



 

