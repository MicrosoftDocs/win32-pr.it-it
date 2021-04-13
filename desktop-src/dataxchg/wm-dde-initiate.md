---
title: Messaggio di WM_DDE_INITIATE (DDE. h)
description: Un'applicazione client di Dynamic Data Exchange (DDE) Invia un \_ \_ messaggio di inizializzazione di WM DDE per avviare una conversazione con un'applicazione server che risponde ai nomi di applicazione e di argomento specificati.
ms.assetid: d486f584-75a3-4ffd-ba5d-f95f2692cd6c
keywords:
- Scambio di dati del messaggio WM_DDE_INITIATE
topic_type:
- apiref
api_name:
- WM_DDE_INITIATE
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36485db262c46d5364ee0ee26e7e6f39ccf0e677
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400554"
---
# <a name="wm_dde_initiate-message"></a><span data-ttu-id="f7d37-104">\_Messaggio di avvio DDE di WM \_</span><span class="sxs-lookup"><span data-stu-id="f7d37-104">WM\_DDE\_INITIATE message</span></span>

<span data-ttu-id="f7d37-105">Un'applicazione client di Dynamic Data Exchange (DDE) Invia un messaggio di **\_ \_ inizializzazione di WM DDE** per avviare una conversazione con un'applicazione server che risponde ai nomi di applicazione e di argomento specificati.</span><span class="sxs-lookup"><span data-stu-id="f7d37-105">A Dynamic Data Exchange (DDE) client application sends a **WM\_DDE\_INITIATE** message to initiate a conversation with a server application responding to the specified application and topic names.</span></span> <span data-ttu-id="f7d37-106">Al momento della ricezione di questo messaggio, è previsto che tutte le applicazioni server con nomi corrispondenti all'applicazione specificata e che supportano l'argomento specificato lo riconosca.</span><span class="sxs-lookup"><span data-stu-id="f7d37-106">Upon receiving this message, all server applications with names that match the specified application and that support the specified topic are expected to acknowledge it.</span></span> <span data-ttu-id="f7d37-107">Per ulteriori informazioni, vedere il messaggio [**\_ \_ ACK DDE di WM**](wm-dde-ack.md) .</span><span class="sxs-lookup"><span data-stu-id="f7d37-107">(For more information, see the [**WM\_DDE\_ACK**](wm-dde-ack.md) message.)</span></span>


```C++
#define WM_DDE_INITIATE        0x03E0
```



## <a name="parameters"></a><span data-ttu-id="f7d37-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="f7d37-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7d37-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f7d37-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f7d37-110">Handle per la finestra client che invia il messaggio.</span><span class="sxs-lookup"><span data-stu-id="f7d37-110">A handle to the client window sending the message.</span></span>

</dd> <dt>

<span data-ttu-id="f7d37-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f7d37-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f7d37-112">La parola di ordine inferiore contiene un Atom che identifica l'applicazione con cui viene richiesta una conversazione.</span><span class="sxs-lookup"><span data-stu-id="f7d37-112">The low-order word contains an atom that identifies the application with which a conversation is requested.</span></span> <span data-ttu-id="f7d37-113">Il nome dell'applicazione non può contenere barre (/) o barre rovesciate ( \) .</span><span class="sxs-lookup"><span data-stu-id="f7d37-113">The application name cannot contain slashes (/) or backslashes (\).</span></span> <span data-ttu-id="f7d37-114">Questi caratteri sono riservati per le implementazioni di rete.</span><span class="sxs-lookup"><span data-stu-id="f7d37-114">These characters are reserved for network implementations.</span></span> <span data-ttu-id="f7d37-115">Se questo parametro è **null**, viene richiesta una conversazione con tutte le applicazioni.</span><span class="sxs-lookup"><span data-stu-id="f7d37-115">If this parameter is **NULL**, a conversation with all applications is requested.</span></span>

<span data-ttu-id="f7d37-116">La parola più significativa contiene un atomo che identifica l'argomento per il quale viene richiesta una conversazione.</span><span class="sxs-lookup"><span data-stu-id="f7d37-116">The high-order word contains an atom that identifies the topic for which a conversation is requested.</span></span> <span data-ttu-id="f7d37-117">Se l'argomento è **null**, vengono richieste le conversazioni per tutti gli argomenti disponibili.</span><span class="sxs-lookup"><span data-stu-id="f7d37-117">If the topic is **NULL**, conversations for all available topics are requested.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f7d37-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="f7d37-118">Remarks</span></span>

<span data-ttu-id="f7d37-119">Se la parola di ordine inferiore di *lParam* è **null**, qualsiasi applicazione server può rispondere.</span><span class="sxs-lookup"><span data-stu-id="f7d37-119">If the low-order word of *lParam* is **NULL**, any server application can respond.</span></span> <span data-ttu-id="f7d37-120">Se la parola più ordinata di *lParam* è **null**, qualsiasi argomento è valido.</span><span class="sxs-lookup"><span data-stu-id="f7d37-120">If the high-order word of *lParam* is **NULL**, any topic is valid.</span></span> <span data-ttu-id="f7d37-121">Al momento della ricezione di una richiesta di **\_ \_ avvio di WM DDE** con la parola più ordinata del parametro *lParam* impostato su **null**, un server deve inviare un messaggio [**\_ \_ ACK DDE di WM**](wm-dde-ack.md) per ogni argomento supportato.</span><span class="sxs-lookup"><span data-stu-id="f7d37-121">Upon receiving a **WM\_DDE\_INITIATE** request with the high-order word of the *lParam* parameter set to **NULL**, a server must send a [**WM\_DDE\_ACK**](wm-dde-ack.md) message for each of the topics it supports.</span></span>

