---
description: Inviato a una DLL di estensione quando il file Manager Scarica la DLL.
title: Messaggio FMEVENT_UNLOAD (Wfext. h)
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
ms.openlocfilehash: 140fbdc79980a2ab6ba9f50b8815429436df0d3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127863"
---
# <a name="fmevent_unload-message"></a><span data-ttu-id="bf6ca-103">\_Messaggio di scaricamento FMEVENT</span><span class="sxs-lookup"><span data-stu-id="bf6ca-103">FMEVENT\_UNLOAD message</span></span>

<span data-ttu-id="bf6ca-104">Inviato a una DLL di estensione quando il file Manager Scarica la DLL.</span><span class="sxs-lookup"><span data-stu-id="bf6ca-104">Sent to an extension DLL when File Manager is unloading the DLL.</span></span>

## <a name="parameters"></a><span data-ttu-id="bf6ca-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="bf6ca-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf6ca-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bf6ca-106">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="bf6ca-107">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="bf6ca-107">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="bf6ca-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bf6ca-108">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="bf6ca-109">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="bf6ca-109">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf6ca-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bf6ca-110">Return value</span></span>

<span data-ttu-id="bf6ca-111">Una DLL di estensione deve restituire zero se elabora questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="bf6ca-111">An extension DLL should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="bf6ca-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="bf6ca-112">Remarks</span></span>

<span data-ttu-id="bf6ca-113">I valori *HWND* e **HMENU** passati con i messaggi [**FMEVENT \_ Load**](fmevent-load.md) e [**FMEVENT \_ INITMENU**](fmevent-initmenu.md) potrebbero non essere validi al momento dell'invio del messaggio.</span><span class="sxs-lookup"><span data-stu-id="bf6ca-113">The *hwnd* and **hMenu** values passed with the [**FMEVENT\_LOAD**](fmevent-load.md) and [**FMEVENT\_INITMENU**](fmevent-initmenu.md) messages may not be valid at the time this message is sent.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf6ca-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bf6ca-114">Requirements</span></span>



| <span data-ttu-id="bf6ca-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf6ca-115">Requirement</span></span> | <span data-ttu-id="bf6ca-116">Valore</span><span class="sxs-lookup"><span data-stu-id="bf6ca-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="bf6ca-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bf6ca-117">Minimum supported client</span></span><br/> | <span data-ttu-id="bf6ca-118">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="bf6ca-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="bf6ca-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bf6ca-119">Minimum supported server</span></span><br/> | <span data-ttu-id="bf6ca-120">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="bf6ca-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="bf6ca-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bf6ca-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="bf6ca-122"><dt>Wfext. h</dt></span><span class="sxs-lookup"><span data-stu-id="bf6ca-122"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf6ca-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bf6ca-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf6ca-124">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="bf6ca-124">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> </dl>

 

 




