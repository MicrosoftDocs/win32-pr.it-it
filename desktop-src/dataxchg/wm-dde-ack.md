---
title: Messaggio di WM_DDE_ACK (DDE. h)
description: Il \_ \_ messaggio ACK DDE di WM notifica a un'applicazione Dynamic Data Exchange (DDE) la ricezione e l'elaborazione dei seguenti messaggi WM \_ DDE \_ poke, WM \_ DDE \_ Execute, WM \_ DDE \_ data, WM \_ DDE \_ Advise, WM \_ DDE \_ Unadvise, WM \_ DDE \_ Initiation o WM DDE \_ \_ Request (in alcuni casi). Per pubblicare questo messaggio, chiamare la funzione PostMessage con i parametri seguenti.
ms.assetid: aca47dbf-e1f2-4725-8364-0aa7fcd98bd9
keywords:
- Scambio di dati del messaggio WM_DDE_ACK
topic_type:
- apiref
api_name:
- WM_DDE_ACK
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a407fc6cad7077586539f119dd65be59a507cacd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048284"
---
# <a name="wm_dde_ack-message"></a><span data-ttu-id="7ca72-105">\_ \_ Messaggio ACK DDE WM</span><span class="sxs-lookup"><span data-stu-id="7ca72-105">WM\_DDE\_ACK message</span></span>

<span data-ttu-id="7ca72-106">Il **messaggio \_ \_ ACK DDE WM** notifica a un'applicazione Dynamic Data Exchange (DDE) la ricezione e l'elaborazione dei messaggi seguenti: [**WM \_ DDE \_ poke**](wm-dde-poke.md), [**WM \_ DDE \_ Execute**](wm-dde-execute.md), [**WM \_ DDE \_ Data**](wm-dde-data.md), [**WM \_ DDE \_ Advise**](wm-dde-advise.md), [**WM \_ DDE \_ Unadvise**](wm-dde-unadvise.md), [**WM \_ DDE \_ Initiation**](wm-dde-initiate.md)o WM DDE [**\_ \_ Request**](wm-dde-request.md) (in alcuni casi).</span><span class="sxs-lookup"><span data-stu-id="7ca72-106">The **WM\_DDE\_ACK** message notifies a Dynamic Data Exchange (DDE) application of the receipt and processing of the following messages: [**WM\_DDE\_POKE**](wm-dde-poke.md), [**WM\_DDE\_EXECUTE**](wm-dde-execute.md), [**WM\_DDE\_DATA**](wm-dde-data.md), [**WM\_DDE\_ADVISE**](wm-dde-advise.md), [**WM\_DDE\_UNADVISE**](wm-dde-unadvise.md), [**WM\_DDE\_INITIATE**](wm-dde-initiate.md), or [**WM\_DDE\_REQUEST**](wm-dde-request.md) (in some cases).</span></span>

<span data-ttu-id="7ca72-107">Per pubblicare questo messaggio, chiamare la funzione [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) con i parametri seguenti.</span><span class="sxs-lookup"><span data-stu-id="7ca72-107">To post this message, call the [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) function with the following parameters.</span></span>


```C++
#define WM_DDE_ACK     0x03E4
```



## <a name="parameters"></a><span data-ttu-id="7ca72-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="7ca72-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ca72-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7ca72-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7ca72-110">Quando si risponde [**all' \_ \_ avvio di WM DDE**](wm-dde-initiate.md), questo parametro è un handle per la finestra del server che invia il messaggio.</span><span class="sxs-lookup"><span data-stu-id="7ca72-110">When responding to [**WM\_DDE\_INITIATE**](wm-dde-initiate.md), this parameter is a handle to the server window sending the message.</span></span>

