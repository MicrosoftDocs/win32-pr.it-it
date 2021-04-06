---
title: Messaggio di WM_DDE_POKE (DDE. h)
description: Un'applicazione client di Dynamic Data Exchange (DDE) Invia un \_ \_ messaggio di poke DDE di WM a un'applicazione server DDE.
ms.assetid: 848142b7-a7ef-4206-9bb3-b511388cfaaa
keywords:
- Scambio di dati del messaggio WM_DDE_POKE
topic_type:
- apiref
api_name:
- WM_DDE_POKE
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 001697cbd5328b9c8d9eb72ebddff5f86ef6381c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743695"
---
# <a name="wm_dde_poke-message"></a><span data-ttu-id="098e9-104">\_ \_ Messaggio poke DDE WM</span><span class="sxs-lookup"><span data-stu-id="098e9-104">WM\_DDE\_POKE message</span></span>

<span data-ttu-id="098e9-105">Un'applicazione client di Dynamic Data Exchange (DDE) Invia un messaggio di **\_ \_ poke DDE di WM** a un'applicazione server DDE.</span><span class="sxs-lookup"><span data-stu-id="098e9-105">A Dynamic Data Exchange (DDE) client application posts a **WM\_DDE\_POKE** message to a DDE server application.</span></span> <span data-ttu-id="098e9-106">Un client utilizza questo messaggio per richiedere al server di accettare un elemento di dati non richiesto.</span><span class="sxs-lookup"><span data-stu-id="098e9-106">A client uses this message to request the server to accept an unsolicited data item.</span></span> <span data-ttu-id="098e9-107">Si prevede che il server risponda con un messaggio di [**\_ \_ ACK DDE WM**](wm-dde-ack.md) che indica se l'elemento di dati è stato accettato.</span><span class="sxs-lookup"><span data-stu-id="098e9-107">The server is expected to reply with a [**WM\_DDE\_ACK**](wm-dde-ack.md) message indicating whether it accepted the data item.</span></span>

<span data-ttu-id="098e9-108">Per pubblicare questo messaggio, chiamare la funzione [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) con i parametri seguenti.</span><span class="sxs-lookup"><span data-stu-id="098e9-108">To post this message, call the [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) function with the following parameters.</span></span>


```C++
#define WM_DDE_POKE        0x03E7
```



## <a name="parameters"></a><span data-ttu-id="098e9-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="098e9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="098e9-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="098e9-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="098e9-111">Handle per la finestra client che invia il messaggio.</span><span class="sxs-lookup"><span data-stu-id="098e9-111">A handle to the client window posting the message.</span></span>

</dd> <dt>

<span data-ttu-id="098e9-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="098e9-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="098e9-113">La parola di ordine inferiore è un handle per un oggetto memoria globale contenente una struttura [**DDEPoke**](/windows/desktop/api/Dde/ns-dde-ddepoke) con i dati e informazioni aggiuntive.</span><span class="sxs-lookup"><span data-stu-id="098e9-113">The low-order word is a handle to a global memory object containing a [**DDEPOKE**](/windows/desktop/api/Dde/ns-dde-ddepoke) structure with the data and additional information.</span></span>

<span data-ttu-id="098e9-114">La parola più ordinata contiene un Atom globale che identifica l'elemento di dati per il quale vengono inviati i dati o la notifica.</span><span class="sxs-lookup"><span data-stu-id="098e9-114">The high-order word contains a global atom that identifies the data item for which the data or notification is being sent.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="098e9-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="098e9-115">Remarks</span></span>

### <a name="posting"></a><span data-ttu-id="098e9-116">Distacco</span><span class="sxs-lookup"><span data-stu-id="098e9-116">Posting</span></span>

<span data-ttu-id="098e9-117">L'applicazione client deve allocare memoria per l'oggetto memoria globale usando la funzione [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc) .</span><span class="sxs-lookup"><span data-stu-id="098e9-117">The client application must allocate memory for the global memory object using the [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc) function.</span></span> <span data-ttu-id="098e9-118">L'applicazione client deve eliminare l'oggetto se si verifica una delle condizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="098e9-118">The client application must delete the object if either of the following conditions is true:</span></span>

