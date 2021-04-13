---
description: Un'applicazione invia il \_ messaggio WM MDICASCADE a una finestra del client di interfaccia a documenti multipli (MDI) per disporre tutte le finestre figlio in un formato Cascade.
ms.assetid: 33d04859-4220-40a6-be46-74a812a44ca8
title: Messaggio WM_MDICASCADE (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6208ce924ab6185399f3f673a435e1fbaca2741
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343201"
---
# <a name="wm_mdicascade-message"></a><span data-ttu-id="0900f-103">\_Messaggio MDICASCADE WM</span><span class="sxs-lookup"><span data-stu-id="0900f-103">WM\_MDICASCADE message</span></span>

<span data-ttu-id="0900f-104">Un'applicazione invia il messaggio **WM \_ MDICASCADE** a una finestra del client di interfaccia a documenti multipli (MDI) per disporre tutte le finestre figlio in un formato Cascade.</span><span class="sxs-lookup"><span data-stu-id="0900f-104">An application sends the **WM\_MDICASCADE** message to a multiple-document interface (MDI) client window to arrange all its child windows in a cascade format.</span></span>


```C++
#define WM_MDICASCADE                   0x0227
```



## <a name="parameters"></a><span data-ttu-id="0900f-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="0900f-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0900f-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0900f-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0900f-107">Comportamento di propagazione.</span><span class="sxs-lookup"><span data-stu-id="0900f-107">The cascade behavior.</span></span> <span data-ttu-id="0900f-108">Il parametro può essere costituito da uno o più dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="0900f-108">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="0900f-109">Valore</span><span class="sxs-lookup"><span data-stu-id="0900f-109">Value</span></span>                                                                                                                                                                                                                                          | <span data-ttu-id="0900f-110">Significato</span><span class="sxs-lookup"><span data-stu-id="0900f-110">Meaning</span></span>                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <span id="MDITILE_SKIPDISABLED"></span><span id="mditile_skipdisabled"></span><dl> <span data-ttu-id="0900f-111"><dt>**MDITILE \_**</dt> <dt>0x0002</dt> SKIPDISABLED</span><span class="sxs-lookup"><span data-stu-id="0900f-111"><dt>**MDITILE\_SKIPDISABLED**</dt> <dt>0x0002</dt></span></span> </dl> | <span data-ttu-id="0900f-112">Impedisce la propagazione delle finestre figlio MDI disabilitate.</span><span class="sxs-lookup"><span data-stu-id="0900f-112">Prevents disabled MDI child windows from being cascaded.</span></span> <br/> |
| <span id="MDITILE_ZORDER"></span><span id="mditile_zorder"></span><dl> <span data-ttu-id="0900f-113"><dt>**MDITILE \_**</dt> <dt>0x0004</dt> ZOrder</span><span class="sxs-lookup"><span data-stu-id="0900f-113"><dt>**MDITILE\_ZORDER**</dt> <dt>0x0004</dt></span></span> </dl>                   | <span data-ttu-id="0900f-114">Dispone le finestre in z order.</span><span class="sxs-lookup"><span data-stu-id="0900f-114">Arranges the windows in Z order.</span></span><br/>                          |



 

</dd> <dt>

<span data-ttu-id="0900f-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0900f-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0900f-116">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="0900f-116">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0900f-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0900f-117">Return value</span></span>

<span data-ttu-id="0900f-118">Tipo: **bool**</span><span class="sxs-lookup"><span data-stu-id="0900f-118">Type: **BOOL**</span></span>

<span data-ttu-id="0900f-119">Se il messaggio ha esito positivo, il valore restituito è **true**.</span><span class="sxs-lookup"><span data-stu-id="0900f-119">If the message succeeds, the return value is **TRUE**.</span></span>

<span data-ttu-id="0900f-120">Se il messaggio ha esito negativo, il valore restituito è **false**.</span><span class="sxs-lookup"><span data-stu-id="0900f-120">If the message fails, the return value is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="0900f-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0900f-121">Requirements</span></span>



| <span data-ttu-id="0900f-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="0900f-122">Requirement</span></span> | <span data-ttu-id="0900f-123">Valore</span><span class="sxs-lookup"><span data-stu-id="0900f-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0900f-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0900f-124">Minimum supported client</span></span><br/> | <span data-ttu-id="0900f-125">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="0900f-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="0900f-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0900f-126">Minimum supported server</span></span><br/> | <span data-ttu-id="0900f-127">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="0900f-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="0900f-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0900f-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="0900f-129"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0900f-129"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0900f-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0900f-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="0900f-131">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="0900f-131">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="0900f-132">**\_MDIICONARRANGE WM**</span><span class="sxs-lookup"><span data-stu-id="0900f-132">**WM\_MDIICONARRANGE**</span></span>](wm-mdiiconarrange.md)
</dt> <dt>

[<span data-ttu-id="0900f-133">**\_MDITILE WM**</span><span class="sxs-lookup"><span data-stu-id="0900f-133">**WM\_MDITILE**</span></span>](wm-mditile.md)
</dt> <dt>

<span data-ttu-id="0900f-134">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="0900f-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="0900f-135">Interfaccia a documenti multipli</span><span class="sxs-lookup"><span data-stu-id="0900f-135">Multiple Document Interface</span></span>](multiple-document-interface.md)
</dt> </dl>

 

 




