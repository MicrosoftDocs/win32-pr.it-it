---
title: Messaggio di ICM_DRAW_CHANGEPALETTE (VFW. h)
description: Il \_ messaggio CHANGEPALETTE per il progetto ICM \_ notifica a un driver di rendering che la tavolozza dei film sta cambiando. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro ICDrawChangePalette.
ms.assetid: 974fc0d8-d0c7-4a82-af84-68b53f753259
keywords:
- ICM_DRAW_CHANGEPALETTE messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- ICM_DRAW_CHANGEPALETTE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6364abb2c535158b2e64ff311041b00490c5958c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873985"
---
# <a name="icm_draw_changepalette-message"></a><span data-ttu-id="3be10-105">\_ \_ Messaggio CHANGEPALETTE per il progetto ICM</span><span class="sxs-lookup"><span data-stu-id="3be10-105">ICM\_DRAW\_CHANGEPALETTE message</span></span>

<span data-ttu-id="3be10-106">Il **messaggio \_ \_ CHANGEPALETTE per il progetto ICM** notifica a un driver di rendering che la tavolozza dei film sta cambiando.</span><span class="sxs-lookup"><span data-stu-id="3be10-106">The **ICM\_DRAW\_CHANGEPALETTE** message notifies a rendering driver that the movie palette is changing.</span></span> <span data-ttu-id="3be10-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**ICDrawChangePalette**](/windows/desktop/api/Vfw/nf-vfw-icdrawchangepalette) .</span><span class="sxs-lookup"><span data-stu-id="3be10-107">You can send this message explicitly or by using the [**ICDrawChangePalette**](/windows/desktop/api/Vfw/nf-vfw-icdrawchangepalette) macro.</span></span>


```C++
ICM_DRAW_CHANGEPALETTE 
wParam = (DWORD_PTR) (LPVOID) lpbiInput; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="3be10-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="3be10-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3be10-109"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*</span><span class="sxs-lookup"><span data-stu-id="3be10-109"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*</span></span>
</dt> <dd>

<span data-ttu-id="3be10-110">Puntatore a una struttura [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) contenente il nuovo formato e la tabella dei colori facoltativa.</span><span class="sxs-lookup"><span data-stu-id="3be10-110">Pointer to a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure containing the new format and optional color table.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3be10-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3be10-111">Return Value</span></span>

<span data-ttu-id="3be10-112">Restituisce ICERR \_ OK se ha esito positivo o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="3be10-112">Returns ICERR\_OK if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="3be10-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="3be10-113">Remarks</span></span>

<span data-ttu-id="3be10-114">Questo messaggio deve essere supportato da gestori di rendering installabili che preferiscono una struttura interna che include una tavolozza.</span><span class="sxs-lookup"><span data-stu-id="3be10-114">This message should be supported by installable rendering handlers that draw DIBs with an internal structure that includes a palette.</span></span>

## <a name="requirements"></a><span data-ttu-id="3be10-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3be10-115">Requirements</span></span>



| <span data-ttu-id="3be10-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="3be10-116">Requirement</span></span> | <span data-ttu-id="3be10-117">Valore</span><span class="sxs-lookup"><span data-stu-id="3be10-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="3be10-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3be10-118">Minimum supported client</span></span><br/> | <span data-ttu-id="3be10-119">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3be10-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="3be10-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3be10-120">Minimum supported server</span></span><br/> | <span data-ttu-id="3be10-121">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3be10-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="3be10-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3be10-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="3be10-123"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="3be10-123"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3be10-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3be10-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3be10-125">Gestione compressione video</span><span class="sxs-lookup"><span data-stu-id="3be10-125">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="3be10-126">Messaggi di compressione video</span><span class="sxs-lookup"><span data-stu-id="3be10-126">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

