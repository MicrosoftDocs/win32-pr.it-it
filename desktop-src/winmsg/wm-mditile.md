---
description: Un'applicazione invia il \_ messaggio WM MDITILE a una finestra del client di interfaccia a documenti multipli (MDI) per disporre tutte le finestre figlio MDI in un formato di riquadro.
ms.assetid: a480ba61-807e-4d0e-bda2-f1876e0bb13c
title: Messaggio WM_MDITILE (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0cf7ee38fbb3622e2d17bf4cea5a28b6b492a244
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226038"
---
# <a name="wm_mditile-message"></a><span data-ttu-id="fce18-103">\_Messaggio MDITILE WM</span><span class="sxs-lookup"><span data-stu-id="fce18-103">WM\_MDITILE message</span></span>

<span data-ttu-id="fce18-104">Un'applicazione invia il messaggio **WM \_ MDITILE** a una finestra del client di interfaccia a documenti multipli (MDI) per disporre tutte le finestre figlio MDI in un formato di riquadro.</span><span class="sxs-lookup"><span data-stu-id="fce18-104">An application sends the **WM\_MDITILE** message to a multiple-document interface (MDI) client window to arrange all of its MDI child windows in a tile format.</span></span>


```C++
#define WM_MDITILE                      0x0226
```



## <a name="parameters"></a><span data-ttu-id="fce18-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="fce18-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fce18-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fce18-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fce18-107">Opzione di affiancamento.</span><span class="sxs-lookup"><span data-stu-id="fce18-107">The tiling option.</span></span> <span data-ttu-id="fce18-108">Questo parametro può essere uno dei valori seguenti, combinati facoltativamente con **MDITILE \_ SKIPDISABLED** per impedire che vengano affiancate le finestre figlio MDI disabilitate.</span><span class="sxs-lookup"><span data-stu-id="fce18-108">This parameter can be one of the following values, optionally combined with **MDITILE\_SKIPDISABLED** to prevent disabled MDI child windows from being tiled.</span></span>



| <span data-ttu-id="fce18-109">Valore</span><span class="sxs-lookup"><span data-stu-id="fce18-109">Value</span></span>                                                                                                                                                                                                                                    | <span data-ttu-id="fce18-110">Significato</span><span class="sxs-lookup"><span data-stu-id="fce18-110">Meaning</span></span>                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="MDITILE_HORIZONTAL"></span><span id="mditile_horizontal"></span><dl> <span data-ttu-id="fce18-111"><dt>**MDITILE \_**</dt> <dt>0x0001</dt> orizzontale</span><span class="sxs-lookup"><span data-stu-id="fce18-111"><dt>**MDITILE\_HORIZONTAL**</dt> <dt>0x0001</dt></span></span> </dl> | <span data-ttu-id="fce18-112">Affianca le finestre orizzontalmente.</span><span class="sxs-lookup"><span data-stu-id="fce18-112">Tiles windows horizontally.</span></span><br/> |
| <span id="MDITILE_VERTICAL"></span><span id="mditile_vertical"></span><dl> <span data-ttu-id="fce18-113"><dt>**MDITILE \_**</dt> <dt>0x0000</dt> verticali</span><span class="sxs-lookup"><span data-stu-id="fce18-113"><dt>**MDITILE\_VERTICAL**</dt> <dt>0x0000</dt></span></span> </dl>       | <span data-ttu-id="fce18-114">Affianca le finestre verticalmente.</span><span class="sxs-lookup"><span data-stu-id="fce18-114">Tiles windows vertically.</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="fce18-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fce18-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fce18-116">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="fce18-116">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fce18-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fce18-117">Return value</span></span>

<span data-ttu-id="fce18-118">Tipo: **bool**</span><span class="sxs-lookup"><span data-stu-id="fce18-118">Type: **BOOL**</span></span>

<span data-ttu-id="fce18-119">Se il messaggio ha esito positivo, il valore restituito è **true**.</span><span class="sxs-lookup"><span data-stu-id="fce18-119">If the message succeeds, the return value is **TRUE**.</span></span>

<span data-ttu-id="fce18-120">Se il messaggio ha esito negativo, il valore restituito è **false**.</span><span class="sxs-lookup"><span data-stu-id="fce18-120">If the message fails, the return value is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="fce18-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fce18-121">Requirements</span></span>



| <span data-ttu-id="fce18-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="fce18-122">Requirement</span></span> | <span data-ttu-id="fce18-123">Valore</span><span class="sxs-lookup"><span data-stu-id="fce18-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fce18-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fce18-124">Minimum supported client</span></span><br/> | <span data-ttu-id="fce18-125">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="fce18-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="fce18-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fce18-126">Minimum supported server</span></span><br/> | <span data-ttu-id="fce18-127">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="fce18-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="fce18-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fce18-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="fce18-129"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fce18-129"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fce18-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fce18-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="fce18-131">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="fce18-131">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="fce18-132">**\_MDICASCADE WM**</span><span class="sxs-lookup"><span data-stu-id="fce18-132">**WM\_MDICASCADE**</span></span>](wm-mdicascade.md)
</dt> <dt>

[<span data-ttu-id="fce18-133">**\_MDIICONARRANGE WM**</span><span class="sxs-lookup"><span data-stu-id="fce18-133">**WM\_MDIICONARRANGE**</span></span>](wm-mdiiconarrange.md)
</dt> <dt>

<span data-ttu-id="fce18-134">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="fce18-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="fce18-135">Interfaccia a documenti multipli</span><span class="sxs-lookup"><span data-stu-id="fce18-135">Multiple Document Interface</span></span>](multiple-document-interface.md)
</dt> </dl>

 

 




