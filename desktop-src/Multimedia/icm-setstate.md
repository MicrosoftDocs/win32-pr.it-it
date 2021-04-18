---
title: Messaggio di ICM_SETSTATE (VFW. h)
description: Il \_ messaggio MCI sestate notifica a un driver di compressione video di impostare lo stato del compressore. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro ICSetState.
ms.assetid: d1a91847-2893-4c8b-9ca1-02db71ec2c81
keywords:
- ICM_SETSTATE messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- ICM_SETSTATE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 230e0aaf3752016efd276d7d55624ee2abb4f8e0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302778"
---
# <a name="icm_setstate-message"></a><span data-ttu-id="14816-105">\_Messaggio di SESTATO ICM</span><span class="sxs-lookup"><span data-stu-id="14816-105">ICM\_SETSTATE message</span></span>

<span data-ttu-id="14816-106">Il messaggio **MCI \_ sestate** notifica a un driver di compressione video di impostare lo stato del compressore.</span><span class="sxs-lookup"><span data-stu-id="14816-106">The **ICM\_SETSTATE** message notifies a video compression driver to set the state of the compressor.</span></span> <span data-ttu-id="14816-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**ICSetState**](/windows/desktop/api/Vfw/nf-vfw-icsetstate) .</span><span class="sxs-lookup"><span data-stu-id="14816-107">You can send this message explicitly or by using the [**ICSetState**](/windows/desktop/api/Vfw/nf-vfw-icsetstate) macro.</span></span>


```C++
ICM_SETSTATE 
wParam = (DWORD_PTR) (LPVOID) pv; 
lParam = (DWORD_PTR) cb; 
```



## <a name="parameters"></a><span data-ttu-id="14816-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="14816-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14816-109"><span id="pv"></span><span id="PV"></span>*PV*</span><span class="sxs-lookup"><span data-stu-id="14816-109"><span id="pv"></span><span id="PV"></span>*pv*</span></span>
</dt> <dd>

<span data-ttu-id="14816-110">Puntatore a un blocco di memoria contenente i dati di configurazione.</span><span class="sxs-lookup"><span data-stu-id="14816-110">Pointer to a block of memory containing configuration data.</span></span> <span data-ttu-id="14816-111">È possibile specificare **null** per questo parametro per ripristinare lo stato predefinito del compressore.</span><span class="sxs-lookup"><span data-stu-id="14816-111">You can specify **NULL** for this parameter to reset the compressor to its default state.</span></span>

</dd> <dt>

<span data-ttu-id="14816-112"><span id="cb"></span><span id="CB"></span>*CB*</span><span class="sxs-lookup"><span data-stu-id="14816-112"><span id="cb"></span><span id="CB"></span>*cb*</span></span>
</dt> <dd>

<span data-ttu-id="14816-113">Dimensione, in byte, del blocco di memoria.</span><span class="sxs-lookup"><span data-stu-id="14816-113">Size, in bytes, of the block of memory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14816-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="14816-114">Return Value</span></span>

<span data-ttu-id="14816-115">Restituisce il numero di byte utilizzati dal compressore se ha esito positivo o zero in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="14816-115">Returns the number of bytes used by the compressor if successful or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="14816-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="14816-116">Remarks</span></span>

<span data-ttu-id="14816-117">Le informazioni usate da questo messaggio sono private e specifiche di un compressore specificato.</span><span class="sxs-lookup"><span data-stu-id="14816-117">The information used by this message is private and specific to a given compressor.</span></span> <span data-ttu-id="14816-118">Le applicazioni client devono utilizzare questo messaggio solo per ripristinare le informazioni ottenute in precedenza con il messaggio [**ICM \_ GetState**](icm-getstate.md) e utilizzare il messaggio di configurazione [**ICM \_**](icm-configure.md) per modificare la configurazione di un driver di compressione video.</span><span class="sxs-lookup"><span data-stu-id="14816-118">Client applications should use this message only to restore information previously obtained with the [**ICM\_GETSTATE**](icm-getstate.md) message and should use the [**ICM\_CONFIGURE**](icm-configure.md) message to adjust the configuration of a video compression driver.</span></span>

## <a name="requirements"></a><span data-ttu-id="14816-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="14816-119">Requirements</span></span>



| <span data-ttu-id="14816-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="14816-120">Requirement</span></span> | <span data-ttu-id="14816-121">Valore</span><span class="sxs-lookup"><span data-stu-id="14816-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="14816-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="14816-122">Minimum supported client</span></span><br/> | <span data-ttu-id="14816-123">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="14816-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="14816-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="14816-124">Minimum supported server</span></span><br/> | <span data-ttu-id="14816-125">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="14816-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="14816-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="14816-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="14816-127"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="14816-127"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14816-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="14816-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14816-129">Gestione compressione video</span><span class="sxs-lookup"><span data-stu-id="14816-129">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="14816-130">Messaggi di compressione video</span><span class="sxs-lookup"><span data-stu-id="14816-130">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





