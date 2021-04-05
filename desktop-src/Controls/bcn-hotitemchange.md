---
title: Codice di notifica BCN_HOTITEMCHANGE (COMmctrl. h)
description: Notifica al proprietario del controllo Button che il mouse entra o esce dall'area client del controllo Button. Il controllo Button invia questo codice di notifica sotto forma di messaggio di \_ notifica WM.
ms.assetid: 92882e21-b69d-4326-94e9-ae69a0d00a83
keywords:
- Controlli di Windows per il codice di notifica BCN_HOTITEMCHANGE
topic_type:
- apiref
api_name:
- BCN_HOTITEMCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67ba6a7e64e95b45d0883b5adf34b384bccac8c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048204"
---
# <a name="bcn_hotitemchange-notification-code"></a><span data-ttu-id="68b03-105">\_Codice di notifica BCN HOTITEMCHANGE</span><span class="sxs-lookup"><span data-stu-id="68b03-105">BCN\_HOTITEMCHANGE notification code</span></span>

<span data-ttu-id="68b03-106">Notifica al proprietario del controllo Button che il mouse entra o esce dall'area client del controllo Button.</span><span class="sxs-lookup"><span data-stu-id="68b03-106">Notifies the button control owner that the mouse is entering or leaving the client area of the button control.</span></span> <span data-ttu-id="68b03-107">Il controllo Button invia questo codice di notifica sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="68b03-107">The button control sends this notification code in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
BCN_HOTITEMCHANGE

    pnmbchotitem = (NMBCHOTITEM*) lParam;
```



## <a name="parameters"></a><span data-ttu-id="68b03-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="68b03-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68b03-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="68b03-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="68b03-110">Puntatore a una struttura [**NMBCHOTITEM**](/windows/win32/api/commctrl/ns-commctrl-nmbchotitem) .</span><span class="sxs-lookup"><span data-stu-id="68b03-110">A pointer to a [**NMBCHOTITEM**](/windows/win32/api/commctrl/ns-commctrl-nmbchotitem) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68b03-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="68b03-111">Return value</span></span>

<span data-ttu-id="68b03-112">Questo messaggio non restituisce alcun valore.</span><span class="sxs-lookup"><span data-stu-id="68b03-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="68b03-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="68b03-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="68b03-114">Per usare questo codice di notifica, è necessario fornire un manifesto che specifichi Comclt32.dll versione 6,0.</span><span class="sxs-lookup"><span data-stu-id="68b03-114">To use this notification code, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="68b03-115">Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="68b03-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="68b03-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="68b03-116">Requirements</span></span>



| <span data-ttu-id="68b03-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="68b03-117">Requirement</span></span> | <span data-ttu-id="68b03-118">Valore</span><span class="sxs-lookup"><span data-stu-id="68b03-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="68b03-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="68b03-119">Minimum supported client</span></span><br/> | <span data-ttu-id="68b03-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="68b03-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="68b03-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="68b03-121">Minimum supported server</span></span><br/> | <span data-ttu-id="68b03-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="68b03-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="68b03-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="68b03-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="68b03-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="68b03-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





