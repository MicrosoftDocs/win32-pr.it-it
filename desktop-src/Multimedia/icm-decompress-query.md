---
title: Messaggio di ICM_DECOMPRESS_QUERY (VFW. h)
description: Il \_ messaggio di query decomprimere ICM \_ esegue una query su un driver di decompressione video per determinare se supporta un formato di input specifico o se può decomprimere un formato di input specifico in un formato di output specifico.
ms.assetid: 622dd1de-3f7a-4841-913c-282c2ad766f4
keywords:
- ICM_DECOMPRESS_QUERY messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- ICM_DECOMPRESS_QUERY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 838c946a38f9c2fda0c9178a36107af73f539a03
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302267"
---
# <a name="icm_decompress_query-message"></a><span data-ttu-id="dbff7-104">\_Messaggio di query di decompressione ICM \_</span><span class="sxs-lookup"><span data-stu-id="dbff7-104">ICM\_DECOMPRESS\_QUERY message</span></span>

<span data-ttu-id="dbff7-105">Il messaggio di **\_ \_ query decomprimere ICM** esegue una query su un driver di decompressione video per determinare se supporta un formato di input specifico o se può decomprimere un formato di input specifico in un formato di output specifico.</span><span class="sxs-lookup"><span data-stu-id="dbff7-105">The **ICM\_DECOMPRESS\_QUERY** message queries a video decompression driver to determine if it supports a specific input format or if it can decompress a specific input format to a specific output format.</span></span> <span data-ttu-id="dbff7-106">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**ICDecompressQuery**](/windows/desktop/api/Vfw/nf-vfw-icdecompressquery) .</span><span class="sxs-lookup"><span data-stu-id="dbff7-106">You can send this message explicitly or by using the [**ICDecompressQuery**](/windows/desktop/api/Vfw/nf-vfw-icdecompressquery) macro.</span></span>


```C++
ICM_DECOMPRESS_QUERY 
wParam = (DWORD_PTR) (LPVOID) lpbiInput; 
lParam = (DWORD_PTR) (LPVOID) lpbiOutput; 
```



## <a name="parameters"></a><span data-ttu-id="dbff7-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="dbff7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dbff7-108"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*</span><span class="sxs-lookup"><span data-stu-id="dbff7-108"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*</span></span>
</dt> <dd>

<span data-ttu-id="dbff7-109">Puntatore a una struttura [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) contenente il formato di input.</span><span class="sxs-lookup"><span data-stu-id="dbff7-109">Pointer to a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure containing the input format.</span></span>

</dd> <dt>

<span data-ttu-id="dbff7-110"><span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*lpbiOutput*</span><span class="sxs-lookup"><span data-stu-id="dbff7-110"><span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*lpbiOutput*</span></span>
</dt> <dd>

<span data-ttu-id="dbff7-111">Puntatore a una struttura [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) contenente il formato di output.</span><span class="sxs-lookup"><span data-stu-id="dbff7-111">Pointer to a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure containing the output format.</span></span> <span data-ttu-id="dbff7-112">È possibile specificare zero per questo parametro per indicare che il formato di output è accettabile.</span><span class="sxs-lookup"><span data-stu-id="dbff7-112">You can specify zero for this parameter to indicate any output format is acceptable.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dbff7-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="dbff7-113">Return Value</span></span>

<span data-ttu-id="dbff7-114">Restituisce ICERR \_ OK se la decompressione specificata è supportata o ICERR \_ BADFORMAT in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="dbff7-114">Returns ICERR\_OK if the specified decompression is supported or ICERR\_BADFORMAT otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="dbff7-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dbff7-115">Requirements</span></span>



| <span data-ttu-id="dbff7-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="dbff7-116">Requirement</span></span> | <span data-ttu-id="dbff7-117">Valore</span><span class="sxs-lookup"><span data-stu-id="dbff7-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="dbff7-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dbff7-118">Minimum supported client</span></span><br/> | <span data-ttu-id="dbff7-119">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="dbff7-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="dbff7-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dbff7-120">Minimum supported server</span></span><br/> | <span data-ttu-id="dbff7-121">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="dbff7-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="dbff7-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="dbff7-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="dbff7-123"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="dbff7-123"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dbff7-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dbff7-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbff7-125">Gestione compressione video</span><span class="sxs-lookup"><span data-stu-id="dbff7-125">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="dbff7-126">Messaggi di compressione video</span><span class="sxs-lookup"><span data-stu-id="dbff7-126">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

