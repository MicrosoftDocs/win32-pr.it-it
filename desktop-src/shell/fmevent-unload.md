---
description: Inviato a una DLL di estensione quando File Manager scarica la DLL.
title: FMEVENT_UNLOAD messaggio (Wfext.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMEVENT_UNLOAD
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 15ffcd46-602f-4ad0-9c58-0b8056b9cac4
ms.openlocfilehash: 24b5b2a77393178cad545cb63c1524a8d7e92c5c
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109843072"
---
# <a name="fmevent_unload-message"></a><span data-ttu-id="cea53-103">Messaggio FMEVENT \_ UNLOAD</span><span class="sxs-lookup"><span data-stu-id="cea53-103">FMEVENT\_UNLOAD message</span></span>

<span data-ttu-id="cea53-104">Inviato a una DLL di estensione quando File Manager scarica la DLL.</span><span class="sxs-lookup"><span data-stu-id="cea53-104">Sent to an extension DLL when File Manager is unloading the DLL.</span></span>

## <a name="parameters"></a><span data-ttu-id="cea53-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="cea53-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cea53-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cea53-106">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="cea53-107">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="cea53-107">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="cea53-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cea53-108">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="cea53-109">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="cea53-109">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cea53-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cea53-110">Return value</span></span>

<span data-ttu-id="cea53-111">Una DLL di estensione deve restituire zero se elabora questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="cea53-111">An extension DLL should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="cea53-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="cea53-112">Remarks</span></span>

<span data-ttu-id="cea53-113">I *valori hwnd* e **hMenu** passati con i messaggi [**FMEVENT \_ LOAD**](fmevent-load.md) e [**FMEVENT \_ INITMENU**](fmevent-initmenu.md) potrebbero non essere validi al momento dell'invio del messaggio.</span><span class="sxs-lookup"><span data-stu-id="cea53-113">The *hwnd* and **hMenu** values passed with the [**FMEVENT\_LOAD**](fmevent-load.md) and [**FMEVENT\_INITMENU**](fmevent-initmenu.md) messages may not be valid at the time this message is sent.</span></span>

## <a name="requirements"></a><span data-ttu-id="cea53-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cea53-114">Requirements</span></span>



| <span data-ttu-id="cea53-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="cea53-115">Requirement</span></span> | <span data-ttu-id="cea53-116">Valore</span><span class="sxs-lookup"><span data-stu-id="cea53-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="cea53-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cea53-117">Minimum supported client</span></span><br/> | <span data-ttu-id="cea53-118">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="cea53-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="cea53-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cea53-119">Minimum supported server</span></span><br/> | <span data-ttu-id="cea53-120">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="cea53-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="cea53-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cea53-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="cea53-122"><dt>Wfext.h</dt></span><span class="sxs-lookup"><span data-stu-id="cea53-122"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cea53-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cea53-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cea53-124">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="cea53-124">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> </dl>

 

 




