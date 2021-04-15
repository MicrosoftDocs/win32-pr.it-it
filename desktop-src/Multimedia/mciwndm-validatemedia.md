---
title: Messaggio di MCIWNDM_VALIDATEMEDIA (VFW. h)
description: Il \_ messaggio MCIWNDM VALIDATEMEDIA aggiorna le posizioni iniziale e finale del contenuto, la posizione corrente nel contenuto e l'oggetto TrackBar in base al formato dell'ora corrente.
ms.assetid: 98ac6227-fc90-4276-8e26-2bd005e35dc6
keywords:
- MCIWNDM_VALIDATEMEDIA messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MCIWNDM_VALIDATEMEDIA
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43cb6e6a4a7c320d4eb6472c3c72da2843d0814c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517410"
---
# <a name="mciwndm_validatemedia-message"></a><span data-ttu-id="648bb-104">\_Messaggio MCIWNDM VALIDATEMEDIA</span><span class="sxs-lookup"><span data-stu-id="648bb-104">MCIWNDM\_VALIDATEMEDIA message</span></span>

<span data-ttu-id="648bb-105">Il messaggio **MCIWNDM \_ VALIDATEMEDIA** aggiorna le posizioni iniziale e finale del contenuto, la posizione corrente nel contenuto e l'oggetto TrackBar in base al formato dell'ora corrente.</span><span class="sxs-lookup"><span data-stu-id="648bb-105">The **MCIWNDM\_VALIDATEMEDIA** message updates the starting and ending locations of the content, the current position in the content, and the trackbar according to the current time format.</span></span> <span data-ttu-id="648bb-106">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MCIWndValidateMedia**](/windows/desktop/api/Vfw/nf-vfw-mciwndvalidatemedia) .</span><span class="sxs-lookup"><span data-stu-id="648bb-106">You can send this message explicitly or by using the [**MCIWndValidateMedia**](/windows/desktop/api/Vfw/nf-vfw-mciwndvalidatemedia) macro.</span></span>


```C++
MCIWNDM_VALIDATEMEDIA 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="648bb-107">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="648bb-107">Return Value</span></span>

<span data-ttu-id="648bb-108">Questo messaggio non restituisce alcun valore.</span><span class="sxs-lookup"><span data-stu-id="648bb-108">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="648bb-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="648bb-109">Remarks</span></span>

<span data-ttu-id="648bb-110">In genere, non è necessario usare questa macro. Tuttavia, se l'applicazione modifica il formato dell'ora di un dispositivo senza usare MCIWnd; le posizioni iniziale e finale del contenuto, oltre a TrackBar, continuano a usare il vecchio formato.</span><span class="sxs-lookup"><span data-stu-id="648bb-110">Typically, you should not need to use this macro; however, if your application changes the time format of a device without using MCIWnd; the starting and ending locations of the content, as well as the trackbar, continue to use the old format.</span></span> <span data-ttu-id="648bb-111">È possibile utilizzare questa macro per aggiornare questi valori.</span><span class="sxs-lookup"><span data-stu-id="648bb-111">You can use this macro to update these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="648bb-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="648bb-112">Requirements</span></span>



| <span data-ttu-id="648bb-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="648bb-113">Requirement</span></span> | <span data-ttu-id="648bb-114">Valore</span><span class="sxs-lookup"><span data-stu-id="648bb-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="648bb-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="648bb-115">Minimum supported client</span></span><br/> | <span data-ttu-id="648bb-116">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="648bb-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="648bb-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="648bb-117">Minimum supported server</span></span><br/> | <span data-ttu-id="648bb-118">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="648bb-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="648bb-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="648bb-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="648bb-120"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="648bb-120"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="648bb-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="648bb-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="648bb-122">**MCIWndValidateMedia**</span><span class="sxs-lookup"><span data-stu-id="648bb-122">**MCIWndValidateMedia**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndvalidatemedia)
</dt> </dl>

 

 





