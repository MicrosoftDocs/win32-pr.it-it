---
title: Messaggio di ICM_COMPRESS_QUERY (VFW. h)
description: Il \_ messaggio ICM compress \_ query Invia un driver di compressione video per determinare se supporta un formato di input specifico o se può comprimere un formato di input specifico in un formato di output specifico.
ms.assetid: 6d0e735e-8252-4507-b8be-1ba87774f637
keywords:
- ICM_COMPRESS_QUERY messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- ICM_COMPRESS_QUERY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00a00482cc39f21ef6ddfb241f0534924c503200
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302274"
---
# <a name="icm_compress_query-message"></a><span data-ttu-id="580fa-104">\_Messaggio di \_ query compressi ICM</span><span class="sxs-lookup"><span data-stu-id="580fa-104">ICM\_COMPRESS\_QUERY message</span></span>

<span data-ttu-id="580fa-105">Il messaggio **ICM \_ compress \_ query** Invia un driver di compressione video per determinare se supporta un formato di input specifico o se può comprimere un formato di input specifico in un formato di output specifico.</span><span class="sxs-lookup"><span data-stu-id="580fa-105">The **ICM\_COMPRESS\_QUERY** message queries a video compression driver to determine if it supports a specific input format or if it can compress a specific input format to a specific output format.</span></span> <span data-ttu-id="580fa-106">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**ICCompressQuery**](/windows/desktop/api/Vfw/nf-vfw-iccompressquery) .</span><span class="sxs-lookup"><span data-stu-id="580fa-106">You can send this message explicitly or by using the [**ICCompressQuery**](/windows/desktop/api/Vfw/nf-vfw-iccompressquery) macro.</span></span>


```C++
ICM_COMPRESS_QUERY 
wParam = (DWORD_PTR) (LPVOID) lpbiInput; 
lParam = (DWORD_PTR) (LPVOID) lpbiOutput; 
```



## <a name="parameters"></a><span data-ttu-id="580fa-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="580fa-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="580fa-108"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*</span><span class="sxs-lookup"><span data-stu-id="580fa-108"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*</span></span>
</dt> <dd>

<span data-ttu-id="580fa-109">Puntatore a una struttura [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) contenente il formato di input.</span><span class="sxs-lookup"><span data-stu-id="580fa-109">Pointer to a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure containing the input format.</span></span>

</dd> <dt>

<span data-ttu-id="580fa-110"><span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*lpbiOutput*</span><span class="sxs-lookup"><span data-stu-id="580fa-110"><span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*lpbiOutput*</span></span>
</dt> <dd>

<span data-ttu-id="580fa-111">Puntatore a una struttura [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) contenente il formato di output.</span><span class="sxs-lookup"><span data-stu-id="580fa-111">Pointer to a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure containing the output format.</span></span> <span data-ttu-id="580fa-112">È possibile specificare zero per questo parametro per indicare che il formato di output è accettabile.</span><span class="sxs-lookup"><span data-stu-id="580fa-112">You can specify zero for this parameter to indicate any output format is acceptable.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="580fa-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="580fa-113">Return Value</span></span>

<span data-ttu-id="580fa-114">Restituisce ICERR \_ OK se la compressione specificata è supportata o ICERR \_ BADFORMAT in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="580fa-114">Returns ICERR\_OK if the specified compression is supported or ICERR\_BADFORMAT otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="580fa-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="580fa-115">Remarks</span></span>

<span data-ttu-id="580fa-116">Quando un driver riceve questo messaggio, deve esaminare la struttura [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) associata a *lpbiInput* per determinare se è possibile comprimere il formato di input.</span><span class="sxs-lookup"><span data-stu-id="580fa-116">When a driver receives this message, it should examine the [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure associated with *lpbiInput* to determine if it can compress the input format.</span></span>

## <a name="requirements"></a><span data-ttu-id="580fa-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="580fa-117">Requirements</span></span>



| <span data-ttu-id="580fa-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="580fa-118">Requirement</span></span> | <span data-ttu-id="580fa-119">Valore</span><span class="sxs-lookup"><span data-stu-id="580fa-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="580fa-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="580fa-120">Minimum supported client</span></span><br/> | <span data-ttu-id="580fa-121">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="580fa-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="580fa-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="580fa-122">Minimum supported server</span></span><br/> | <span data-ttu-id="580fa-123">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="580fa-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="580fa-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="580fa-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="580fa-125"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="580fa-125"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="580fa-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="580fa-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="580fa-127">Gestione compressione video</span><span class="sxs-lookup"><span data-stu-id="580fa-127">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="580fa-128">Messaggi di compressione video</span><span class="sxs-lookup"><span data-stu-id="580fa-128">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

