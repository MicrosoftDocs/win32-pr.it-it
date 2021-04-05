---
title: Messaggio DM_POINTERHITTEST
description: Inviato a una finestra, quando viene rilevato per la prima volta l'input del puntatore, per determinare la destinazione di input più probabile per la manipolazione diretta.
ms.assetid: E4CE60F0-0C2A-440A-8F64-B070867A1572
keywords:
- Messaggi e notifiche di input del messaggio DM_POINTERHITTEST
topic_type:
- apiref
api_name:
- DM_POINTERHITTEST
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 23efab4606f758acfffdd02fa4c53a729f1f4a99
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120559"
---
# <a name="dm_pointerhittest-message"></a><span data-ttu-id="8ffdb-104">Messaggio DM_POINTERHITTEST</span><span class="sxs-lookup"><span data-stu-id="8ffdb-104">DM_POINTERHITTEST message</span></span>

<span data-ttu-id="8ffdb-105">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="8ffdb-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="8ffdb-106">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="8ffdb-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="8ffdb-107">Inviato a una finestra, quando viene rilevato per la prima volta l'input del puntatore, per determinare la destinazione di input più probabile per la [manipolazione diretta](/previous-versions/windows/desktop/directmanipulation/direct-manipulation-portal).</span><span class="sxs-lookup"><span data-stu-id="8ffdb-107">Sent to a window, when pointer input is first detected, in order to determine the most probable input target for [Direct Manipulation](/previous-versions/windows/desktop/directmanipulation/direct-manipulation-portal).</span></span>

> <span data-ttu-id="8ffdb-108">\[! Importante\]</span><span class="sxs-lookup"><span data-stu-id="8ffdb-108">\[!Important\]</span></span>  
> <span data-ttu-id="8ffdb-109">Le applicazioni desktop devono essere compatibili con DPI.</span><span class="sxs-lookup"><span data-stu-id="8ffdb-109">Desktop apps should be DPI aware.</span></span> <span data-ttu-id="8ffdb-110">Se l'app non è compatibile con DPI, le coordinate dello schermo contenute nei messaggi puntatore e le strutture correlate potrebbero sembrare non accurate a causa della virtualizzazione DPI.</span><span class="sxs-lookup"><span data-stu-id="8ffdb-110">If your app is not DPI aware, screen coordinates contained in pointer messages and related structures might appear inaccurate due to DPI virtualization.</span></span> <span data-ttu-id="8ffdb-111">La virtualizzazione DPI fornisce il supporto per il ridimensionamento automatico per le applicazioni che non sono compatibili con DPI ed è attivo per impostazione predefinita (gli utenti possono disabilitarlo).</span><span class="sxs-lookup"><span data-stu-id="8ffdb-111">DPI virtualization provides automatic scaling support to applications that are not DPI aware and is active by default (users can turn it off).</span></span> <span data-ttu-id="8ffdb-112">Per altre informazioni, vedere [scrittura di applicazioni Win32 ad alta risoluzione](/previous-versions//dd464660(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8ffdb-112">For more information, see [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).</span></span>

 


```C++
#define DM_POINTERHITTEST       0x0250
```



## <a name="parameters"></a><span data-ttu-id="8ffdb-113">Parametri</span><span class="sxs-lookup"><span data-stu-id="8ffdb-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ffdb-114">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8ffdb-114">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8ffdb-115">Non utilizzato.</span><span class="sxs-lookup"><span data-stu-id="8ffdb-115">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="8ffdb-116">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8ffdb-116">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8ffdb-117">Non utilizzato.</span><span class="sxs-lookup"><span data-stu-id="8ffdb-117">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ffdb-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8ffdb-118">Return value</span></span>

<span data-ttu-id="8ffdb-119">NULL</span><span class="sxs-lookup"><span data-stu-id="8ffdb-119">NULL</span></span>

## <a name="requirements"></a><span data-ttu-id="8ffdb-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8ffdb-120">Requirements</span></span>



| <span data-ttu-id="8ffdb-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="8ffdb-121">Requirement</span></span> | <span data-ttu-id="8ffdb-122">Valore</span><span class="sxs-lookup"><span data-stu-id="8ffdb-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ffdb-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8ffdb-123">Minimum supported client</span></span><br/> | <span data-ttu-id="8ffdb-124">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="8ffdb-124">Windows 10 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="8ffdb-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8ffdb-125">Minimum supported server</span></span><br/> | <span data-ttu-id="8ffdb-126">\[Solo app desktop Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="8ffdb-126">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="8ffdb-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8ffdb-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="8ffdb-128"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8ffdb-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ffdb-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8ffdb-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ffdb-130">Messaggi</span><span class="sxs-lookup"><span data-stu-id="8ffdb-130">Messages</span></span>](messages.md)
</dt> </dl>

 

