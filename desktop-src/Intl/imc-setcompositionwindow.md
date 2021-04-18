---
description: Indica a una finestra IME di impostare lo stile della finestra di composizione. Per inviare questo comando, l'applicazione usa il \_ \_ messaggio di controllo IME WM con le impostazioni dei parametri mostrate di seguito.
ms.assetid: 19b99228-a1fc-4cd5-8f37-5462bf767f85
title: Comando IMC_SETCOMPOSITIONWINDOW (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b06c53b1ff2ec343d6382dd48d0d4108cf403c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307862"
---
# <a name="imc_setcompositionwindow-command"></a><span data-ttu-id="c65de-104">\_Comando SETCOMPOSITIONWINDOW IMC</span><span class="sxs-lookup"><span data-stu-id="c65de-104">IMC\_SETCOMPOSITIONWINDOW command</span></span>

<span data-ttu-id="c65de-105">Indica a una finestra IME di impostare lo stile della finestra di composizione.</span><span class="sxs-lookup"><span data-stu-id="c65de-105">Instructs an IME window to set the style of the composition window.</span></span> <span data-ttu-id="c65de-106">Per inviare questo comando, l'applicazione usa il messaggio di [**\_ \_ controllo IME WM**](wm-ime-control.md) con le impostazioni dei parametri mostrate di seguito.</span><span class="sxs-lookup"><span data-stu-id="c65de-106">To send this command, the application uses the [**WM\_IME\_CONTROL**](wm-ime-control.md) message with the parameter settings shown below.</span></span>


```C++
LRESULT IMC_SETCOMPOSITIONWINDOW
```



## <a name="parameters"></a><span data-ttu-id="c65de-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="c65de-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c65de-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="c65de-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="c65de-109">Impostare su IMC \_ SETCOMPOSITIONWINDOW.</span><span class="sxs-lookup"><span data-stu-id="c65de-109">Set to IMC\_SETCOMPOSITIONWINDOW.</span></span>

</dd> <dt>

<span data-ttu-id="c65de-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="c65de-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="c65de-111">Puntatore a una struttura [**COMPOSITIONFORM**](/windows/win32/api/imm/ns-imm-compositionform) che contiene le informazioni sullo stile.</span><span class="sxs-lookup"><span data-stu-id="c65de-111">Pointer to a [**COMPOSITIONFORM**](/windows/win32/api/imm/ns-imm-compositionform) structure that contains the style information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c65de-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c65de-112">Return Value</span></span>

<span data-ttu-id="c65de-113">Restituisce 0 se ha esito positivo o un valore diverso da zero. in caso contrario,.</span><span class="sxs-lookup"><span data-stu-id="c65de-113">Returns 0 if successful, or a nonzero value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="c65de-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="c65de-114">Remarks</span></span>

<span data-ttu-id="c65de-115">Questo comando imposta lo stile nel contesto di input corrente e lo stile viene applicato successivamente a ogni finestra IME che riceve il contesto di input.</span><span class="sxs-lookup"><span data-stu-id="c65de-115">This command sets the style in the current input context, and the style is subsequently applied to each IME window that receives that input context.</span></span>

<span data-ttu-id="c65de-116">Per impostazione predefinita, la finestra IME presenta lo \_ stile punto di CFS.</span><span class="sxs-lookup"><span data-stu-id="c65de-116">By default, the IME window has the CFS\_POINT style.</span></span> <span data-ttu-id="c65de-117">Con questo stile, la finestra IME usa la posizione corrente del cursore e l'area client della finestra quando viene aperta una finestra di composizione.</span><span class="sxs-lookup"><span data-stu-id="c65de-117">With this style, the IME window uses the current caret position and window client area when it opens any composition window.</span></span>

## <a name="requirements"></a><span data-ttu-id="c65de-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c65de-118">Requirements</span></span>



| <span data-ttu-id="c65de-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="c65de-119">Requirement</span></span> | <span data-ttu-id="c65de-120">Valore</span><span class="sxs-lookup"><span data-stu-id="c65de-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c65de-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c65de-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c65de-122">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c65de-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="c65de-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c65de-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c65de-124">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c65de-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="c65de-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c65de-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="c65de-126"><dt>Imm. h (Includi Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c65de-126"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c65de-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c65de-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c65de-128">Gestione metodo di input</span><span class="sxs-lookup"><span data-stu-id="c65de-128">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="c65de-129">Comandi di input Method Manager</span><span class="sxs-lookup"><span data-stu-id="c65de-129">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="c65de-130">**COMPOSITIONFORM**</span><span class="sxs-lookup"><span data-stu-id="c65de-130">**COMPOSITIONFORM**</span></span>](/windows/win32/api/imm/ns-imm-compositionform)
</dt> <dt>

[<span data-ttu-id="c65de-131">**\_controllo IME \_ WM**</span><span class="sxs-lookup"><span data-stu-id="c65de-131">**WM\_IME\_CONTROL**</span></span>](wm-ime-control.md)
</dt> </dl>

 

 




