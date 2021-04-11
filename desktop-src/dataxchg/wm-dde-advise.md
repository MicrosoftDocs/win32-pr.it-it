---
title: Messaggio di WM_DDE_ADVISE (DDE. h)
description: Un'applicazione client di Dynamic Data Exchange (DDE) Invia il \_ \_ messaggio di notifica DDE di WM a un'applicazione server DDE per richiedere al server di fornire un aggiornamento per un elemento di dati ogni volta che l'elemento viene modificato.
ms.assetid: b00db740-36a7-4487-abbf-d74b12f5212a
keywords:
- Scambio di dati del messaggio WM_DDE_ADVISE
topic_type:
- apiref
api_name:
- WM_DDE_ADVISE
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 832c6991169b71955c0ab21b59d2b55b0b54fc9a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119623"
---
# <a name="wm_dde_advise-message"></a><span data-ttu-id="f6b58-104">\_Messaggio di avviso DDE di WM \_</span><span class="sxs-lookup"><span data-stu-id="f6b58-104">WM\_DDE\_ADVISE message</span></span>

<span data-ttu-id="f6b58-105">Un'applicazione client di Dynamic Data Exchange (DDE) Invia il messaggio di **\_ \_ notifica DDE di WM** a un'applicazione server DDE per richiedere al server di fornire un aggiornamento per un elemento di dati ogni volta che l'elemento viene modificato.</span><span class="sxs-lookup"><span data-stu-id="f6b58-105">A Dynamic Data Exchange (DDE) client application posts the **WM\_DDE\_ADVISE** message to a DDE server application to request the server to supply an update for a data item whenever the item changes.</span></span>

<span data-ttu-id="f6b58-106">Per pubblicare questo messaggio, chiamare la funzione [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) con i parametri seguenti.</span><span class="sxs-lookup"><span data-stu-id="f6b58-106">To post this message, call the [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) function with the following parameters.</span></span>


```C++
#define WM_DDE_ADVISE      0x03E2
```



## <a name="parameters"></a><span data-ttu-id="f6b58-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="f6b58-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6b58-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f6b58-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f6b58-109">Handle per la finestra client che invia il messaggio.</span><span class="sxs-lookup"><span data-stu-id="f6b58-109">A handle to the client window posting the message.</span></span>

</dd> <dt>

<span data-ttu-id="f6b58-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f6b58-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f6b58-111">La parola di ordine inferiore è un handle per un oggetto memoria globale contenente una struttura [**DDEAdvise**](/windows/desktop/api/Dde/ns-dde-ddeadvise) che specifica la modalità di invio dei dati.</span><span class="sxs-lookup"><span data-stu-id="f6b58-111">The low-order word is a handle to a global memory object containing a [**DDEADVISE**](/windows/desktop/api/Dde/ns-dde-ddeadvise) structure that specifies how the data is to be sent.</span></span>

<span data-ttu-id="f6b58-112">La parola più ordinata contiene un Atom che identifica l'elemento di dati richiesto.</span><span class="sxs-lookup"><span data-stu-id="f6b58-112">The high-order word contains an atom that identifies the requested data item.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f6b58-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="f6b58-113">Remarks</span></span>

<span data-ttu-id="f6b58-114">Se un'applicazione client supporta più di un formato degli Appunti per un singolo argomento ed elemento, può inserire più messaggi di **\_ \_ notifica DDE di WM** per l'argomento e l'elemento, specificando un formato degli Appunti diverso a ogni messaggio.</span><span class="sxs-lookup"><span data-stu-id="f6b58-114">If a client application supports more than one clipboard format for a single topic and item, it can post multiple **WM\_DDE\_ADVISE** messages for the topic and item, specifying a different clipboard format with each message.</span></span> <span data-ttu-id="f6b58-115">Si noti che un server può supportare più formati solo per i collegamenti dati ad accesso frequente, non per i collegamenti dati caldi.</span><span class="sxs-lookup"><span data-stu-id="f6b58-115">Note that a server can support multiple formats only for hot data links, not warm data links.</span></span>

