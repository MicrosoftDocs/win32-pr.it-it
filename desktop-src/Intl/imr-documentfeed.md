---
description: Notifica a un'applicazione quando l'IME selezionato necessita della stringa convertita dall'applicazione. L'applicazione riceve questo comando tramite il \_ \_ messaggio di richiesta IME WM con i parametri impostati come illustrato di seguito.
ms.assetid: 1a007bed-15e5-4400-9d2f-32e37e1765d2
title: Codice di notifica IMR_DOCUMENTFEED (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc4fe46f95b7ad17ba7bb7850ec3fb9ca980519f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227416"
---
# <a name="imr_documentfeed-notification-code"></a><span data-ttu-id="ec86d-104">\_Codice di notifica DOCUMENTFEED di IMR</span><span class="sxs-lookup"><span data-stu-id="ec86d-104">IMR\_DOCUMENTFEED notification code</span></span>

<span data-ttu-id="ec86d-105">Notifica a un'applicazione quando l'IME selezionato necessita della stringa convertita dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ec86d-105">Notifies an application when the selected IME needs the converted string from the application.</span></span> <span data-ttu-id="ec86d-106">L'applicazione riceve questo comando tramite il messaggio di [**\_ \_ richiesta IME WM**](wm-ime-request.md) con i parametri impostati come illustrato di seguito.</span><span class="sxs-lookup"><span data-stu-id="ec86d-106">The application receives this command through the [**WM\_IME\_REQUEST**](wm-ime-request.md) message with parameters set as shown below.</span></span>


```C++
LRESULT IMR_DOCUMENTFEED
```



## <a name="parameters"></a><span data-ttu-id="ec86d-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="ec86d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec86d-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="ec86d-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="ec86d-109">Impostare su IMR \_ DOCUMENTFEED.</span><span class="sxs-lookup"><span data-stu-id="ec86d-109">Set to IMR\_DOCUMENTFEED.</span></span>

</dd> <dt>

<span data-ttu-id="ec86d-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="ec86d-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="ec86d-111">Puntatore a un buffer per contenere la struttura [**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring) .</span><span class="sxs-lookup"><span data-stu-id="ec86d-111">Pointer to a buffer to contain the [**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec86d-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ec86d-112">Return Value</span></span>

<span data-ttu-id="ec86d-113">Restituisce la struttura della stringa di riconversione corrente.</span><span class="sxs-lookup"><span data-stu-id="ec86d-113">Returns the current reconversion string structure.</span></span> <span data-ttu-id="ec86d-114">Se *lParam* è impostato su **null**, l'applicazione restituisce la dimensione richiesta per il buffer in cui deve essere contenuta la struttura.</span><span class="sxs-lookup"><span data-stu-id="ec86d-114">If *lParam* is set to **NULL**, the application returns the required size for the buffer to hold the structure.</span></span> <span data-ttu-id="ec86d-115">Se l'operazione non riesce, il comando restituisce 0.</span><span class="sxs-lookup"><span data-stu-id="ec86d-115">The command returns 0 if it does not succeed.</span></span>

## <a name="remarks"></a><span data-ttu-id="ec86d-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="ec86d-116">Remarks</span></span>

<span data-ttu-id="ec86d-117">L'IME memorizza nella cache le stringhe convertite per una maggiore accuratezza della conversione.</span><span class="sxs-lookup"><span data-stu-id="ec86d-117">The IME caches converted strings for higher conversion accuracy.</span></span> <span data-ttu-id="ec86d-118">Una limitazione della memorizzazione nella cache dell'IME è la perdita della stringa convertita nei casi seguenti:</span><span class="sxs-lookup"><span data-stu-id="ec86d-118">One caching limitation of the IME is that it loses the converted string under the following circumstances:</span></span>

-   <span data-ttu-id="ec86d-119">La posizione del punto di inserimento per l'applicazione viene spostata da una chiave, ad esempio una chiave del cursore.</span><span class="sxs-lookup"><span data-stu-id="ec86d-119">The caret position for the application is moved by a key, for example, a cursor key.</span></span>
-   <span data-ttu-id="ec86d-120">La posizione del punto di inserimento per l'applicazione viene spostata dal mouse.</span><span class="sxs-lookup"><span data-stu-id="ec86d-120">The caret position for the application is moved by the mouse.</span></span>
-   <span data-ttu-id="ec86d-121">Viene aperto un nuovo documento.</span><span class="sxs-lookup"><span data-stu-id="ec86d-121">A new document is opened.</span></span>

<span data-ttu-id="ec86d-122">Con il comando **IMR \_ DOCUMENTFEED** , l'IME può aggiornare le stringhe memorizzate nella cache in qualsiasi momento.</span><span class="sxs-lookup"><span data-stu-id="ec86d-122">With the **IMR\_DOCUMENTFEED** command, the IME can refresh its cached strings any time.</span></span> <span data-ttu-id="ec86d-123">L'uso di questo comando migliora l'accuratezza della conversione.</span><span class="sxs-lookup"><span data-stu-id="ec86d-123">Use of this command improves conversion accuracy.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec86d-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ec86d-124">Requirements</span></span>



| <span data-ttu-id="ec86d-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="ec86d-125">Requirement</span></span> | <span data-ttu-id="ec86d-126">Valore</span><span class="sxs-lookup"><span data-stu-id="ec86d-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec86d-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ec86d-127">Minimum supported client</span></span><br/> | <span data-ttu-id="ec86d-128">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ec86d-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="ec86d-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ec86d-129">Minimum supported server</span></span><br/> | <span data-ttu-id="ec86d-130">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ec86d-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="ec86d-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ec86d-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="ec86d-132"><dt>Imm. h (Includi Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ec86d-132"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec86d-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ec86d-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec86d-134">Gestione metodo di input</span><span class="sxs-lookup"><span data-stu-id="ec86d-134">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="ec86d-135">Comandi di input Method Manager</span><span class="sxs-lookup"><span data-stu-id="ec86d-135">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="ec86d-136">**RECONVERTSTRING**</span><span class="sxs-lookup"><span data-stu-id="ec86d-136">**RECONVERTSTRING**</span></span>](/windows/win32/api/imm/ns-imm-reconvertstring)
</dt> <dt>

[<span data-ttu-id="ec86d-137">**\_richiesta IME \_ WM**</span><span class="sxs-lookup"><span data-stu-id="ec86d-137">**WM\_IME\_REQUEST**</span></span>](wm-ime-request.md)
</dt> </dl>

 

 




