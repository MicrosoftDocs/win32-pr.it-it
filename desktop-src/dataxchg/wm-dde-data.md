---
title: Messaggio di WM_DDE_DATA (DDE. h)
description: Un'applicazione server Dynamic Data Exchange (DDE) Invia un \_ messaggio di \_ dati DDE WM a un'applicazione client DDE per passare un elemento dati al client o per notificare al client la disponibilità di un elemento di dati.
ms.assetid: ed6a65d3-b2a3-45f2-9600-291ce2ec8c0a
keywords:
- Scambio di dati del messaggio WM_DDE_DATA
topic_type:
- apiref
api_name:
- WM_DDE_DATA
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f045ff07e01023e6535eb00dcb78400e4c9519a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301493"
---
# <a name="wm_dde_data-message"></a><span data-ttu-id="25ae8-104">\_ \_ Messaggio dati DDE WM</span><span class="sxs-lookup"><span data-stu-id="25ae8-104">WM\_DDE\_DATA message</span></span>

<span data-ttu-id="25ae8-105">Un'applicazione server Dynamic Data Exchange (DDE) Invia un messaggio di **\_ \_ dati DDE WM** a un'applicazione client DDE per passare un elemento dati al client o per notificare al client la disponibilità di un elemento di dati.</span><span class="sxs-lookup"><span data-stu-id="25ae8-105">A Dynamic Data Exchange (DDE) server application posts a **WM\_DDE\_DATA** message to a DDE client application to pass a data item to the client or to notify the client of the availability of a data item.</span></span>

<span data-ttu-id="25ae8-106">Per pubblicare questo messaggio, chiamare la funzione [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) con i parametri seguenti.</span><span class="sxs-lookup"><span data-stu-id="25ae8-106">To post this message, call the [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) function with the following parameters.</span></span>


```C++
#define WM_DDE_DATA        0x03E05
```



## <a name="parameters"></a><span data-ttu-id="25ae8-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="25ae8-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25ae8-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="25ae8-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="25ae8-109">Handle per la finestra del server che pubblica il messaggio.</span><span class="sxs-lookup"><span data-stu-id="25ae8-109">A handle to the server window posting the message.</span></span>

</dd> <dt>

<span data-ttu-id="25ae8-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="25ae8-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="25ae8-111">La parola di ordine inferiore è un handle per un oggetto memoria globale contenente una struttura [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata) con i dati e informazioni aggiuntive.</span><span class="sxs-lookup"><span data-stu-id="25ae8-111">The low-order word is a handle to a global memory object containing a [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata) structure with the data and additional information.</span></span> <span data-ttu-id="25ae8-112">L'handle deve essere impostato su **null** se il server invia una notifica al client che il valore dell'elemento di dati è stato modificato durante un collegamento dati caldo.</span><span class="sxs-lookup"><span data-stu-id="25ae8-112">The handle should be set to **NULL** if the server is notifying the client that the data-item value has changed during a warm data link.</span></span> <span data-ttu-id="25ae8-113">Un collegamento a caldo viene stabilito dal client che invia un messaggio di [**\_ \_ notifica DDE di WM**](wm-dde-advise.md) con il set di bit **FDeferUpd** .</span><span class="sxs-lookup"><span data-stu-id="25ae8-113">A warm link is established by the client sending a [**WM\_DDE\_ADVISE**](wm-dde-advise.md) message with the **fDeferUpd** bit set.</span></span>

<span data-ttu-id="25ae8-114">La parola più significativa contiene un atomo che identifica l'elemento di dati per il quale vengono inviati i dati o la notifica.</span><span class="sxs-lookup"><span data-stu-id="25ae8-114">The high-order word contains an atom that identifies the data item for which the data or notification is sent.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="25ae8-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="25ae8-115">Remarks</span></span>

### <a name="posting"></a><span data-ttu-id="25ae8-116">Distacco</span><span class="sxs-lookup"><span data-stu-id="25ae8-116">Posting</span></span>

<span data-ttu-id="25ae8-117">L'applicazione server alloca l'oggetto memoria globale mediante la funzione [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc) .</span><span class="sxs-lookup"><span data-stu-id="25ae8-117">The server application allocates the global memory object using the [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc) function.</span></span> <span data-ttu-id="25ae8-118">Alloca il Atom usando la funzione [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) .</span><span class="sxs-lookup"><span data-stu-id="25ae8-118">It allocates the atom using the [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) function.</span></span>

<span data-ttu-id="25ae8-119">Il server deve creare o riutilizzare il parametro *lParam* **\_ \_ dei dati DDE di WM** chiamando la funzione [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) o [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) .</span><span class="sxs-lookup"><span data-stu-id="25ae8-119">The server must create or reuse the **WM\_DDE\_DATA** *lParam* parameter by calling the [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) function or the [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) function.</span></span>