### <a name="posting"></a><span data-ttu-id="f6b58-116">Distacco</span><span class="sxs-lookup"><span data-stu-id="f6b58-116">Posting</span></span>

<span data-ttu-id="f6b58-117">L'applicazione client invia il messaggio di **\_ \_ notifica DDE di WM** chiamando la funzione [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) , non la funzione [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) .</span><span class="sxs-lookup"><span data-stu-id="f6b58-117">The client application posts the **WM\_DDE\_ADVISE** message by calling the [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) function, not the [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) function.</span></span>

<span data-ttu-id="f6b58-118">L'applicazione client alloca l'oggetto memoria globale usando la funzione [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc) .</span><span class="sxs-lookup"><span data-stu-id="f6b58-118">The client application allocates the global memory object using the [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc) function.</span></span> <span data-ttu-id="f6b58-119">Alloca il Atom usando la funzione [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) .</span><span class="sxs-lookup"><span data-stu-id="f6b58-119">It allocates the atom using the [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) function.</span></span>

<span data-ttu-id="f6b58-120">L'applicazione client deve creare o riutilizzare il parametro *lParam* del **\_ \_ Consiglio DDE di WM** chiamando la funzione [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) o [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) .</span><span class="sxs-lookup"><span data-stu-id="f6b58-120">The client application must create or reuse the **WM\_DDE\_ADVISE** *lParam* parameter by calling the [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) function or the [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) function.</span></span>

<span data-ttu-id="f6b58-121">Se l'applicazione ricevente (Server) risponde con un messaggio [**di \_ \_ ACK DDE di WM**](wm-dde-ack.md) negativo, l'applicazione di pubblicazione deve eliminare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="f6b58-121">If the receiving (server) application responds with a negative [**WM\_DDE\_ACK**](wm-dde-ack.md) message, the posting application must delete the object.</span></span>

<span data-ttu-id="f6b58-122">Il flag **fRelease** non viene usato nei messaggi di **\_ \_ notifica DDE di WM** , ma il comportamento di liberazione dei dati è simile a quello dei [**\_ \_ dati DDE**](wm-dde-data.md) di WM e dei messaggi [**\_ \_ poke DDE di WM**](wm-dde-poke.md) in cui **fRelease** è **true**.</span><span class="sxs-lookup"><span data-stu-id="f6b58-122">The **fRelease** flag is not used in **WM\_DDE\_ADVISE** messages, but their data-freeing behavior is similar to that of [**WM\_DDE\_DATA**](wm-dde-data.md) and [**WM\_DDE\_POKE**](wm-dde-poke.md) messages where **fRelease** is **TRUE**.</span></span>

### <a name="receiving"></a><span data-ttu-id="f6b58-123">Ricezione</span><span class="sxs-lookup"><span data-stu-id="f6b58-123">Receiving</span></span>

<span data-ttu-id="f6b58-124">L'applicazione server inserisce il [**messaggio \_ \_ ACK DDE di WM**](wm-dde-ack.md) per rispondere in modo positivo o negativo.</span><span class="sxs-lookup"><span data-stu-id="f6b58-124">The server application posts the [**WM\_DDE\_ACK**](wm-dde-ack.md) message to respond positively or negatively.</span></span> <span data-ttu-id="f6b58-125">Quando si invia un **\_ \_ ACK DDE di WM**, l'applicazione può riutilizzare l'Atom o eliminarlo e crearne uno nuovo.</span><span class="sxs-lookup"><span data-stu-id="f6b58-125">When posting **WM\_DDE\_ACK**, the application can reuse the atom or delete it and create a new one.</span></span> <span data-ttu-id="f6b58-126">Se il **messaggio \_ \_ ACK DDE WM** è positivo, l'applicazione deve eliminare l'oggetto memoria globale; in caso contrario, l'applicazione non deve eliminare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="f6b58-126">If the **WM\_DDE\_ACK** message is positive, the application should delete the global memory object; otherwise, the application should not delete the object.</span></span>

