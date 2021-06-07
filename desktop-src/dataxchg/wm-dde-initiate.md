---
title: WM_DDE_INITIATE messaggio (Dde.h)
description: Un'applicazione client Dynamic Data Exchange (DDE) invia un messaggio WM DDE INITIATE per avviare una conversazione con un'applicazione server che risponde ai nomi dell'applicazione e \_ \_ dell'argomento specificati.
ms.assetid: d486f584-75a3-4ffd-ba5d-f95f2692cd6c
keywords:
- WM_DDE_INITIATE scambio di dati del messaggio
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
ms.openlocfilehash: bf65e222c7711d429db44e391d4f03c35997e219
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111386729"
---
# <a name="wm_dde_initiate-message"></a><span data-ttu-id="543fb-104">Messaggio WM \_ DDE \_ INITIATE</span><span class="sxs-lookup"><span data-stu-id="543fb-104">WM\_DDE\_INITIATE message</span></span>

<span data-ttu-id="543fb-105">Un'applicazione client Dynamic Data Exchange (DDE) invia un messaggio **WM \_ DDE \_ INITIATE** per avviare una conversazione con un'applicazione server che risponde ai nomi dell'applicazione e degli argomenti specificati.</span><span class="sxs-lookup"><span data-stu-id="543fb-105">A Dynamic Data Exchange (DDE) client application sends a **WM\_DDE\_INITIATE** message to initiate a conversation with a server application responding to the specified application and topic names.</span></span> <span data-ttu-id="543fb-106">Quando si riceve questo messaggio, tutte le applicazioni server con nomi che corrispondono all'applicazione specificata e che supportano l'argomento specificato devono confermarlo.</span><span class="sxs-lookup"><span data-stu-id="543fb-106">Upon receiving this message, all server applications with names that match the specified application and that support the specified topic are expected to acknowledge it.</span></span> <span data-ttu-id="543fb-107">Per altre informazioni, vedere il [**messaggio WM \_ DDE \_ ACK.**](wm-dde-ack.md)</span><span class="sxs-lookup"><span data-stu-id="543fb-107">(For more information, see the [**WM\_DDE\_ACK**](wm-dde-ack.md) message.)</span></span>


```C++
#define WM_DDE_INITIATE        0x03E0
```



## <a name="parameters"></a><span data-ttu-id="543fb-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="543fb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="543fb-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="543fb-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="543fb-110">Handle alla finestra client che invia il messaggio.</span><span class="sxs-lookup"><span data-stu-id="543fb-110">A handle to the client window sending the message.</span></span>

</dd> <dt>

<span data-ttu-id="543fb-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="543fb-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="543fb-112">La parola di ordine basso contiene un atom che identifica l'applicazione con cui viene richiesta una conversazione.</span><span class="sxs-lookup"><span data-stu-id="543fb-112">The low-order word contains an atom that identifies the application with which a conversation is requested.</span></span> <span data-ttu-id="543fb-113">Il nome dell'applicazione non può contenere barre (/) o barre rovesciate ( \\ ).</span><span class="sxs-lookup"><span data-stu-id="543fb-113">The application name cannot contain slashes (/) or backslashes (\\).</span></span> <span data-ttu-id="543fb-114">Questi caratteri sono riservati per le implementazioni di rete.</span><span class="sxs-lookup"><span data-stu-id="543fb-114">These characters are reserved for network implementations.</span></span> <span data-ttu-id="543fb-115">Se questo parametro è **NULL,** viene richiesta una conversazione con tutte le applicazioni.</span><span class="sxs-lookup"><span data-stu-id="543fb-115">If this parameter is **NULL**, a conversation with all applications is requested.</span></span>

<span data-ttu-id="543fb-116">La parola di ordine elevato contiene un atomo che identifica l'argomento per cui è richiesta una conversazione.</span><span class="sxs-lookup"><span data-stu-id="543fb-116">The high-order word contains an atom that identifies the topic for which a conversation is requested.</span></span> <span data-ttu-id="543fb-117">Se l'argomento è **NULL,** vengono richieste conversazioni per tutti gli argomenti disponibili.</span><span class="sxs-lookup"><span data-stu-id="543fb-117">If the topic is **NULL**, conversations for all available topics are requested.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="543fb-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="543fb-118">Remarks</span></span>

<span data-ttu-id="543fb-119">Se la parola di basso livello *di lParam* è **NULL,** qualsiasi applicazione server può rispondere.</span><span class="sxs-lookup"><span data-stu-id="543fb-119">If the low-order word of *lParam* is **NULL**, any server application can respond.</span></span> <span data-ttu-id="543fb-120">Se la parola di ordine superiore di *lParam* è **NULL,** qualsiasi argomento è valido.</span><span class="sxs-lookup"><span data-stu-id="543fb-120">If the high-order word of *lParam* is **NULL**, any topic is valid.</span></span> <span data-ttu-id="543fb-121">Quando si riceve una richiesta WM DDE INITIATE con la parola più alta del parametro *lParam* impostata su **NULL,** un server deve inviare un messaggio WM **\_ \_ DDE** [**\_ \_ ACK**](wm-dde-ack.md) per ognuno degli argomenti supportati.</span><span class="sxs-lookup"><span data-stu-id="543fb-121">Upon receiving a **WM\_DDE\_INITIATE** request with the high-order word of the *lParam* parameter set to **NULL**, a server must send a [**WM\_DDE\_ACK**](wm-dde-ack.md) message for each of the topics it supports.</span></span>