<span data-ttu-id="25ae8-120">Se l'applicazione ricevente (client) risponde con un messaggio [**\_ \_ ACK DDE**](wm-dde-ack.md) negativo, l'applicazione di invio (Server) deve eliminare l'oggetto memoria globale. in caso contrario, il client deve eliminare l'oggetto dopo aver estratto il contenuto chiamando la funzione [**UnpackDDElParam**](/windows/desktop/api/Dde/nf-dde-unpackddelparam) .</span><span class="sxs-lookup"><span data-stu-id="25ae8-120">If the receiving (client) application responds with a negative [**WM\_DDE\_ACK**](wm-dde-ack.md) message, the posting (server) application must delete the global memory object; otherwise, the client must delete the object after extracting its contents by calling the [**UnpackDDElParam**](/windows/desktop/api/Dde/nf-dde-unpackddelparam) function.</span></span>

<span data-ttu-id="25ae8-121">Se l'applicazione server imposta il membro **fRelease** della struttura [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata) su **false**, il server è responsabile dell'eliminazione dell'oggetto in caso di ricezione di un riconoscimento positivo o negativo.</span><span class="sxs-lookup"><span data-stu-id="25ae8-121">If the server application sets the **fRelease** member of the [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata) structure to **FALSE**, the server is responsible for deleting the object upon receiving either a positive or negative acknowledgment.</span></span>

<span data-ttu-id="25ae8-122">L'applicazione server non deve impostare i membri **fAckReq** e **FRelease** della struttura [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata) su **false**.</span><span class="sxs-lookup"><span data-stu-id="25ae8-122">The server application should not set both the **fAckReq** and **fRelease** members of the [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata) structure to **FALSE**.</span></span> <span data-ttu-id="25ae8-123">Se entrambi i membri sono impostati su **false**, è impossibile per il server determinare quando eliminare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="25ae8-123">If both members are set to **FALSE**, it is impossible for the server to determine when to delete the object.</span></span>

### <a name="receiving"></a><span data-ttu-id="25ae8-124">Ricezione</span><span class="sxs-lookup"><span data-stu-id="25ae8-124">Receiving</span></span>

<span data-ttu-id="25ae8-125">Se **fAckReq** è **true**, l'applicazione client deve pubblicare il [**messaggio \_ \_ ACK DDE di WM**](wm-dde-ack.md) per rispondere in modo positivo o negativo.</span><span class="sxs-lookup"><span data-stu-id="25ae8-125">If **fAckReq** is **TRUE**, the client application should post the [**WM\_DDE\_ACK**](wm-dde-ack.md) message to respond positively or negatively.</span></span> <span data-ttu-id="25ae8-126">Quando si invia un **\_ \_ ACK DDE di WM**, il client può riutilizzare il formato Atom oppure può eliminarlo e crearne uno nuovo.</span><span class="sxs-lookup"><span data-stu-id="25ae8-126">When posting **WM\_DDE\_ACK**, the client can either reuse the atom, or it can delete it and create a new one.</span></span>

<span data-ttu-id="25ae8-127">Il client deve creare o riutilizzare il parametro *lParam* del [**\_ \_ ACK DDE WM**](wm-dde-ack.md) chiamando la funzione [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) o [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) .</span><span class="sxs-lookup"><span data-stu-id="25ae8-127">The client must create or reuse the [**WM\_DDE\_ACK**](wm-dde-ack.md) *lParam* parameter by calling the [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) function or the [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) function.</span></span>

<span data-ttu-id="25ae8-128">Se **fAckReq** è **false**, l'applicazione client deve eliminare il formato Atom.</span><span class="sxs-lookup"><span data-stu-id="25ae8-128">If **fAckReq** is **FALSE**, the client application should delete the atom.</span></span>

<span data-ttu-id="25ae8-129">Se l'applicazione di invio ha specificato l'oggetto memoria globale come **null**, l'applicazione ricevente può richiedere al server di inviare i dati pubblicando un messaggio di [**\_ \_ richiesta DDE di WM**](wm-dde-request.md) .</span><span class="sxs-lookup"><span data-stu-id="25ae8-129">If the posting application specified global memory object as **NULL**, the receiving application can request the server to send the data by posting a [**WM\_DDE\_REQUEST**](wm-dde-request.md) message.</span></span>