<span data-ttu-id="f6b58-127">Il server deve creare o riutilizzare il parametro *lParam* del [**\_ \_ ACK DDE WM**](wm-dde-ack.md) chiamando la funzione [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) o [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) .</span><span class="sxs-lookup"><span data-stu-id="f6b58-127">The server must create or reuse the [**WM\_DDE\_ACK**](wm-dde-ack.md) *lParam* parameter by calling the [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) function or the [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="f6b58-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f6b58-128">Requirements</span></span>



| <span data-ttu-id="f6b58-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="f6b58-129">Requirement</span></span> | <span data-ttu-id="f6b58-130">Valore</span><span class="sxs-lookup"><span data-stu-id="f6b58-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6b58-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f6b58-131">Minimum supported client</span></span><br/> | <span data-ttu-id="f6b58-132">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f6b58-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="f6b58-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f6b58-133">Minimum supported server</span></span><br/> | <span data-ttu-id="f6b58-134">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f6b58-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="f6b58-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f6b58-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="f6b58-136"><dt>DDE. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f6b58-136"><dt>Dde.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f6b58-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f6b58-137">See also</span></span>

<dl> <dt>

<span data-ttu-id="f6b58-138">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="f6b58-138">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f6b58-139">**DDEADVISE**</span><span class="sxs-lookup"><span data-stu-id="f6b58-139">**DDEADVISE**</span></span>](/windows/desktop/api/Dde/ns-dde-ddeadvise)
</dt> <dt>

[<span data-ttu-id="f6b58-140">**FreeDDElParam**</span><span class="sxs-lookup"><span data-stu-id="f6b58-140">**FreeDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-freeddelparam)
</dt> <dt>

[<span data-ttu-id="f6b58-141">**GlobalAddAtom**</span><span class="sxs-lookup"><span data-stu-id="f6b58-141">**GlobalAddAtom**</span></span>](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma)
</dt> <dt>

[<span data-ttu-id="f6b58-142">**PackDDElParam**</span><span class="sxs-lookup"><span data-stu-id="f6b58-142">**PackDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-packddelparam)
</dt> <dt>

[<span data-ttu-id="f6b58-143">**PostMessage**</span><span class="sxs-lookup"><span data-stu-id="f6b58-143">**PostMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[<span data-ttu-id="f6b58-144">**ReuseDDElParam**</span><span class="sxs-lookup"><span data-stu-id="f6b58-144">**ReuseDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-reuseddelparam)
</dt> <dt>

[<span data-ttu-id="f6b58-145">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="f6b58-145">**SendMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[<span data-ttu-id="f6b58-146">**UnpackDDElParam**</span><span class="sxs-lookup"><span data-stu-id="f6b58-146">**UnpackDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-unpackddelparam)
</dt> <dt>

[<span data-ttu-id="f6b58-147">**\_ACK DDE \_ WM**</span><span class="sxs-lookup"><span data-stu-id="f6b58-147">**WM\_DDE\_ACK**</span></span>](wm-dde-ack.md)
</dt> <dt>

[<span data-ttu-id="f6b58-148">**\_dati DDE di WM \_**</span><span class="sxs-lookup"><span data-stu-id="f6b58-148">**WM\_DDE\_DATA**</span></span>](wm-dde-data.md)
</dt> <dt>

[<span data-ttu-id="f6b58-149">**\_poke DDE \_ WM**</span><span class="sxs-lookup"><span data-stu-id="f6b58-149">**WM\_DDE\_POKE**</span></span>](wm-dde-poke.md)
</dt> <dt>

[<span data-ttu-id="f6b58-150">**\_richiesta DDE \_ WM**</span><span class="sxs-lookup"><span data-stu-id="f6b58-150">**WM\_DDE\_REQUEST**</span></span>](wm-dde-request.md)
</dt> <dt>

<span data-ttu-id="f6b58-151">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="f6b58-151">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="f6b58-152">Informazioni su Dynamic Data Exchange</span><span class="sxs-lookup"><span data-stu-id="f6b58-152">About Dynamic Data Exchange</span></span>](about-dynamic-data-exchange.md)
</dt> </dl>

 