### <a name="sending"></a><span data-ttu-id="543fb-122">Invio</span><span class="sxs-lookup"><span data-stu-id="543fb-122">Sending</span></span>

<span data-ttu-id="543fb-123">Il client trasmette il messaggio a tutte le finestre di primo livello impostando il primo parametro di [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) su **HWND \_ BROADCAST**.</span><span class="sxs-lookup"><span data-stu-id="543fb-123">The client broadcasts the message to all top-level windows by setting the first parameter of [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) to **HWND\_BROADCAST**.</span></span>

<span data-ttu-id="543fb-124">Se l'applicazione client ha già ottenuto l'handle di finestra del server desiderato, può inviare **WM \_ DDE \_ INITIATE** direttamente alla finestra del server passando l'handle di finestra del server come primo parametro di [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage).</span><span class="sxs-lookup"><span data-stu-id="543fb-124">If the client application has already obtained the window handle of the desired server, it can send **WM\_DDE\_INITIATE** directly to the server window by passing the server's window handle as the first parameter of [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage).</span></span>

<span data-ttu-id="543fb-125">L'applicazione client alloca atom chiamando la [**funzione GlobalAddAtom.**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma)</span><span class="sxs-lookup"><span data-stu-id="543fb-125">The client application allocates atoms by calling the [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) function.</span></span>

<span data-ttu-id="543fb-126">Quando [**sendMessage viene**](/windows/desktop/api/winuser/nf-winuser-sendmessage) restituito, l'applicazione client deve eliminare gli atom.</span><span class="sxs-lookup"><span data-stu-id="543fb-126">When [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) returns, the client application must delete the atoms.</span></span>

### <a name="receiving"></a><span data-ttu-id="543fb-127">Ricezione</span><span class="sxs-lookup"><span data-stu-id="543fb-127">Receiving</span></span>

<span data-ttu-id="543fb-128">Per completare l'avvio di una conversazione, l'applicazione server deve rispondere con uno o più messaggi [**\_ WM DDE \_ ACK,**](wm-dde-ack.md) in cui ogni messaggio è relativo a un argomento separato.</span><span class="sxs-lookup"><span data-stu-id="543fb-128">To complete the initiation of a conversation, the server application must respond with one or more [**WM\_DDE\_ACK**](wm-dde-ack.md) messages, where each message is for a separate topic.</span></span> <span data-ttu-id="543fb-129">Quando si invia un messaggio **\_ WM DDE \_ ACK,** il server deve creare nuovi atomi e non riusare gli atomi inviati con **WM \_ DDE \_ INITIATE.**</span><span class="sxs-lookup"><span data-stu-id="543fb-129">When sending **WM\_DDE\_ACK** message, the server should create new atoms; it should not reuse the atoms sent with **WM\_DDE\_INITIATE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="543fb-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="543fb-130">Requirements</span></span>



| <span data-ttu-id="543fb-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="543fb-131">Requirement</span></span> | <span data-ttu-id="543fb-132">Valore</span><span class="sxs-lookup"><span data-stu-id="543fb-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="543fb-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="543fb-133">Minimum supported client</span></span><br/> | <span data-ttu-id="543fb-134">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="543fb-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="543fb-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="543fb-135">Minimum supported server</span></span><br/> | <span data-ttu-id="543fb-136">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="543fb-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="543fb-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="543fb-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="543fb-138"><dt>Dde.h (includere Windows.h)</dt></span><span class="sxs-lookup"><span data-stu-id="543fb-138"><dt>Dde.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="543fb-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="543fb-139">See also</span></span>

<dl> <dt>

<span data-ttu-id="543fb-140">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="543fb-140">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="543fb-141">**GlobalAddAtom**</span><span class="sxs-lookup"><span data-stu-id="543fb-141">**GlobalAddAtom**</span></span>](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma)
</dt> <dt>

[<span data-ttu-id="543fb-142">**PostMessage**</span><span class="sxs-lookup"><span data-stu-id="543fb-142">**PostMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[<span data-ttu-id="543fb-143">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="543fb-143">**SendMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[<span data-ttu-id="543fb-144">**WM \_ DDE \_ ACK**</span><span class="sxs-lookup"><span data-stu-id="543fb-144">**WM\_DDE\_ACK**</span></span>](wm-dde-ack.md)
</dt> <dt>

<span data-ttu-id="543fb-145">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="543fb-145">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="543fb-146">Informazioni Dynamic Data Exchange</span><span class="sxs-lookup"><span data-stu-id="543fb-146">About Dynamic Data Exchange</span></span>](about-dynamic-data-exchange.md)
</dt> </dl>

 