<span data-ttu-id="25ae8-130">Dopo l'elaborazione di un messaggio di **\_ \_ dati DDE di WM** in cui l'oggetto memoria globale non è **null**, il client deve liberare l'oggetto, a meno che non si verifica una delle condizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="25ae8-130">After processing a **WM\_DDE\_DATA** message in which the global memory object is not **NULL**, the client should free the object, unless one of the following conditions is true:</span></span>

-   <span data-ttu-id="25ae8-131">Il membro **fRelease** è **false**.</span><span class="sxs-lookup"><span data-stu-id="25ae8-131">The **fRelease** member is **FALSE**.</span></span>
-   <span data-ttu-id="25ae8-132">Il membro **fRelease** è **true**, ma l'applicazione client risponde con un messaggio [**\_ \_ ACK DDE di WM**](wm-dde-ack.md) negativo.</span><span class="sxs-lookup"><span data-stu-id="25ae8-132">The **fRelease** member is **TRUE**, but the client application responds with a negative [**WM\_DDE\_ACK**](wm-dde-ack.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="25ae8-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="25ae8-133">Requirements</span></span>



| <span data-ttu-id="25ae8-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="25ae8-134">Requirement</span></span> | <span data-ttu-id="25ae8-135">Valore</span><span class="sxs-lookup"><span data-stu-id="25ae8-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="25ae8-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="25ae8-136">Minimum supported client</span></span><br/> | <span data-ttu-id="25ae8-137">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="25ae8-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="25ae8-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="25ae8-138">Minimum supported server</span></span><br/> | <span data-ttu-id="25ae8-139">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="25ae8-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="25ae8-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="25ae8-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="25ae8-141"><dt>DDE. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="25ae8-141"><dt>Dde.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25ae8-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="25ae8-142">See also</span></span>

<dl> <dt>

<span data-ttu-id="25ae8-143">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="25ae8-143">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="25ae8-144">**DDEDATA**</span><span class="sxs-lookup"><span data-stu-id="25ae8-144">**DDEDATA**</span></span>](/windows/desktop/api/Dde/ns-dde-ddedata)
</dt> <dt>

[<span data-ttu-id="25ae8-145">**FreeDDElParam**</span><span class="sxs-lookup"><span data-stu-id="25ae8-145">**FreeDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-freeddelparam)
</dt> <dt>

[<span data-ttu-id="25ae8-146">**GlobalAddAtom**</span><span class="sxs-lookup"><span data-stu-id="25ae8-146">**GlobalAddAtom**</span></span>](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma)
</dt> <dt>

[<span data-ttu-id="25ae8-147">**PackDDElParam**</span><span class="sxs-lookup"><span data-stu-id="25ae8-147">**PackDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-packddelparam)
</dt> <dt>

[<span data-ttu-id="25ae8-148">**PostMessage**</span><span class="sxs-lookup"><span data-stu-id="25ae8-148">**PostMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[<span data-ttu-id="25ae8-149">**ReuseDDElParam**</span><span class="sxs-lookup"><span data-stu-id="25ae8-149">**ReuseDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-reuseddelparam)
</dt> <dt>

[<span data-ttu-id="25ae8-150">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="25ae8-150">**SendMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[<span data-ttu-id="25ae8-151">**UnpackDDElParam**</span><span class="sxs-lookup"><span data-stu-id="25ae8-151">**UnpackDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-unpackddelparam)
</dt> <dt>

[<span data-ttu-id="25ae8-152">**\_ACK DDE \_ WM**</span><span class="sxs-lookup"><span data-stu-id="25ae8-152">**WM\_DDE\_ACK**</span></span>](wm-dde-ack.md)
</dt> <dt>

[<span data-ttu-id="25ae8-153">**\_avviso DDE di WM \_**</span><span class="sxs-lookup"><span data-stu-id="25ae8-153">**WM\_DDE\_ADVISE**</span></span>](wm-dde-advise.md)
</dt> <dt>

[<span data-ttu-id="25ae8-154">**\_poke DDE \_ WM**</span><span class="sxs-lookup"><span data-stu-id="25ae8-154">**WM\_DDE\_POKE**</span></span>](wm-dde-poke.md)
</dt> <dt>

[<span data-ttu-id="25ae8-155">**\_richiesta DDE \_ WM**</span><span class="sxs-lookup"><span data-stu-id="25ae8-155">**WM\_DDE\_REQUEST**</span></span>](wm-dde-request.md)
</dt> <dt>

<span data-ttu-id="25ae8-156">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="25ae8-156">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="25ae8-157">Informazioni su Dynamic Data Exchange</span><span class="sxs-lookup"><span data-stu-id="25ae8-157">About Dynamic Data Exchange</span></span>](about-dynamic-data-exchange.md)
</dt> </dl>

 

