---
title: Messaggio di WM_DDE_UNADVISE (DDE. h)
description: Un'applicazione client di Dynamic Data Exchange (DDE) Invia un \_ \_ messaggio di avviso DDE di WM per informare un'applicazione server DDE che l'elemento specificato o un particolare formato degli Appunti per l'elemento non deve più essere aggiornato.
ms.assetid: 9a5f9a86-e6fa-450e-b8bf-f20042c7e6d1
keywords:
- Scambio di dati del messaggio WM_DDE_UNADVISE
topic_type:
- apiref
api_name:
- WM_DDE_UNADVISE
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dba83badcb689789d2654d99780bcb8cc503511d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478305"
---
# <a name="wm_dde_unadvise-message"></a><span data-ttu-id="eb662-104">\_ \_ Messaggio Unadvise DDE WM</span><span class="sxs-lookup"><span data-stu-id="eb662-104">WM\_DDE\_UNADVISE message</span></span>

<span data-ttu-id="eb662-105">Un'applicazione client di Dynamic Data Exchange (DDE) Invia un messaggio di avviso **\_ \_ DDE di WM** per informare un'applicazione server DDE che l'elemento specificato o un particolare formato degli Appunti per l'elemento non deve più essere aggiornato.</span><span class="sxs-lookup"><span data-stu-id="eb662-105">A Dynamic Data Exchange (DDE) client application posts a **WM\_DDE\_UNADVISE** message to inform a DDE server application that the specified item or a particular clipboard format for the item should no longer be updated.</span></span> <span data-ttu-id="eb662-106">Questa operazione interrompe il collegamento dati caldo o attivo per l'elemento specificato.</span><span class="sxs-lookup"><span data-stu-id="eb662-106">This terminates the warm or hot data link for the specified item.</span></span>

<span data-ttu-id="eb662-107">Per pubblicare questo messaggio, chiamare la funzione [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) con i parametri seguenti.</span><span class="sxs-lookup"><span data-stu-id="eb662-107">To post this message, call the [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) function with the following parameters.</span></span>


```C++
#define WM_DDE_UNADVISE        0x03E3
```



## <a name="parameters"></a><span data-ttu-id="eb662-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="eb662-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb662-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="eb662-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="eb662-110">Handle per la finestra client che invia il messaggio.</span><span class="sxs-lookup"><span data-stu-id="eb662-110">A handle to the client window sending the message.</span></span>

</dd> <dt>

<span data-ttu-id="eb662-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="eb662-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="eb662-112">La parola di ordine inferiore specifica il formato degli Appunti dell'elemento per il quale la richiesta di aggiornamento viene ritratta.</span><span class="sxs-lookup"><span data-stu-id="eb662-112">The low-order word specifies the clipboard format of the item for which the update request is being retracted.</span></span> <span data-ttu-id="eb662-113">Se il **valore è null**, tutte le conversazioni di [**\_ \_ notifica del DDE di WM**](wm-dde-advise.md) attive per l'elemento devono essere terminate.</span><span class="sxs-lookup"><span data-stu-id="eb662-113">If this is **NULL**, all active [**WM\_DDE\_ADVISE**](wm-dde-advise.md) conversations for the item are to be terminated.</span></span>

<span data-ttu-id="eb662-114">La parola più ordinata contiene un Atom globale che identifica l'elemento per il quale viene ritratta la richiesta di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="eb662-114">The high-order word contains a global atom that identifies the item for which the update request is being retracted.</span></span> <span data-ttu-id="eb662-115">Se è **null**, tutti i collegamenti [**di \_ \_ avviso DDE di WM**](wm-dde-advise.md) attivi associati alla conversazione devono essere interrotti.</span><span class="sxs-lookup"><span data-stu-id="eb662-115">If this is **NULL**, all active [**WM\_DDE\_ADVISE**](wm-dde-advise.md) links associated with the conversation are to be terminated.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="eb662-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="eb662-116">Remarks</span></span>

<span data-ttu-id="eb662-117">L'applicazione client alloca la parola più ordinata di *lParam* chiamando la funzione [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) .</span><span class="sxs-lookup"><span data-stu-id="eb662-117">The client application allocates the high-order word of *lParam* by calling the [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) function.</span></span>

<span data-ttu-id="eb662-118">L'applicazione server inserisce il [**messaggio \_ \_ ACK DDE di WM**](wm-dde-ack.md) per rispondere in modo positivo o negativo.</span><span class="sxs-lookup"><span data-stu-id="eb662-118">The server application posts the [**WM\_DDE\_ACK**](wm-dde-ack.md) message to respond positively or negatively.</span></span> <span data-ttu-id="eb662-119">Quando si invia un **\_ \_ ACK DDE di WM**, il server può riutilizzare il formato Atom o eliminare l'Atom e crearne uno nuovo.</span><span class="sxs-lookup"><span data-stu-id="eb662-119">When posting **WM\_DDE\_ACK**, the server can either reuse the atom, or it can delete the atom and create a new one.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb662-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="eb662-120">Requirements</span></span>



| <span data-ttu-id="eb662-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="eb662-121">Requirement</span></span> | <span data-ttu-id="eb662-122">Valore</span><span class="sxs-lookup"><span data-stu-id="eb662-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb662-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="eb662-123">Minimum supported client</span></span><br/> | <span data-ttu-id="eb662-124">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="eb662-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="eb662-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="eb662-125">Minimum supported server</span></span><br/> | <span data-ttu-id="eb662-126">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="eb662-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="eb662-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="eb662-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="eb662-128"><dt>DDE. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="eb662-128"><dt>Dde.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb662-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="eb662-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="eb662-130">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="eb662-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="eb662-131">**GlobalAddAtom**</span><span class="sxs-lookup"><span data-stu-id="eb662-131">**GlobalAddAtom**</span></span>](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma)
</dt> <dt>

[<span data-ttu-id="eb662-132">**PackDDElParam**</span><span class="sxs-lookup"><span data-stu-id="eb662-132">**PackDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-packddelparam)
</dt> <dt>

[<span data-ttu-id="eb662-133">**PostMessage**</span><span class="sxs-lookup"><span data-stu-id="eb662-133">**PostMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[<span data-ttu-id="eb662-134">**ReuseDDElParam**</span><span class="sxs-lookup"><span data-stu-id="eb662-134">**ReuseDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-reuseddelparam)
</dt> <dt>

[<span data-ttu-id="eb662-135">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="eb662-135">**SendMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[<span data-ttu-id="eb662-136">**UnpackDDElParam**</span><span class="sxs-lookup"><span data-stu-id="eb662-136">**UnpackDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-unpackddelparam)
</dt> <dt>

[<span data-ttu-id="eb662-137">**\_ACK DDE \_ WM**</span><span class="sxs-lookup"><span data-stu-id="eb662-137">**WM\_DDE\_ACK**</span></span>](wm-dde-ack.md)
</dt> <dt>

[<span data-ttu-id="eb662-138">**\_avviso DDE di WM \_**</span><span class="sxs-lookup"><span data-stu-id="eb662-138">**WM\_DDE\_ADVISE**</span></span>](wm-dde-advise.md)
</dt> <dt>

<span data-ttu-id="eb662-139">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="eb662-139">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="eb662-140">Informazioni su Dynamic Data Exchange</span><span class="sxs-lookup"><span data-stu-id="eb662-140">About Dynamic Data Exchange</span></span>](about-dynamic-data-exchange.md)
</dt> </dl>

 

