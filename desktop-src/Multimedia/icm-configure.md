---
title: Messaggio di ICM_CONFIGURE (VFW. h)
description: Il \_ messaggio ICM Configure invia una notifica a un driver di compressione video per visualizzare la finestra di dialogo di configurazione oppure esegue una query su un driver di compressione video per determinare se dispone di una finestra di dialogo di configurazione.
ms.assetid: 9760788e-fa66-44d7-bda6-aa9536143774
keywords:
- ICM_CONFIGURE messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- ICM_CONFIGURE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9faae26fcf132abfa424b0db7a88670735d30727
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302271"
---
# <a name="icm_configure-message"></a><span data-ttu-id="01b57-104">\_Messaggio di configurazione ICM</span><span class="sxs-lookup"><span data-stu-id="01b57-104">ICM\_CONFIGURE message</span></span>

<span data-ttu-id="01b57-105">Il messaggio **ICM \_ Configure** invia una notifica a un driver di compressione video per visualizzare la finestra di dialogo di configurazione oppure esegue una query su un driver di compressione video per determinare se dispone di una finestra di dialogo di configurazione.</span><span class="sxs-lookup"><span data-stu-id="01b57-105">The **ICM\_CONFIGURE** message notifies a video compression driver to display its configuration dialog box or queries a video compression driver to determine if it has a configuration dialog box.</span></span> <span data-ttu-id="01b57-106">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**ICConfigure**](/windows/desktop/api/Vfw/nf-vfw-icconfigure) .</span><span class="sxs-lookup"><span data-stu-id="01b57-106">You can send this message explicitly or by using the [**ICConfigure**](/windows/desktop/api/Vfw/nf-vfw-icconfigure) macro.</span></span>


```C++
ICM_CONFIGURE 
wParam = (DWORD_PTR) (UINT_PTR) hwnd; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="01b57-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="01b57-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01b57-108"><span id="hwnd"></span><span id="HWND"></span>*HWND*</span><span class="sxs-lookup"><span data-stu-id="01b57-108"><span id="hwnd"></span><span id="HWND"></span>*hwnd*</span></span>
</dt> <dd>

<span data-ttu-id="01b57-109">Handle per la finestra padre della finestra di dialogo visualizzata.</span><span class="sxs-lookup"><span data-stu-id="01b57-109">Handle to the parent window of the displayed dialog box.</span></span> <span data-ttu-id="01b57-110">È possibile determinare se un driver dispone di una finestra di dialogo di configurazione specificando 1 in questo parametro, come nella macro [**ICQueryConfigure**](/windows/desktop/api/Vfw/nf-vfw-icqueryconfigure) .</span><span class="sxs-lookup"><span data-stu-id="01b57-110">You can determine if a driver has a configuration dialog box by specifying  1 in this parameter, as in the [**ICQueryConfigure**](/windows/desktop/api/Vfw/nf-vfw-icqueryconfigure) macro.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01b57-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="01b57-111">Return Value</span></span>

<span data-ttu-id="01b57-112">Restituisce ICERR \_ OK se il driver supporta questo messaggio o ICERR non \_ supportato in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="01b57-112">Returns ICERR\_OK if the driver supports this message or ICERR\_UNSUPPORTED otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="01b57-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="01b57-113">Remarks</span></span>

<span data-ttu-id="01b57-114">Questo messaggio è diverso dal messaggio [**di \_ configurazione di DRV**](drv-configure.md) usato per la configurazione hardware.</span><span class="sxs-lookup"><span data-stu-id="01b57-114">This message is different from the [**DRV\_CONFIGURE**](drv-configure.md) message used for hardware configuration.</span></span> <span data-ttu-id="01b57-115">La finestra di dialogo per questo messaggio deve consentire all'utente di impostare e modificare lo stato interno a cui fanno riferimento i messaggi di stato [**MCI \_**](icm-getstate.md) GetState e [**ICM \_**](icm-setstate.md) .</span><span class="sxs-lookup"><span data-stu-id="01b57-115">The dialog box for this message should let the user set and edit the internal state referenced by the [**ICM\_GETSTATE**](icm-getstate.md) and [**ICM\_SETSTATE**](icm-setstate.md) messages.</span></span> <span data-ttu-id="01b57-116">Questa finestra di dialogo, ad esempio, può consentire all'utente di modificare i parametri che interessano il livello di qualità e altre opzioni di compressione simili.</span><span class="sxs-lookup"><span data-stu-id="01b57-116">For example, this dialog box can let the user change parameters affecting the quality level and other similar compression options.</span></span>

## <a name="requirements"></a><span data-ttu-id="01b57-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="01b57-117">Requirements</span></span>



| <span data-ttu-id="01b57-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="01b57-118">Requirement</span></span> | <span data-ttu-id="01b57-119">Valore</span><span class="sxs-lookup"><span data-stu-id="01b57-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="01b57-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="01b57-120">Minimum supported client</span></span><br/> | <span data-ttu-id="01b57-121">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="01b57-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="01b57-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="01b57-122">Minimum supported server</span></span><br/> | <span data-ttu-id="01b57-123">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="01b57-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="01b57-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="01b57-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="01b57-125"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="01b57-125"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01b57-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="01b57-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01b57-127">Gestione compressione video</span><span class="sxs-lookup"><span data-stu-id="01b57-127">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="01b57-128">Messaggi di compressione video</span><span class="sxs-lookup"><span data-stu-id="01b57-128">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