-   <span data-ttu-id="098e9-119">L'applicazione server risponde con un messaggio di [**\_ \_ ACK DDE WM**](wm-dde-ack.md) negativo.</span><span class="sxs-lookup"><span data-stu-id="098e9-119">The server application responds with a negative [**WM\_DDE\_ACK**](wm-dde-ack.md) message.</span></span>
-   <span data-ttu-id="098e9-120">Il membro **fRelease** è **false**, ma l'applicazione server risponde con un [**\_ \_ ACK DDE WM**](wm-dde-ack.md)positivo o negativo.</span><span class="sxs-lookup"><span data-stu-id="098e9-120">The **fRelease** member is **FALSE**, but the server application responds with either a positive or negative [**WM\_DDE\_ACK**](wm-dde-ack.md).</span></span>

<span data-ttu-id="098e9-121">L'applicazione client deve creare il Atom usando la funzione [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) .</span><span class="sxs-lookup"><span data-stu-id="098e9-121">The client application must create the atom using the [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) function.</span></span>

<span data-ttu-id="098e9-122">L'applicazione client deve creare o riutilizzare *il parametro di* **WM \_ DDE \_ poke** , chiamando la funzione [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) o [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) .</span><span class="sxs-lookup"><span data-stu-id="098e9-122">The client application must create or reuse the **WM\_DDE\_POKE** *lParam* parameter by calling the [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) function or the [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) function.</span></span>

### <a name="receiving"></a><span data-ttu-id="098e9-123">Ricezione</span><span class="sxs-lookup"><span data-stu-id="098e9-123">Receiving</span></span>

<span data-ttu-id="098e9-124">L'applicazione server deve pubblicare il [**messaggio \_ \_ ACK DDE di WM**](wm-dde-ack.md) per rispondere in modo positivo o negativo.</span><span class="sxs-lookup"><span data-stu-id="098e9-124">The server application should post the [**WM\_DDE\_ACK**](wm-dde-ack.md) message to respond positively or negatively.</span></span> <span data-ttu-id="098e9-125">Quando si invia un **\_ \_ ACK DDE WM**, il server può riutilizzare il formato Atom o eliminarlo e crearne uno nuovo.</span><span class="sxs-lookup"><span data-stu-id="098e9-125">When posting **WM\_DDE\_ACK**, the server can either reuse the atom, or it can delete it and create a new one.</span></span>

<span data-ttu-id="098e9-126">Il server deve creare o riutilizzare il parametro *lParam* del [**\_ \_ ACK DDE WM**](wm-dde-ack.md) chiamando la funzione [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) o [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) .</span><span class="sxs-lookup"><span data-stu-id="098e9-126">The server must create or reuse the [**WM\_DDE\_ACK**](wm-dde-ack.md) *lParam* parameter by calling the [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) function or the [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) function.</span></span>

<span data-ttu-id="098e9-127">Per liberare l'oggetto memoria globale, il server deve chiamare la funzione [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) .</span><span class="sxs-lookup"><span data-stu-id="098e9-127">To free the global memory object, the server should call the [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) function.</span></span> <span data-ttu-id="098e9-128">Inoltre, se il formato dei dati è [**CF \_ DSPMETAFILEPICT**](clipboard-formats.md) o **CF \_ METAFILEPICT**, il server deve anche chiamare [**DeleteMetaFile**](/windows/desktop/api/wingdi/nf-wingdi-deletemetafile) con l'handle del metafile incorporato.</span><span class="sxs-lookup"><span data-stu-id="098e9-128">Also, if the data format is either [**CF\_DSPMETAFILEPICT**](clipboard-formats.md) or **CF\_METAFILEPICT**, the server must also call [**DeleteMetaFile**](/windows/desktop/api/wingdi/nf-wingdi-deletemetafile) with the embedded metafile handle.</span></span> <span data-ttu-id="098e9-129">Questi due formati hanno un ulteriore livello di riferimento indiretto; Ciò significa che un'applicazione deve bloccare l'oggetto per ottenere un puntatore a un handle, quindi bloccare tale handle per ottenere un puntatore a una struttura [**METAFILEPICT**](/windows/win32/api/wingdi/ns-wingdi-metafilepict) e infine chiamare **DeleteMetaFile** con l'handle del membro **HMF** della struttura **METAFILEPICT** .</span><span class="sxs-lookup"><span data-stu-id="098e9-129">These two formats have an extra level of indirection; that is, an application must lock the object to get a pointer to a handle, then lock that handle to get a pointer to a [**METAFILEPICT**](/windows/win32/api/wingdi/ns-wingdi-metafilepict) structure, and finally call **DeleteMetaFile** with the handle from the **hMF** member of the **METAFILEPICT** structure.</span></span>

