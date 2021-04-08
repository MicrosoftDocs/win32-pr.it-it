---
title: Messaggio di ICM_GET (VFW. h)
description: Il \_ messaggio ICM Get recupera un valore DWORD definito dall'applicazione da un driver di compressione video.
ms.assetid: 288c0053-16a1-4547-b748-da218a0b588c
keywords:
- ICM_GET messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- ICM_GET
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e23cd994546be41b5f938331b2dc632897635c32
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740495"
---
# <a name="icm_get-message"></a><span data-ttu-id="26be0-104">\_Messaggio ICM Get</span><span class="sxs-lookup"><span data-stu-id="26be0-104">ICM\_GET message</span></span>

<span data-ttu-id="26be0-105">Il messaggio **ICM \_ Get** recupera un valore **DWORD** definito dall'applicazione da un driver di compressione video.</span><span class="sxs-lookup"><span data-stu-id="26be0-105">The **ICM\_GET** message retrieves an application-defined **DWORD** value from a video compression driver.</span></span>


```C++
ICM_GET 
wParam = (DWORD) (LPVOID) pv; 
lParam = (DWORD) cb; 
```



## <a name="parameters"></a><span data-ttu-id="26be0-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="26be0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26be0-107"><span id="pv"></span><span id="PV"></span>*PV*</span><span class="sxs-lookup"><span data-stu-id="26be0-107"><span id="pv"></span><span id="PV"></span>*pv*</span></span>
</dt> <dd>

<span data-ttu-id="26be0-108">Puntatore a un blocco di memoria da riempire con lo stato corrente.</span><span class="sxs-lookup"><span data-stu-id="26be0-108">Pointer to a block of memory to be filled with the current state.</span></span> <span data-ttu-id="26be0-109">È anche possibile specificare **null** per determinare la quantità di memoria richiesta dalle informazioni sullo stato.</span><span class="sxs-lookup"><span data-stu-id="26be0-109">You can also specify **NULL** to determine the amount of memory required by the state information.</span></span>

</dd> <dt>

<span data-ttu-id="26be0-110"><span id="cb"></span><span id="CB"></span>*CB*</span><span class="sxs-lookup"><span data-stu-id="26be0-110"><span id="cb"></span><span id="CB"></span>*cb*</span></span>
</dt> <dd>

<span data-ttu-id="26be0-111">Dimensione, in byte, del blocco di memoria.</span><span class="sxs-lookup"><span data-stu-id="26be0-111">Size, in bytes, of the block of memory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26be0-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="26be0-112">Return Value</span></span>

<span data-ttu-id="26be0-113">Restituisce la quantità di memoria, in byte, necessaria per archiviare le informazioni sullo stato.</span><span class="sxs-lookup"><span data-stu-id="26be0-113">Returns the amount of memory, in bytes, required to store the status information.</span></span>

## <a name="remarks"></a><span data-ttu-id="26be0-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="26be0-114">Remarks</span></span>

<span data-ttu-id="26be0-115">La struttura utilizzata per rappresentare le informazioni sullo stato è specifica del driver ed è definita dal driver.</span><span class="sxs-lookup"><span data-stu-id="26be0-115">The structure used to represent state information is driver specific and is defined by the driver.</span></span>

## <a name="requirements"></a><span data-ttu-id="26be0-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="26be0-116">Requirements</span></span>



| <span data-ttu-id="26be0-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="26be0-117">Requirement</span></span> | <span data-ttu-id="26be0-118">Valore</span><span class="sxs-lookup"><span data-stu-id="26be0-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="26be0-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="26be0-119">Minimum supported client</span></span><br/> | <span data-ttu-id="26be0-120">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="26be0-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="26be0-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="26be0-121">Minimum supported server</span></span><br/> | <span data-ttu-id="26be0-122">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="26be0-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="26be0-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="26be0-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="26be0-124"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="26be0-124"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26be0-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="26be0-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26be0-126">Gestione compressione video</span><span class="sxs-lookup"><span data-stu-id="26be0-126">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="26be0-127">Messaggi di compressione video</span><span class="sxs-lookup"><span data-stu-id="26be0-127">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





