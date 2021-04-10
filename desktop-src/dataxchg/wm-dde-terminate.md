---
title: Messaggio di WM_DDE_TERMINATE (DDE. h)
description: Un'applicazione Dynamic Data Exchange (DDE) (client o server) Invia un \_ \_ messaggio di terminazione DDE WM per terminare una conversazione. Per pubblicare questo messaggio, chiamare la funzione PostMessage con i parametri seguenti.
ms.assetid: 4fc162c0-ccc2-44e3-9c07-d49d7426af8b
keywords:
- Scambio di dati del messaggio WM_DDE_TERMINATE
topic_type:
- apiref
api_name:
- WM_DDE_TERMINATE
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 105b4a7daab87b1311a58a7b5e5805bbd81e73ce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119519"
---
# <a name="wm_dde_terminate-message"></a><span data-ttu-id="df652-105">\_Messaggio di \_ terminazione DDE WM</span><span class="sxs-lookup"><span data-stu-id="df652-105">WM\_DDE\_TERMINATE message</span></span>

<span data-ttu-id="df652-106">Un'applicazione Dynamic Data Exchange (DDE) (client o server) Invia un messaggio di **\_ \_ terminazione DDE WM** per terminare una conversazione.</span><span class="sxs-lookup"><span data-stu-id="df652-106">A Dynamic Data Exchange (DDE) application (client or server) posts a **WM\_DDE\_TERMINATE** message to terminate a conversation.</span></span>

<span data-ttu-id="df652-107">Per pubblicare questo messaggio, chiamare la funzione [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) con i parametri seguenti.</span><span class="sxs-lookup"><span data-stu-id="df652-107">To post this message, call the [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) function with the following parameters.</span></span>


```C++
#define WM_DDE_TERMINATE       0x03E1
```



## <a name="parameters"></a><span data-ttu-id="df652-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="df652-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df652-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="df652-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="df652-110">Handle per la finestra client o server che pubblica il messaggio.</span><span class="sxs-lookup"><span data-stu-id="df652-110">A handle to the client or server window posting the message.</span></span>

</dd> <dt>

<span data-ttu-id="df652-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="df652-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="df652-112">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="df652-112">This parameter is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="df652-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="df652-113">Remarks</span></span>

### <a name="posting"></a><span data-ttu-id="df652-114">Distacco</span><span class="sxs-lookup"><span data-stu-id="df652-114">Posting</span></span>

<span data-ttu-id="df652-115">Durante l'attesa della conferma della chiusura, l'applicazione di pubblicazione non deve inviare altri messaggi all'applicazione ricevente.</span><span class="sxs-lookup"><span data-stu-id="df652-115">While waiting for confirmation of the termination, the posting application should not post any other messages to the receiving application.</span></span> <span data-ttu-id="df652-116">Se l'applicazione mittente riceve messaggi (diversi da **WM \_ DDE \_ Terminate**) dall'applicazione ricevente, deve eliminare tutti gli oggetti di memoria condivisa o gli atomi che accompagnano i messaggi, ad eccezione degli oggetti memoria globale associati ai messaggi di [**\_ \_ dati DDE**](wm-dde-data.md) di [**WM o WM DDE per \_ \_**](wm-dde-poke.md) i quali non è impostato il membro **fRelease** .</span><span class="sxs-lookup"><span data-stu-id="df652-116">If the sending application receives messages (other than **WM\_DDE\_TERMINATE**) from the receiving application, it should delete any atoms or shared memory objects accompanying the messages, except global memory objects associated with [**WM\_DDE\_POKE**](wm-dde-poke.md) or [**WM\_DDE\_DATA**](wm-dde-data.md) messages that do not have the **fRelease** member set.</span></span>

### <a name="receiving"></a><span data-ttu-id="df652-117">Ricezione</span><span class="sxs-lookup"><span data-stu-id="df652-117">Receiving</span></span>

<span data-ttu-id="df652-118">È necessario che l'applicazione client o server risponda inviando un messaggio di **\_ \_ terminazione DDE WM** .</span><span class="sxs-lookup"><span data-stu-id="df652-118">The client or server application should respond by posting a **WM\_DDE\_TERMINATE** message.</span></span>

## <a name="requirements"></a><span data-ttu-id="df652-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="df652-119">Requirements</span></span>



| <span data-ttu-id="df652-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="df652-120">Requirement</span></span> | <span data-ttu-id="df652-121">Valore</span><span class="sxs-lookup"><span data-stu-id="df652-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df652-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="df652-122">Minimum supported client</span></span><br/> | <span data-ttu-id="df652-123">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="df652-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="df652-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="df652-124">Minimum supported server</span></span><br/> | <span data-ttu-id="df652-125">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="df652-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="df652-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="df652-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="df652-127"><dt>DDE. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="df652-127"><dt>Dde.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df652-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="df652-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="df652-129">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="df652-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="df652-130">**PostMessage**</span><span class="sxs-lookup"><span data-stu-id="df652-130">**PostMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[<span data-ttu-id="df652-131">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="df652-131">**SendMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[<span data-ttu-id="df652-132">**\_dati DDE di WM \_**</span><span class="sxs-lookup"><span data-stu-id="df652-132">**WM\_DDE\_DATA**</span></span>](wm-dde-data.md)
</dt> <dt>

[<span data-ttu-id="df652-133">**\_poke DDE \_ WM**</span><span class="sxs-lookup"><span data-stu-id="df652-133">**WM\_DDE\_POKE**</span></span>](wm-dde-poke.md)
</dt> <dt>

<span data-ttu-id="df652-134">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="df652-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="df652-135">Informazioni su Dynamic Data Exchange</span><span class="sxs-lookup"><span data-stu-id="df652-135">About Dynamic Data Exchange</span></span>](about-dynamic-data-exchange.md)
</dt> </dl>

 