### <a name="sending"></a><span data-ttu-id="f7d37-122">Invio</span><span class="sxs-lookup"><span data-stu-id="f7d37-122">Sending</span></span>

<span data-ttu-id="f7d37-123">Il client trasmette il messaggio a tutte le finestre di primo livello impostando il primo parametro di [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) sulla **\_ trasmissione HWND**.</span><span class="sxs-lookup"><span data-stu-id="f7d37-123">The client broadcasts the message to all top-level windows by setting the first parameter of [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) to **HWND\_BROADCAST**.</span></span>

<span data-ttu-id="f7d37-124">Se l'applicazione client ha già ottenuto l'handle di finestra del server desiderato, può inviare l' **\_ \_ avvio di WM DDE** direttamente alla finestra del server passando l'handle della finestra del server come primo parametro di [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage).</span><span class="sxs-lookup"><span data-stu-id="f7d37-124">If the client application has already obtained the window handle of the desired server, it can send **WM\_DDE\_INITIATE** directly to the server window by passing the server's window handle as the first parameter of [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage).</span></span>

<span data-ttu-id="f7d37-125">L'applicazione client alloca gli atomi chiamando la funzione [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) .</span><span class="sxs-lookup"><span data-stu-id="f7d37-125">The client application allocates atoms by calling the [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) function.</span></span>

<span data-ttu-id="f7d37-126">Quando [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) restituisce, l'applicazione client deve eliminare gli atomi.</span><span class="sxs-lookup"><span data-stu-id="f7d37-126">When [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) returns, the client application must delete the atoms.</span></span>

### <a name="receiving"></a><span data-ttu-id="f7d37-127">Ricezione</span><span class="sxs-lookup"><span data-stu-id="f7d37-127">Receiving</span></span>

<span data-ttu-id="f7d37-128">Per completare l'avvio di una conversazione, l'applicazione server deve rispondere con uno o più messaggi [**di \_ \_ ACK DDE WM**](wm-dde-ack.md) , dove ogni messaggio è per un argomento separato.</span><span class="sxs-lookup"><span data-stu-id="f7d37-128">To complete the initiation of a conversation, the server application must respond with one or more [**WM\_DDE\_ACK**](wm-dde-ack.md) messages, where each message is for a separate topic.</span></span> <span data-ttu-id="f7d37-129">Quando si invia un messaggio **\_ \_ ACK di WM DDE** , il server deve creare nuovi atomi. non deve riutilizzare gli atomi inviati con l' **\_ \_ avvio di WM DDE**.</span><span class="sxs-lookup"><span data-stu-id="f7d37-129">When sending **WM\_DDE\_ACK** message, the server should create new atoms; it should not reuse the atoms sent with **WM\_DDE\_INITIATE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7d37-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f7d37-130">Requirements</span></span>



| <span data-ttu-id="f7d37-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="f7d37-131">Requirement</span></span> | <span data-ttu-id="f7d37-132">Valore</span><span class="sxs-lookup"><span data-stu-id="f7d37-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7d37-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f7d37-133">Minimum supported client</span></span><br/> | <span data-ttu-id="f7d37-134">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f7d37-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="f7d37-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f7d37-135">Minimum supported server</span></span><br/> | <span data-ttu-id="f7d37-136">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f7d37-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="f7d37-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f7d37-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="f7d37-138"><dt>DDE. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f7d37-138"><dt>Dde.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f7d37-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f7d37-139">See also</span></span>

<dl> <dt>

<span data-ttu-id="f7d37-140">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="f7d37-140">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f7d37-141">**GlobalAddAtom**</span><span class="sxs-lookup"><span data-stu-id="f7d37-141">**GlobalAddAtom**</span></span>](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma)
</dt> <dt>

[<span data-ttu-id="f7d37-142">**PostMessage**</span><span class="sxs-lookup"><span data-stu-id="f7d37-142">**PostMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[<span data-ttu-id="f7d37-143">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="f7d37-143">**SendMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[<span data-ttu-id="f7d37-144">**\_ACK DDE \_ WM**</span><span class="sxs-lookup"><span data-stu-id="f7d37-144">**WM\_DDE\_ACK**</span></span>](wm-dde-ack.md)
</dt> <dt>

<span data-ttu-id="f7d37-145">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="f7d37-145">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="f7d37-146">Informazioni su Dynamic Data Exchange</span><span class="sxs-lookup"><span data-stu-id="f7d37-146">About Dynamic Data Exchange</span></span>](about-dynamic-data-exchange.md)
</dt> </dl>

 

