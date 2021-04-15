---
title: Messaggio di ICM_DRAW_QUERY (VFW. h)
description: Il \_ \_ messaggio di query di estrazione ICM esegue una query su un driver di rendering per determinare se è possibile eseguire il rendering dei dati in un formato specifico. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro ICDrawQuery.
ms.assetid: b829a04b-c1be-47c6-96e9-a6dc6f802811
keywords:
- ICM_DRAW_QUERY messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- ICM_DRAW_QUERY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27266484cffa503583df32b60c6e8a0c04f344f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477255"
---
# <a name="icm_draw_query-message"></a><span data-ttu-id="cd61a-105">Messaggio di query di \_ estrazione ICM \_</span><span class="sxs-lookup"><span data-stu-id="cd61a-105">ICM\_DRAW\_QUERY message</span></span>

<span data-ttu-id="cd61a-106">Il messaggio di **\_ \_ query di estrazione ICM** esegue una query su un driver di rendering per determinare se è possibile eseguire il rendering dei dati in un formato specifico.</span><span class="sxs-lookup"><span data-stu-id="cd61a-106">The **ICM\_DRAW\_QUERY** message queries a rendering driver to determine if it can render data in a specific format.</span></span> <span data-ttu-id="cd61a-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**ICDrawQuery**](/windows/desktop/api/Vfw/nf-vfw-icdrawquery) .</span><span class="sxs-lookup"><span data-stu-id="cd61a-107">You can send this message explicitly or by using the [**ICDrawQuery**](/windows/desktop/api/Vfw/nf-vfw-icdrawquery) macro.</span></span>


```C++
ICM_DRAW_QUERY 
wParam = (DWORD_PTR) (LPVOID) lpbiInput; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="cd61a-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="cd61a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd61a-109"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*</span><span class="sxs-lookup"><span data-stu-id="cd61a-109"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*</span></span>
</dt> <dd>

<span data-ttu-id="cd61a-110">Puntatore a una struttura [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) contenente il formato di input.</span><span class="sxs-lookup"><span data-stu-id="cd61a-110">Pointer to a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure containing the input format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd61a-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cd61a-111">Return Value</span></span>

<span data-ttu-id="cd61a-112">Restituisce ICERR \_ OK se il driver è in grado di eseguire il rendering dei dati nel formato specificato o in ICERR \_ BADFORMAT in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="cd61a-112">Returns ICERR\_OK if the driver can render data in the specified format or ICERR\_BADFORMAT otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="cd61a-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="cd61a-113">Remarks</span></span>

<span data-ttu-id="cd61a-114">Questo messaggio è diverso dal messaggio [**di \_ \_ inizio del progetto ICM**](icm-draw-begin.md) in quanto esegue una query sul driver in senso generale.</span><span class="sxs-lookup"><span data-stu-id="cd61a-114">This message differs from the [**ICM\_DRAW\_BEGIN**](icm-draw-begin.md) message in that it queries the driver in a general sense.</span></span> <span data-ttu-id="cd61a-115">**ICM \_ L' \_ inizio dell'estrazione** determina se il driver può creare i dati utilizzando il formato specificato in condizioni specifiche, ad esempio l'estensione dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="cd61a-115">**ICM\_DRAW\_BEGIN** determines if the driver can draw the data using the specified format under specific conditions, such as stretching the image.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd61a-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cd61a-116">Requirements</span></span>



| <span data-ttu-id="cd61a-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd61a-117">Requirement</span></span> | <span data-ttu-id="cd61a-118">Valore</span><span class="sxs-lookup"><span data-stu-id="cd61a-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="cd61a-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cd61a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="cd61a-120">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="cd61a-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="cd61a-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cd61a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="cd61a-122">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="cd61a-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="cd61a-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cd61a-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="cd61a-124"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="cd61a-124"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd61a-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cd61a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd61a-126">Gestione compressione video</span><span class="sxs-lookup"><span data-stu-id="cd61a-126">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="cd61a-127">Messaggi di compressione video</span><span class="sxs-lookup"><span data-stu-id="cd61a-127">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

