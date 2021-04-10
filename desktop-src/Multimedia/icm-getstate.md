---
title: Messaggio di ICM_GETSTATE (VFW. h)
description: Il \_ messaggio ICM GetState esegue una query su un driver di compressione video per restituire la configurazione corrente in un blocco di memoria o per determinare la quantità di memoria necessaria per recuperare le informazioni di configurazione.
ms.assetid: 4b77e294-f3aa-45f9-a4f4-f103b83eae8d
keywords:
- ICM_GETSTATE messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- ICM_GETSTATE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b6a45dcde627a02c1a4a402ea9a2a725f0429a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121683"
---
# <a name="icm_getstate-message"></a><span data-ttu-id="b8cab-104">\_Messaggio ICM GETstate</span><span class="sxs-lookup"><span data-stu-id="b8cab-104">ICM\_GETSTATE message</span></span>

<span data-ttu-id="b8cab-105">Il messaggio **ICM \_ GetState** esegue una query su un driver di compressione video per restituire la configurazione corrente in un blocco di memoria o per determinare la quantità di memoria necessaria per recuperare le informazioni di configurazione.</span><span class="sxs-lookup"><span data-stu-id="b8cab-105">The **ICM\_GETSTATE** message queries a video compression driver to return its current configuration in a block of memory or to determine the amount of memory required to retrieve the configuration information.</span></span> <span data-ttu-id="b8cab-106">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**ICGetState**](/windows/desktop/api/Vfw/nf-vfw-icgetstate) .</span><span class="sxs-lookup"><span data-stu-id="b8cab-106">You can send this message explicitly or by using the [**ICGetState**](/windows/desktop/api/Vfw/nf-vfw-icgetstate) macro.</span></span>


```C++
ICM_GETSTATE 
wParam = (DWORD_PTR) (LPVOID) pv; 
lParam = (DWORD_PTR) cb; 
```



## <a name="parameters"></a><span data-ttu-id="b8cab-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="b8cab-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8cab-108"><span id="pv"></span><span id="PV"></span>*PV*</span><span class="sxs-lookup"><span data-stu-id="b8cab-108"><span id="pv"></span><span id="PV"></span>*pv*</span></span>
</dt> <dd>

<span data-ttu-id="b8cab-109">Puntatore a un blocco di memoria per contenere le informazioni di configurazione correnti.</span><span class="sxs-lookup"><span data-stu-id="b8cab-109">Pointer to a block of memory to contain the current configuration information.</span></span> <span data-ttu-id="b8cab-110">È possibile specificare **null** per questo parametro per determinare la quantità di memoria richiesta per le informazioni di configurazione, come in [**ICGetStateSize**](/windows/desktop/api/Vfw/nf-vfw-icgetstatesize).</span><span class="sxs-lookup"><span data-stu-id="b8cab-110">You can specify **NULL** for this parameter to determine the amount of memory required for the configuration information, as in [**ICGetStateSize**](/windows/desktop/api/Vfw/nf-vfw-icgetstatesize).</span></span>

</dd> <dt>

<span data-ttu-id="b8cab-111"><span id="cb"></span><span id="CB"></span>*CB*</span><span class="sxs-lookup"><span data-stu-id="b8cab-111"><span id="cb"></span><span id="CB"></span>*cb*</span></span>
</dt> <dd>

<span data-ttu-id="b8cab-112">Dimensione, in byte, del blocco di memoria.</span><span class="sxs-lookup"><span data-stu-id="b8cab-112">Size, in bytes, of the block of memory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8cab-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b8cab-113">Return Value</span></span>

<span data-ttu-id="b8cab-114">Se *PV* è **null**, restituisce la quantità di memoria, in byte, necessaria per le informazioni di configurazione.</span><span class="sxs-lookup"><span data-stu-id="b8cab-114">If *pv* is **NULL**, returns the amount of memory, in bytes, required for configuration information.</span></span>

<span data-ttu-id="b8cab-115">Se *PV* non è **null**, restituisce ICERR \_ OK se ha esito positivo o un errore in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="b8cab-115">If *pv* is not **NULL**, returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="b8cab-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="b8cab-116">Remarks</span></span>

<span data-ttu-id="b8cab-117">La struttura utilizzata per rappresentare le informazioni di configurazione è specifica del driver e viene definita dal driver.</span><span class="sxs-lookup"><span data-stu-id="b8cab-117">The structure used to represent configuration information is driver specific and is defined by the driver.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8cab-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b8cab-118">Requirements</span></span>



| <span data-ttu-id="b8cab-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="b8cab-119">Requirement</span></span> | <span data-ttu-id="b8cab-120">Valore</span><span class="sxs-lookup"><span data-stu-id="b8cab-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="b8cab-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b8cab-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b8cab-122">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b8cab-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="b8cab-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b8cab-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b8cab-124">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b8cab-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="b8cab-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b8cab-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="b8cab-126"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="b8cab-126"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8cab-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b8cab-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8cab-128">Gestione compressione video</span><span class="sxs-lookup"><span data-stu-id="b8cab-128">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="b8cab-129">Messaggi di compressione video</span><span class="sxs-lookup"><span data-stu-id="b8cab-129">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





