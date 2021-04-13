---
title: Messaggio di MCIWNDM_SETINACTIVETIMER (VFW. h)
description: Il \_ messaggio MCIWNDM SETINACTIVETIMER imposta il periodo di aggiornamento usato da MCIWnd per aggiornare il controllo TrackBar nella finestra MCIWnd, aggiornare le informazioni sulla posizione visualizzate nella barra del titolo della finestra e inviare messaggi di notifica alla finestra padre quando la finestra MCIWnd è inattiva. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro MCIWndSetInactiveTimer.
ms.assetid: 8900c372-0493-4a63-a027-ef6ecf8f8254
keywords:
- MCIWNDM_SETINACTIVETIMER messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MCIWNDM_SETINACTIVETIMER
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba4504d84b254dfb67616568f5f97bba8e3bc2e3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518250"
---
# <a name="mciwndm_setinactivetimer-message"></a><span data-ttu-id="1242c-105">\_Messaggio MCIWNDM SETINACTIVETIMER</span><span class="sxs-lookup"><span data-stu-id="1242c-105">MCIWNDM\_SETINACTIVETIMER message</span></span>

<span data-ttu-id="1242c-106">Il messaggio **MCIWNDM \_ SETINACTIVETIMER** imposta il periodo di aggiornamento usato da MCIWnd per aggiornare il controllo TrackBar nella finestra MCIWnd, aggiornare le informazioni sulla posizione visualizzate nella barra del titolo della finestra e inviare messaggi di notifica alla finestra padre quando la finestra MCIWnd è inattiva.</span><span class="sxs-lookup"><span data-stu-id="1242c-106">The **MCIWNDM\_SETINACTIVETIMER** message sets the update period used by MCIWnd to update the trackbar in the MCIWnd window, update position information displayed in the window title bar, and send notification messages to the parent window when the MCIWnd window is inactive.</span></span> <span data-ttu-id="1242c-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MCIWndSetInactiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetinactivetimer) .</span><span class="sxs-lookup"><span data-stu-id="1242c-107">You can send this message explicitly or by using the [**MCIWndSetInactiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetinactivetimer) macro.</span></span>


```C++
MCIWNDM_SETINACTIVETIMER 
wParam = (WPARAM) (UINT) inactive; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="1242c-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="1242c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1242c-109"><span id="inactive"></span><span id="INACTIVE"></span>*inattivo*</span><span class="sxs-lookup"><span data-stu-id="1242c-109"><span id="inactive"></span><span id="INACTIVE"></span>*inactive*</span></span>
</dt> <dd>

<span data-ttu-id="1242c-110">Periodo di aggiornamento, in millisecondi.</span><span class="sxs-lookup"><span data-stu-id="1242c-110">Update period, in milliseconds.</span></span> <span data-ttu-id="1242c-111">Il valore predefinito è 2000 millisecondi.</span><span class="sxs-lookup"><span data-stu-id="1242c-111">The default is 2000 milliseconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1242c-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1242c-112">Return Value</span></span>

<span data-ttu-id="1242c-113">Questo messaggio non restituisce alcun valore.</span><span class="sxs-lookup"><span data-stu-id="1242c-113">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="1242c-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1242c-114">Requirements</span></span>



| <span data-ttu-id="1242c-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="1242c-115">Requirement</span></span> | <span data-ttu-id="1242c-116">Valore</span><span class="sxs-lookup"><span data-stu-id="1242c-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="1242c-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1242c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="1242c-118">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="1242c-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="1242c-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1242c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="1242c-120">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="1242c-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="1242c-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1242c-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="1242c-122"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="1242c-122"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1242c-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1242c-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1242c-124">**MCIWndSetInactiveTimer**</span><span class="sxs-lookup"><span data-stu-id="1242c-124">**MCIWndSetInactiveTimer**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndsetinactivetimer)
</dt> </dl>

 

 