<span data-ttu-id="7ca72-111">Quando si risponde [**all' \_ \_ esecuzione di WM DDE**](wm-dde-execute.md), questo parametro è un handle per la finestra del server che pubblica il messaggio.</span><span class="sxs-lookup"><span data-stu-id="7ca72-111">When responding to [**WM\_DDE\_EXECUTE**](wm-dde-execute.md), this parameter is a handle to the server window posting the message.</span></span>

<span data-ttu-id="7ca72-112">Quando si risponde a tutti gli altri messaggi, questo parametro è un handle per la finestra client o server che pubblica il messaggio.</span><span class="sxs-lookup"><span data-stu-id="7ca72-112">When replying to all other messages, this parameter is a handle to the client or server window posting the message.</span></span>

</dd> <dt>

<span data-ttu-id="7ca72-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7ca72-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7ca72-114">Quando si risponde [**all' \_ \_ avvio di WM DDE**](wm-dde-initiate.md), la parola più bassa contiene un atomo che identifica l'applicazione di risposta.</span><span class="sxs-lookup"><span data-stu-id="7ca72-114">When responding to [**WM\_DDE\_INITIATE**](wm-dde-initiate.md), the low-order word contains an atom that identifies the replying application.</span></span> <span data-ttu-id="7ca72-115">La parola più ordinata contiene un atomo che identifica l'argomento per cui viene stabilita una conversazione.</span><span class="sxs-lookup"><span data-stu-id="7ca72-115">The high-order word contains an atom that identifies the topic for which a conversation is being established.</span></span>

<span data-ttu-id="7ca72-116">Quando si risponde [**all' \_ \_ esecuzione di WM DDE**](wm-dde-execute.md), la parola più bassa indica una struttura [**DDEACK**](/windows/desktop/api/Dde/ns-dde-ddeack) contenente una serie di flag che indicano lo stato della risposta.</span><span class="sxs-lookup"><span data-stu-id="7ca72-116">When responding to [**WM\_DDE\_EXECUTE**](wm-dde-execute.md), the low-order word specifies a [**DDEACK**](/windows/desktop/api/Dde/ns-dde-ddeack) structure containing a series of flags that indicate the status of the response.</span></span> <span data-ttu-id="7ca72-117">La parola più ordinata è un handle per un oggetto memoria globale che contiene la stringa di comando ricevuta nel messaggio di **\_ \_ esecuzione DDE di WM** .</span><span class="sxs-lookup"><span data-stu-id="7ca72-117">The high-order word is a handle to a global memory object that contains the command string that was received in the **WM\_DDE\_EXECUTE** message.</span></span>

<span data-ttu-id="7ca72-118">Quando si risponde a tutti gli altri messaggi, la parola di ordine inferiore specifica una struttura [**DDEACK**](/windows/desktop/api/Dde/ns-dde-ddeack) contenente una serie di flag che indicano lo stato della risposta.</span><span class="sxs-lookup"><span data-stu-id="7ca72-118">When replying to all other messages, the low-order word specifies a [**DDEACK**](/windows/desktop/api/Dde/ns-dde-ddeack) structure containing a series of flags that indicate the status of the response.</span></span> <span data-ttu-id="7ca72-119">La parola più ordinata contiene un Atom globale che identifica il nome dell'elemento di dati per cui viene inviata la risposta.</span><span class="sxs-lookup"><span data-stu-id="7ca72-119">The high-order word contains a global atom that identifies the name of the data item for which the response is sent.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7ca72-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="7ca72-120">Remarks</span></span>

### <a name="posting"></a><span data-ttu-id="7ca72-121">Distacco</span><span class="sxs-lookup"><span data-stu-id="7ca72-121">Posting</span></span>

<span data-ttu-id="7ca72-122">Tranne che in risposta al messaggio di [**\_ \_ inizializzazione di WM DDE**](wm-dde-initiate.md) , l'applicazione invia il messaggio **\_ \_ ACK DDE di WM** chiamando la funzione [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) , non chiamando la funzione [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) .</span><span class="sxs-lookup"><span data-stu-id="7ca72-122">Except in response to the [**WM\_DDE\_INITIATE**](wm-dde-initiate.md) message, the application posts the **WM\_DDE\_ACK** message by calling the [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) function, not by calling the [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) function.</span></span> <span data-ttu-id="7ca72-123">Quando si risponde **all' \_ \_ avvio di WM DDE**, l'applicazione invia il messaggio **\_ \_ ACK DDE di WM** chiamando **SendMessage**.</span><span class="sxs-lookup"><span data-stu-id="7ca72-123">When responding to **WM\_DDE\_INITIATE**, the application sends the **WM\_DDE\_ACK** message by calling **SendMessage**.</span></span> <span data-ttu-id="7ca72-124">In questo caso, né il nome dell'applicazione Atom né il nome dell'argomento Atom devono essere **null** (anche se il messaggio di **\_ \_ inizializzazione del DDE di WM** ha specificato atomi **null** ).</span><span class="sxs-lookup"><span data-stu-id="7ca72-124">In this case, neither the application-name atom nor the topic-name atom should be **NULL** (even if the **WM\_DDE\_INITIATE** message specified **NULL** atoms).</span></span>

<span data-ttu-id="7ca72-125">Quando si riconosce un messaggio con un Atom associato, l'applicazione che invia **l' \_ \_ ACK DDE WM** può riutilizzare il Atom che ha accompagnato il messaggio originale oppure può eliminarlo e crearne uno nuovo.</span><span class="sxs-lookup"><span data-stu-id="7ca72-125">When acknowledging any message with an accompanying atom, the application posting **WM\_DDE\_ACK** can either reuse the atom that accompanied the original message, or it can delete it and create a new one.</span></span>

<span data-ttu-id="7ca72-126">Quando si riconosce [**l' \_ \_ esecuzione di WM DDE**](wm-dde-execute.md), l'applicazione che invia **ACK di WM \_ DDE \_** deve riutilizzare l'oggetto memoria globale identificato nel messaggio **\_ \_ Execute DDE** originale di WM.</span><span class="sxs-lookup"><span data-stu-id="7ca72-126">When acknowledging [**WM\_DDE\_EXECUTE**](wm-dde-execute.md), the application that posts **WM\_DDE\_ACK** should reuse the global memory object identified in the original **WM\_DDE\_EXECUTE** message.</span></span>

<span data-ttu-id="7ca72-127">Tutti i messaggi di **\_ \_ ACK con DDE WM** inviati devono creare o riutilizzare il parametro *lParam* chiamando la funzione [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) o [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) .</span><span class="sxs-lookup"><span data-stu-id="7ca72-127">All posted **WM\_DDE\_ACK** messages must create or reuse the *lParam* parameter by calling the [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) function or the [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) function.</span></span>

<span data-ttu-id="7ca72-128">Se un'applicazione ha avviato la chiusura di una conversazione pubblicando la terminazione di [**WM \_ DDE \_**](wm-dde-terminate.md) ed è in attesa di conferma, l'applicazione in attesa non deve riconoscere (in modo positivo o negativo) i messaggi successivi inviati dall'altra applicazione.</span><span class="sxs-lookup"><span data-stu-id="7ca72-128">If an application has initiated the termination of a conversation by posting [**WM\_DDE\_TERMINATE**](wm-dde-terminate.md) and is awaiting confirmation, the waiting application should not acknowledge (positively or negatively) any subsequent messages sent by the other application.</span></span> <span data-ttu-id="7ca72-129">L'applicazione in attesa deve eliminare tutti gli atomi o gli oggetti di memoria condivisa ricevuti in questi messaggi.</span><span class="sxs-lookup"><span data-stu-id="7ca72-129">The waiting application should delete any atoms or shared memory objects received in these intervening messages.</span></span> <span data-ttu-id="7ca72-130">Gli oggetti memoria non devono essere liberati se il flag **fRelease** è impostato su **false** nei messaggi di [**\_ \_ dati DDE**](wm-dde-data.md) del DDE [**WM \_ \_**](wm-dde-poke.md) e WM.</span><span class="sxs-lookup"><span data-stu-id="7ca72-130">Memory objects should not be freed if the **fRelease** flag is set to **FALSE** in [**WM\_DDE\_POKE**](wm-dde-poke.md) and [**WM\_DDE\_DATA**](wm-dde-data.md) messages.</span></span>

### <a name="receiving"></a><span data-ttu-id="7ca72-131">Ricezione</span><span class="sxs-lookup"><span data-stu-id="7ca72-131">Receiving</span></span>

<span data-ttu-id="7ca72-132">L'applicazione che riceve un **messaggio \_ \_ ACK DDE WM** deve eliminare tutti gli atomi che accompagnano il messaggio.</span><span class="sxs-lookup"><span data-stu-id="7ca72-132">The application that receives a **WM\_DDE\_ACK** message should delete all atoms accompanying the message.</span></span> <span data-ttu-id="7ca72-133">Se l'applicazione riceve un **\_ \_ ACK DDE di WM** in risposta a un messaggio con un oggetto di memoria globale associato e l'oggetto è stato inviato con i flag **fRelease** impostati su **false**, l'applicazione è responsabile dell'eliminazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="7ca72-133">If the application receives a **WM\_DDE\_ACK** in response to a message with an accompanying global memory object, and the object was sent with the **fRelease** flags set to **FALSE**, the application is responsible for deleting the object.</span></span>

<span data-ttu-id="7ca72-134">Se l'applicazione riceve un messaggio **\_ \_ ACK DDE di WM** negativo inviato in risposta a un messaggio di [**\_ \_ avviso DDE di WM**](wm-dde-advise.md) , l'applicazione deve eliminare l'oggetto memoria globale inviato con il messaggio di **\_ \_ notifica DDE** di WM originale.</span><span class="sxs-lookup"><span data-stu-id="7ca72-134">If the application receives a negative **WM\_DDE\_ACK** message posted in reply to a [**WM\_DDE\_ADVISE**](wm-dde-advise.md) message, the application should delete the global memory object posted with the original **WM\_DDE\_ADVISE** message.</span></span> <span data-ttu-id="7ca72-135">Se l'applicazione riceve un messaggio **\_ \_ ACK DDE di WM** negativo pubblicato in risposta a [**\_ \_ dati DDE WM**](wm-dde-data.md), [**WM \_ DDE \_ poke**](wm-dde-poke.md)o [**WM \_ DDE \_ Execute**](wm-dde-execute.md) Message, l'applicazione deve eliminare l'oggetto memoria globale inviato con i **\_ \_ dati DDE di WM** originali, **WM \_ DDE \_ poke** o WM DDE **\_ \_ Execute** Message.</span><span class="sxs-lookup"><span data-stu-id="7ca72-135">If the application receives a negative **WM\_DDE\_ACK** message posted in reply to a [**WM\_DDE\_DATA**](wm-dde-data.md), [**WM\_DDE\_POKE**](wm-dde-poke.md), or [**WM\_DDE\_EXECUTE**](wm-dde-execute.md) message, the application should delete the global memory object posted with the original **WM\_DDE\_DATA**, **WM\_DDE\_POKE**, or **WM\_DDE\_EXECUTE** message.</span></span>

<span data-ttu-id="7ca72-136">L'applicazione che riceve un messaggio **di \_ \_ ACK DDE WM** inviato deve liberare il parametro *lParam* usando la funzione [**FreeDDElParam**](/windows/desktop/api/Dde/nf-dde-freeddelparam) .</span><span class="sxs-lookup"><span data-stu-id="7ca72-136">The application that receives a posted **WM\_DDE\_ACK** message must free the *lParam* parameter by using the [**FreeDDElParam**](/windows/desktop/api/Dde/nf-dde-freeddelparam) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ca72-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7ca72-137">Requirements</span></span>



| <span data-ttu-id="7ca72-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="7ca72-138">Requirement</span></span> | <span data-ttu-id="7ca72-139">Valore</span><span class="sxs-lookup"><span data-stu-id="7ca72-139">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ca72-140">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7ca72-140">Minimum supported client</span></span><br/> | <span data-ttu-id="7ca72-141">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="7ca72-141">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="7ca72-142">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7ca72-142">Minimum supported server</span></span><br/> | <span data-ttu-id="7ca72-143">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="7ca72-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="7ca72-144">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7ca72-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="7ca72-145"><dt>DDE. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7ca72-145"><dt>Dde.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7ca72-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7ca72-146">See also</span></span>

<dl> <dt>

<span data-ttu-id="7ca72-147">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="7ca72-147">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="7ca72-148">**DDEACK**</span><span class="sxs-lookup"><span data-stu-id="7ca72-148">**DDEACK**</span></span>](/windows/desktop/api/Dde/ns-dde-ddeack)
</dt> <dt>

[<span data-ttu-id="7ca72-149">**FreeDDElParam**</span><span class="sxs-lookup"><span data-stu-id="7ca72-149">**FreeDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-freeddelparam)
</dt> <dt>

[<span data-ttu-id="7ca72-150">**PackDDElParam**</span><span class="sxs-lookup"><span data-stu-id="7ca72-150">**PackDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-packddelparam)
</dt> <dt>

[<span data-ttu-id="7ca72-151">**PostMessage**</span><span class="sxs-lookup"><span data-stu-id="7ca72-151">**PostMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[<span data-ttu-id="7ca72-152">**ReuseDDElParam**</span><span class="sxs-lookup"><span data-stu-id="7ca72-152">**ReuseDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-reuseddelparam)
</dt> <dt>

[<span data-ttu-id="7ca72-153">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="7ca72-153">**SendMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[<span data-ttu-id="7ca72-154">**UnpackDDElParam**</span><span class="sxs-lookup"><span data-stu-id="7ca72-154">**UnpackDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-unpackddelparam)
</dt> <dt>

[<span data-ttu-id="7ca72-155">**\_avviso DDE di WM \_**</span><span class="sxs-lookup"><span data-stu-id="7ca72-155">**WM\_DDE\_ADVISE**</span></span>](wm-dde-advise.md)
</dt> <dt>

[<span data-ttu-id="7ca72-156">**\_dati DDE di WM \_**</span><span class="sxs-lookup"><span data-stu-id="7ca72-156">**WM\_DDE\_DATA**</span></span>](wm-dde-data.md)
</dt> <dt>

[<span data-ttu-id="7ca72-157">**esecuzione di WM \_ DDE \_**</span><span class="sxs-lookup"><span data-stu-id="7ca72-157">**WM\_DDE\_EXECUTE**</span></span>](wm-dde-execute.md)
</dt> <dt>

[<span data-ttu-id="7ca72-158">**\_avvio DDE \_ WM**</span><span class="sxs-lookup"><span data-stu-id="7ca72-158">**WM\_DDE\_INITIATE**</span></span>](wm-dde-initiate.md)
</dt> <dt>

[<span data-ttu-id="7ca72-159">**\_poke DDE \_ WM**</span><span class="sxs-lookup"><span data-stu-id="7ca72-159">**WM\_DDE\_POKE**</span></span>](wm-dde-poke.md)
</dt> <dt>

[<span data-ttu-id="7ca72-160">**\_richiesta DDE \_ WM**</span><span class="sxs-lookup"><span data-stu-id="7ca72-160">**WM\_DDE\_REQUEST**</span></span>](wm-dde-request.md)
</dt> <dt>

[<span data-ttu-id="7ca72-161">**\_ \_ terminazione DDE WM**</span><span class="sxs-lookup"><span data-stu-id="7ca72-161">**WM\_DDE\_TERMINATE**</span></span>](wm-dde-terminate.md)
</dt> <dt>

[<span data-ttu-id="7ca72-162">**\_Unadvise DDE WM \_**</span><span class="sxs-lookup"><span data-stu-id="7ca72-162">**WM\_DDE\_UNADVISE**</span></span>](wm-dde-unadvise.md)
</dt> <dt>

<span data-ttu-id="7ca72-163">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="7ca72-163">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="7ca72-164">Informazioni su Dynamic Data Exchange</span><span class="sxs-lookup"><span data-stu-id="7ca72-164">About Dynamic Data Exchange</span></span>](about-dynamic-data-exchange.md)
</dt> </dl>

 

