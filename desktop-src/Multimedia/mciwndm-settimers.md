---
title: Messaggio di MCIWNDM_SETTIMERS (VFW. h)
description: Il \_ messaggio MCIWNDM Timers imposta i periodi di aggiornamento utilizzati da MCIWnd per aggiornare il controllo TrackBar nella finestra MCIWnd, aggiornare le informazioni sulla posizione visualizzate nella barra del titolo della finestra e inviare messaggi di notifica alla finestra padre.
ms.assetid: 06407c67-b620-4f80-9fe9-456cdf3d0666
keywords:
- MCIWNDM_SETTIMERS messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MCIWNDM_SETTIMERS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7bba3fa2e474a15dc23deb9cdc6d00d148b8cd3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740234"
---
# <a name="mciwndm_settimers-message"></a><span data-ttu-id="78041-104">MCIWNDM \_ messaggi temporizzati</span><span class="sxs-lookup"><span data-stu-id="78041-104">MCIWNDM\_SETTIMERS message</span></span>

<span data-ttu-id="78041-105">Il messaggio **MCIWNDM \_ Timers** imposta i periodi di aggiornamento utilizzati da MCIWnd per aggiornare il controllo TrackBar nella finestra MCIWnd, aggiornare le informazioni sulla posizione visualizzate nella barra del titolo della finestra e inviare messaggi di notifica alla finestra padre.</span><span class="sxs-lookup"><span data-stu-id="78041-105">The **MCIWNDM\_SETTIMERS** message sets the update periods used by MCIWnd to update the trackbar in the MCIWnd window, update the position information displayed in the window title bar, and send notification messages to the parent window.</span></span> <span data-ttu-id="78041-106">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MCIWndSetTimers**](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimers) .</span><span class="sxs-lookup"><span data-stu-id="78041-106">You can send this message explicitly or by using the [**MCIWndSetTimers**](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimers) macro.</span></span>


```C++
MCIWNDM_SETTIMERS 
wParam = (WPARAM) (UINT) active; 
lParam = (LPARAM) (UINT) inactive; 
```



## <a name="parameters"></a><span data-ttu-id="78041-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="78041-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78041-108"><span id="active"></span><span id="ACTIVE"></span>*Active*</span><span class="sxs-lookup"><span data-stu-id="78041-108"><span id="active"></span><span id="ACTIVE"></span>*active*</span></span>
</dt> <dd>

<span data-ttu-id="78041-109">Periodo di aggiornamento utilizzato da MCIWnd quando è la finestra attiva.</span><span class="sxs-lookup"><span data-stu-id="78041-109">Update period used by MCIWnd when it is the active window.</span></span> <span data-ttu-id="78041-110">Il valore predefinito è 500 millisecondi.</span><span class="sxs-lookup"><span data-stu-id="78041-110">The default value is 500 milliseconds.</span></span> <span data-ttu-id="78041-111">Lo spazio di archiviazione per questo valore è limitato a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="78041-111">Storage for this value is limited to 16 bits.</span></span>

</dd> <dt>

<span data-ttu-id="78041-112"><span id="inactive"></span><span id="INACTIVE"></span>*inattivo*</span><span class="sxs-lookup"><span data-stu-id="78041-112"><span id="inactive"></span><span id="INACTIVE"></span>*inactive*</span></span>
</dt> <dd>

<span data-ttu-id="78041-113">Periodo di aggiornamento utilizzato da MCIWnd quando si tratta della finestra inattiva.</span><span class="sxs-lookup"><span data-stu-id="78041-113">Update period used by MCIWnd when it is the inactive window.</span></span> <span data-ttu-id="78041-114">Il valore predefinito è 2000 millisecondi.</span><span class="sxs-lookup"><span data-stu-id="78041-114">The default value is 2000 milliseconds.</span></span> <span data-ttu-id="78041-115">Lo spazio di archiviazione per questo valore è limitato a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="78041-115">Storage for this value is limited to 16 bits.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78041-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="78041-116">Return Value</span></span>

<span data-ttu-id="78041-117">Questo messaggio non restituisce alcun valore.</span><span class="sxs-lookup"><span data-stu-id="78041-117">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="78041-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="78041-118">Requirements</span></span>



| <span data-ttu-id="78041-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="78041-119">Requirement</span></span> | <span data-ttu-id="78041-120">Valore</span><span class="sxs-lookup"><span data-stu-id="78041-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="78041-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="78041-121">Minimum supported client</span></span><br/> | <span data-ttu-id="78041-122">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="78041-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="78041-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="78041-123">Minimum supported server</span></span><br/> | <span data-ttu-id="78041-124">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="78041-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="78041-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="78041-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="78041-126"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="78041-126"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78041-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="78041-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78041-128">**MCIWndSetTimers**</span><span class="sxs-lookup"><span data-stu-id="78041-128">**MCIWndSetTimers**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimers)
</dt> </dl>

 

 





