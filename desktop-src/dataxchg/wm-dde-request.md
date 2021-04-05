---
title: Messaggio di WM_DDE_REQUEST (DDE. h)
description: Un'applicazione client di Dynamic Data Exchange (DDE) Invia un \_ \_ messaggio di richiesta DDE di WM a un'applicazione server DDE per richiedere il valore di un elemento di dati. Per pubblicare questo messaggio, chiamare la funzione PostMessage con i parametri seguenti.
ms.assetid: 922452d2-455c-43e1-a8a8-e3c52b0fab51
keywords:
- Scambio di dati del messaggio WM_DDE_REQUEST
topic_type:
- apiref
api_name:
- WM_DDE_REQUEST
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f7d5eab75d3b7298d78547b17fccfb164a47ae4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741087"
---
# <a name="wm_dde_request-message"></a><span data-ttu-id="e6c57-105">\_Messaggio di \_ richiesta DDE WM</span><span class="sxs-lookup"><span data-stu-id="e6c57-105">WM\_DDE\_REQUEST message</span></span>

<span data-ttu-id="e6c57-106">Un'applicazione client di Dynamic Data Exchange (DDE) Invia un messaggio di **\_ \_ richiesta DDE di WM** a un'applicazione server DDE per richiedere il valore di un elemento di dati.</span><span class="sxs-lookup"><span data-stu-id="e6c57-106">A Dynamic Data Exchange (DDE) client application posts a **WM\_DDE\_REQUEST** message to a DDE server application to request the value of a data item.</span></span>

<span data-ttu-id="e6c57-107">Per pubblicare questo messaggio, chiamare la funzione [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) con i parametri seguenti.</span><span class="sxs-lookup"><span data-stu-id="e6c57-107">To post this message, call the [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) function with the following parameters.</span></span>


```C++
#define WM_DDE_REQUEST     0x03E6
```



## <a name="parameters"></a><span data-ttu-id="e6c57-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="e6c57-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6c57-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e6c57-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e6c57-110">Handle per la finestra client che invia il messaggio.</span><span class="sxs-lookup"><span data-stu-id="e6c57-110">A handle to the client window sending the message.</span></span>

</dd> <dt>

<span data-ttu-id="e6c57-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e6c57-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e6c57-112">La parola di ordine inferiore specifica un formato degli Appunti standard o registrato.</span><span class="sxs-lookup"><span data-stu-id="e6c57-112">The low-order word specifies a standard or registered clipboard format.</span></span>

<span data-ttu-id="e6c57-113">La parola più ordinata contiene un Atom che identifica l'elemento dati richiesto dal server.</span><span class="sxs-lookup"><span data-stu-id="e6c57-113">The high-order word contains an atom that identifies the data item requested from the server.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e6c57-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="e6c57-114">Remarks</span></span>

### <a name="posting"></a><span data-ttu-id="e6c57-115">Distacco</span><span class="sxs-lookup"><span data-stu-id="e6c57-115">Posting</span></span>

<span data-ttu-id="e6c57-116">L'applicazione client alloca il Atom chiamando la funzione [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) .</span><span class="sxs-lookup"><span data-stu-id="e6c57-116">The client application allocates the atom by calling the [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) function.</span></span>

### <a name="receiving"></a><span data-ttu-id="e6c57-117">Ricezione</span><span class="sxs-lookup"><span data-stu-id="e6c57-117">Receiving</span></span>

<span data-ttu-id="e6c57-118">Se l'applicazione ricevente (Server) può soddisfare la richiesta, risponde con un messaggio [**di \_ \_ dati DDE WM**](wm-dde-data.md) contenente i dati richiesti.</span><span class="sxs-lookup"><span data-stu-id="e6c57-118">If the receiving (server) application can satisfy the request, it responds with a [**WM\_DDE\_DATA**](wm-dde-data.md) message containing the requested data.</span></span> <span data-ttu-id="e6c57-119">In caso contrario, risponde con un messaggio [**di \_ \_ ACK DDE WM**](wm-dde-ack.md) negativo.</span><span class="sxs-lookup"><span data-stu-id="e6c57-119">Otherwise, it responds with a negative [**WM\_DDE\_ACK**](wm-dde-ack.md) message.</span></span>

<span data-ttu-id="e6c57-120">Quando si rispondono a un messaggio [**WM \_ DDE \_**](wm-dde-data.md) o a un messaggio [**\_ \_ ACK DDE**](wm-dde-ack.md) , l'applicazione server può riutilizzare il formato Atom o eliminare l'Atom e crearne uno nuovo.</span><span class="sxs-lookup"><span data-stu-id="e6c57-120">When responding with either a [**WM\_DDE\_DATA**](wm-dde-data.md) or [**WM\_DDE\_ACK**](wm-dde-ack.md) message, the server application can either reuse the atom or it can delete the atom and create a new one.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6c57-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e6c57-121">Requirements</span></span>



| <span data-ttu-id="e6c57-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6c57-122">Requirement</span></span> | <span data-ttu-id="e6c57-123">Valore</span><span class="sxs-lookup"><span data-stu-id="e6c57-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6c57-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e6c57-124">Minimum supported client</span></span><br/> | <span data-ttu-id="e6c57-125">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e6c57-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="e6c57-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e6c57-126">Minimum supported server</span></span><br/> | <span data-ttu-id="e6c57-127">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e6c57-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="e6c57-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e6c57-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="e6c57-129"><dt>DDE. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e6c57-129"><dt>Dde.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6c57-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e6c57-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="e6c57-131">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="e6c57-131">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="e6c57-132">**GlobalAddAtom**</span><span class="sxs-lookup"><span data-stu-id="e6c57-132">**GlobalAddAtom**</span></span>](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma)
</dt> <dt>

[<span data-ttu-id="e6c57-133">**PackDDElParam**</span><span class="sxs-lookup"><span data-stu-id="e6c57-133">**PackDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-packddelparam)
</dt> <dt>

[<span data-ttu-id="e6c57-134">**PostMessage**</span><span class="sxs-lookup"><span data-stu-id="e6c57-134">**PostMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[<span data-ttu-id="e6c57-135">**ReuseDDElParam**</span><span class="sxs-lookup"><span data-stu-id="e6c57-135">**ReuseDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-reuseddelparam)
</dt> <dt>

[<span data-ttu-id="e6c57-136">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="e6c57-136">**SendMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[<span data-ttu-id="e6c57-137">**UnpackDDElParam**</span><span class="sxs-lookup"><span data-stu-id="e6c57-137">**UnpackDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-unpackddelparam)
</dt> <dt>

[<span data-ttu-id="e6c57-138">**\_ACK DDE \_ WM**</span><span class="sxs-lookup"><span data-stu-id="e6c57-138">**WM\_DDE\_ACK**</span></span>](wm-dde-ack.md)
</dt> <dt>

[<span data-ttu-id="e6c57-139">**\_dati DDE di WM \_**</span><span class="sxs-lookup"><span data-stu-id="e6c57-139">**WM\_DDE\_DATA**</span></span>](wm-dde-data.md)
</dt> <dt>

<span data-ttu-id="e6c57-140">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="e6c57-140">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="e6c57-141">Informazioni su Dynamic Data Exchange</span><span class="sxs-lookup"><span data-stu-id="e6c57-141">About Dynamic Data Exchange</span></span>](about-dynamic-data-exchange.md)
</dt> </dl>

 