<span data-ttu-id="098e9-130">Per liberare l'oggetto, il server deve chiamare la funzione [**FreeDDElParam**](/windows/desktop/api/Dde/nf-dde-freeddelparam) .</span><span class="sxs-lookup"><span data-stu-id="098e9-130">To free the object, the server should call the [**FreeDDElParam**](/windows/desktop/api/Dde/nf-dde-freeddelparam) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="098e9-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="098e9-131">Requirements</span></span>



| <span data-ttu-id="098e9-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="098e9-132">Requirement</span></span> | <span data-ttu-id="098e9-133">Valore</span><span class="sxs-lookup"><span data-stu-id="098e9-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="098e9-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="098e9-134">Minimum supported client</span></span><br/> | <span data-ttu-id="098e9-135">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="098e9-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="098e9-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="098e9-136">Minimum supported server</span></span><br/> | <span data-ttu-id="098e9-137">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="098e9-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="098e9-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="098e9-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="098e9-139"><dt>DDE. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="098e9-139"><dt>Dde.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="098e9-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="098e9-140">See also</span></span>

<dl> <dt>

<span data-ttu-id="098e9-141">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="098e9-141">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="098e9-142">**DDEPOKE**</span><span class="sxs-lookup"><span data-stu-id="098e9-142">**DDEPOKE**</span></span>](/windows/desktop/api/Dde/ns-dde-ddepoke)
</dt> <dt>

[<span data-ttu-id="098e9-143">**FreeDDElParam**</span><span class="sxs-lookup"><span data-stu-id="098e9-143">**FreeDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-freeddelparam)
</dt> <dt>

[<span data-ttu-id="098e9-144">**GlobalAddAtom**</span><span class="sxs-lookup"><span data-stu-id="098e9-144">**GlobalAddAtom**</span></span>](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma)
</dt> <dt>

[<span data-ttu-id="098e9-145">**METAFILEPICT**</span><span class="sxs-lookup"><span data-stu-id="098e9-145">**METAFILEPICT**</span></span>](/windows/win32/api/wingdi/ns-wingdi-metafilepict)
</dt> <dt>

[<span data-ttu-id="098e9-146">**PackDDElParam**</span><span class="sxs-lookup"><span data-stu-id="098e9-146">**PackDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-packddelparam)
</dt> <dt>

[<span data-ttu-id="098e9-147">**PostMessage**</span><span class="sxs-lookup"><span data-stu-id="098e9-147">**PostMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[<span data-ttu-id="098e9-148">**ReuseDDElParam**</span><span class="sxs-lookup"><span data-stu-id="098e9-148">**ReuseDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-reuseddelparam)
</dt> <dt>

[<span data-ttu-id="098e9-149">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="098e9-149">**SendMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[<span data-ttu-id="098e9-150">**UnpackDDElParam**</span><span class="sxs-lookup"><span data-stu-id="098e9-150">**UnpackDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-unpackddelparam)
</dt> <dt>

[<span data-ttu-id="098e9-151">**\_ACK DDE \_ WM**</span><span class="sxs-lookup"><span data-stu-id="098e9-151">**WM\_DDE\_ACK**</span></span>](wm-dde-ack.md)
</dt> <dt>

<span data-ttu-id="098e9-152">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="098e9-152">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="098e9-153">Informazioni su Dynamic Data Exchange</span><span class="sxs-lookup"><span data-stu-id="098e9-153">About Dynamic Data Exchange</span></span>](about-dynamic-data-exchange.md)
</dt> </dl>

 

