---
description: Notifica a un'applicazione quando l'IME deve modificare la struttura RECONVERTSTRING. L'applicazione riceve questo comando tramite il \_ \_ messaggio di richiesta IME WM con le impostazioni dei parametri, come illustrato di seguito.
ms.assetid: 035a7072-d292-4883-bc3e-d1e9ed64d9ec
title: Codice di notifica IMR_CONFIRMRECONVERTSTRING (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c500a155be14f447bb07ad506e12d5bece66e225
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756494"
---
# <a name="imr_confirmreconvertstring-notification-code"></a><span data-ttu-id="7164a-104">\_Codice di notifica CONFIRMRECONVERTSTRING di IMR</span><span class="sxs-lookup"><span data-stu-id="7164a-104">IMR\_CONFIRMRECONVERTSTRING notification code</span></span>

<span data-ttu-id="7164a-105">Notifica a un'applicazione quando l'IME deve modificare la struttura [**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring) .</span><span class="sxs-lookup"><span data-stu-id="7164a-105">Notifies an application when the IME needs to change the [**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring) structure.</span></span> <span data-ttu-id="7164a-106">L'applicazione riceve questo comando tramite il messaggio di [**\_ \_ richiesta IME WM**](wm-ime-request.md) con le impostazioni dei parametri, come illustrato di seguito.</span><span class="sxs-lookup"><span data-stu-id="7164a-106">The application receives this command through the [**WM\_IME\_REQUEST**](wm-ime-request.md) message with parameter settings as shown below.</span></span>


```C++
LRESULT IMR_CONFIRMRECONVERTSTRING
```



## <a name="parameters"></a><span data-ttu-id="7164a-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="7164a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7164a-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="7164a-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="7164a-109">Impostare su IMR \_ CONFIRMRECONVERTSTRING.</span><span class="sxs-lookup"><span data-stu-id="7164a-109">Set to IMR\_CONFIRMRECONVERTSTRING.</span></span>

</dd> <dt>

<span data-ttu-id="7164a-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="7164a-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="7164a-111">Puntatore a una struttura [**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring) dall'IME.</span><span class="sxs-lookup"><span data-stu-id="7164a-111">Pointer to a [**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring) structure from the IME.</span></span> <span data-ttu-id="7164a-112">Per altre informazioni, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="7164a-112">For more information, see the Remarks section.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7164a-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7164a-113">Return Value</span></span>

<span data-ttu-id="7164a-114">Restituisce un valore diverso da zero se l'applicazione accetta la struttura [**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring) modificata.</span><span class="sxs-lookup"><span data-stu-id="7164a-114">Returns a nonzero value if the application accepts the changed [**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring) structure.</span></span> <span data-ttu-id="7164a-115">In caso contrario, il comando restituisce 0 e l'IME utilizza la struttura **RECONVERTSTRING** originale.</span><span class="sxs-lookup"><span data-stu-id="7164a-115">Otherwise, the command returns 0 and the IME uses the original **RECONVERTSTRING** structure.</span></span>

## <a name="remarks"></a><span data-ttu-id="7164a-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="7164a-116">Remarks</span></span>

<span data-ttu-id="7164a-117">L'applicazione compila la struttura [**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring) alla ricezione del comando [IMR \_ RECONVERTSTRING](imr-reconvertstring.md) .</span><span class="sxs-lookup"><span data-stu-id="7164a-117">The application fills in the [**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring) structure upon receiving the [IMR\_RECONVERTSTRING](imr-reconvertstring.md) command.</span></span>

<span data-ttu-id="7164a-118">Dopo che l'applicazione ha gestito [IMR \_ RECONVERTSTRING](imr-reconvertstring.md), è possibile che l'IME non modifichi la struttura [**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring) .</span><span class="sxs-lookup"><span data-stu-id="7164a-118">After the application has handled [IMR\_RECONVERTSTRING](imr-reconvertstring.md), the IME might or might not adjust the [**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring) structure.</span></span> <span data-ttu-id="7164a-119">L'IME invia una \_ richiesta IME WM \_ con **IMR \_ CONFIRMRECONVERTSTRING** per confermare le modifiche apportate alla struttura **RECONVERTSTRING** .</span><span class="sxs-lookup"><span data-stu-id="7164a-119">The IME sends WM\_IME\_REQUEST with **IMR\_CONFIRMRECONVERTSTRING** to confirm the changes to the **RECONVERTSTRING** structure.</span></span> <span data-ttu-id="7164a-120">Se l'applicazione restituisce **true** per **IMR \_ CONFIRMRECONVERTSTRING**, l'IME genera una nuova stringa di composizione basata sulla struttura **RECONVERTSTRING** per il comando **IMR \_ CONFIRMRECONVERTSTRING** .</span><span class="sxs-lookup"><span data-stu-id="7164a-120">If the application returns **TRUE** for **IMR\_CONFIRMRECONVERTSTRING**, the IME generates a new composition string based on the **RECONVERTSTRING** structure for the **IMR\_CONFIRMRECONVERTSTRING** command.</span></span> <span data-ttu-id="7164a-121">Se l'applicazione restituisce **false** per **IMR \_ CONFIRMRECONVERTSTRING**, l'IME genera una nuova stringa di composizione basata sulla struttura **RECONVERTSTRING** originale specificata dall'applicazione nel \_ comando IMR RECONVERTSTRING.</span><span class="sxs-lookup"><span data-stu-id="7164a-121">If the application returns **FALSE** for **IMR\_CONFIRMRECONVERTSTRING**, the IME generates a new composition string based on the original **RECONVERTSTRING** structure specified by the application in the IMR\_RECONVERTSTRING command.</span></span>

## <a name="requirements"></a><span data-ttu-id="7164a-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7164a-122">Requirements</span></span>



| <span data-ttu-id="7164a-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="7164a-123">Requirement</span></span> | <span data-ttu-id="7164a-124">Valore</span><span class="sxs-lookup"><span data-stu-id="7164a-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7164a-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7164a-125">Minimum supported client</span></span><br/> | <span data-ttu-id="7164a-126">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="7164a-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="7164a-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7164a-127">Minimum supported server</span></span><br/> | <span data-ttu-id="7164a-128">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="7164a-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="7164a-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7164a-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="7164a-130"><dt>Imm. h (Includi Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7164a-130"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7164a-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7164a-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7164a-132">Gestione metodo di input</span><span class="sxs-lookup"><span data-stu-id="7164a-132">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="7164a-133">Comandi di input Method Manager</span><span class="sxs-lookup"><span data-stu-id="7164a-133">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="7164a-134">\_RECONVERTSTRING IMR</span><span class="sxs-lookup"><span data-stu-id="7164a-134">IMR\_RECONVERTSTRING</span></span>](imr-reconvertstring.md)
</dt> <dt>

[<span data-ttu-id="7164a-135">**RECONVERTSTRING**</span><span class="sxs-lookup"><span data-stu-id="7164a-135">**RECONVERTSTRING**</span></span>](/windows/win32/api/imm/ns-imm-reconvertstring)
</dt> <dt>

[<span data-ttu-id="7164a-136">**\_richiesta IME \_ WM**</span><span class="sxs-lookup"><span data-stu-id="7164a-136">**WM\_IME\_REQUEST**</span></span>](wm-ime-request.md)
</dt> </dl>

 

 




