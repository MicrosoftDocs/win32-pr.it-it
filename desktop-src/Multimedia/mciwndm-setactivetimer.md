---
title: Messaggio di MCIWNDM_SETACTIVETIMER (VFW. h)
description: Il \_ messaggio MCIWNDM SETACTIVETIMER imposta il periodo di aggiornamento usato da MCIWnd per aggiornare il controllo TrackBar nella finestra MCIWnd, aggiornare le informazioni sulla posizione visualizzate nella barra del titolo della finestra e inviare i messaggi di notifica alla finestra padre quando la finestra MCIWnd è attiva. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro MCIWndSetActiveTimer.
ms.assetid: a30c0091-d9bb-44a3-a7b0-d1be30adcd9c
keywords:
- MCIWNDM_SETACTIVETIMER messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MCIWNDM_SETACTIVETIMER
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1924a991f0627009a8e622c8f8be086b2e045635
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120459"
---
# <a name="mciwndm_setactivetimer-message"></a><span data-ttu-id="ac510-105">\_Messaggio MCIWNDM SETACTIVETIMER</span><span class="sxs-lookup"><span data-stu-id="ac510-105">MCIWNDM\_SETACTIVETIMER message</span></span>

<span data-ttu-id="ac510-106">Il messaggio **MCIWNDM \_ SETACTIVETIMER** imposta il periodo di aggiornamento usato da MCIWnd per aggiornare il controllo TrackBar nella finestra MCIWnd, aggiornare le informazioni sulla posizione visualizzate nella barra del titolo della finestra e inviare i messaggi di notifica alla finestra padre quando la finestra MCIWnd è attiva.</span><span class="sxs-lookup"><span data-stu-id="ac510-106">The **MCIWNDM\_SETACTIVETIMER** message sets the update period used by MCIWnd to update the trackbar in the MCIWnd window, update position information displayed in the window title bar, and send notification messages to the parent window when the MCIWnd window is active.</span></span> <span data-ttu-id="ac510-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MCIWndSetActiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetactivetimer) .</span><span class="sxs-lookup"><span data-stu-id="ac510-107">You can send this message explicitly or by using the [**MCIWndSetActiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetactivetimer) macro.</span></span>


```C++
MCIWNDM_SETACTIVETIMER 
wParam = (WPARAM) (UINT) active; 
lParam = 0L; 
```



## <a name="parameters"></a><span data-ttu-id="ac510-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="ac510-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac510-109"><span id="active"></span><span id="ACTIVE"></span>*Active*</span><span class="sxs-lookup"><span data-stu-id="ac510-109"><span id="active"></span><span id="ACTIVE"></span>*active*</span></span>
</dt> <dd>

<span data-ttu-id="ac510-110">Periodo di aggiornamento, in millisecondi.</span><span class="sxs-lookup"><span data-stu-id="ac510-110">Update period, in milliseconds.</span></span> <span data-ttu-id="ac510-111">Il valore predefinito è 500 millisecondi.</span><span class="sxs-lookup"><span data-stu-id="ac510-111">The default is 500 milliseconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac510-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ac510-112">Return Value</span></span>

<span data-ttu-id="ac510-113">Questo messaggio non restituisce alcun valore.</span><span class="sxs-lookup"><span data-stu-id="ac510-113">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac510-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ac510-114">Requirements</span></span>



| <span data-ttu-id="ac510-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="ac510-115">Requirement</span></span> | <span data-ttu-id="ac510-116">Valore</span><span class="sxs-lookup"><span data-stu-id="ac510-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="ac510-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ac510-117">Minimum supported client</span></span><br/> | <span data-ttu-id="ac510-118">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ac510-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="ac510-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ac510-119">Minimum supported server</span></span><br/> | <span data-ttu-id="ac510-120">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ac510-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="ac510-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ac510-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="ac510-122"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="ac510-122"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac510-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ac510-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac510-124">**MCIWndSetActiveTimer**</span><span class="sxs-lookup"><span data-stu-id="ac510-124">**MCIWndSetActiveTimer**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndsetactivetimer)
</dt> </dl>

 

 





