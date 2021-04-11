---
title: Transazione XTYP_CONNECT (DDEML. h)
description: Un client usa la \_ transazione di connessione XTYP per stabilire una conversazione.
ms.assetid: 74f43b10-f7ac-4370-9caa-7b9ddf3413ed
keywords:
- Scambio di dati delle transazioni XTYP_CONNECT
topic_type:
- apiref
api_name:
- XTYP_CONNECT
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2268994f1be000373691d6c25dbb7220d3e109e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120035"
---
# <a name="xtyp_connect-transaction"></a><span data-ttu-id="a7164-104">\_Transazione di connessione XTYP</span><span class="sxs-lookup"><span data-stu-id="a7164-104">XTYP\_CONNECT transaction</span></span>

<span data-ttu-id="a7164-105">Un client usa la transazione di **\_ connessione XTYP** per stabilire una conversazione.</span><span class="sxs-lookup"><span data-stu-id="a7164-105">A client uses the **XTYP\_CONNECT** transaction to establish a conversation.</span></span> <span data-ttu-id="a7164-106">Una funzione di callback del server Dynamic Data Exchange (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), riceve questa transazione quando un client specifica un nome di servizio supportato dal server (e un nome di argomento non **null**) in una chiamata alla funzione [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) .</span><span class="sxs-lookup"><span data-stu-id="a7164-106">A Dynamic Data Exchange (DDE) server callback function, [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), receives this transaction when a client specifies a service name that the server supports (and a topic name that is not **NULL**) in a call to the [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) function.</span></span>


```C++
#define     XCLASS_BOOL              0x1000
#define     XTYPF_NOBLOCK            0x0002
#define     XTYP_CONNECT            (0x0060 | XCLASS_BOOL | XTYPF_NOBLOCK)
```



## <a name="parameters"></a><span data-ttu-id="a7164-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="a7164-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7164-108">*uType*</span><span class="sxs-lookup"><span data-stu-id="a7164-108">*uType*</span></span> 
</dt> <dd>

<span data-ttu-id="a7164-109">Tipo di transazione.</span><span class="sxs-lookup"><span data-stu-id="a7164-109">The transaction type.</span></span>

</dd> <dt>

<span data-ttu-id="a7164-110">*uFmt*</span><span class="sxs-lookup"><span data-stu-id="a7164-110">*uFmt*</span></span> 
</dt> <dd>

<span data-ttu-id="a7164-111">Non usato.</span><span class="sxs-lookup"><span data-stu-id="a7164-111">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="a7164-112">*hconv*</span><span class="sxs-lookup"><span data-stu-id="a7164-112">*hconv*</span></span> 
</dt> <dd>

<span data-ttu-id="a7164-113">Non usato.</span><span class="sxs-lookup"><span data-stu-id="a7164-113">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="a7164-114">*hsz1*</span><span class="sxs-lookup"><span data-stu-id="a7164-114">*hsz1*</span></span> 
</dt> <dd>

<span data-ttu-id="a7164-115">Handle per il nome dell'argomento.</span><span class="sxs-lookup"><span data-stu-id="a7164-115">A handle to the topic name.</span></span>

</dd> <dt>

<span data-ttu-id="a7164-116">*hsz2*</span><span class="sxs-lookup"><span data-stu-id="a7164-116">*hsz2*</span></span> 
</dt> <dd>

<span data-ttu-id="a7164-117">Handle per il nome del servizio.</span><span class="sxs-lookup"><span data-stu-id="a7164-117">A handle to the service name.</span></span>

</dd> <dt>

<span data-ttu-id="a7164-118">*hdata*</span><span class="sxs-lookup"><span data-stu-id="a7164-118">*hdata*</span></span> 
</dt> <dd>

<span data-ttu-id="a7164-119">Non usato.</span><span class="sxs-lookup"><span data-stu-id="a7164-119">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="a7164-120">*dwData1*</span><span class="sxs-lookup"><span data-stu-id="a7164-120">*dwData1*</span></span> 
</dt> <dd>

<span data-ttu-id="a7164-121">Puntatore a una struttura [**CONVCONTEXT**](/windows/win32/api/ddeml/ns-ddeml-convcontext) che contiene informazioni di contesto per la conversazione.</span><span class="sxs-lookup"><span data-stu-id="a7164-121">A pointer to a [**CONVCONTEXT**](/windows/win32/api/ddeml/ns-ddeml-convcontext) structure that contains context information for the conversation.</span></span> <span data-ttu-id="a7164-122">Se il client non è un'applicazione DDEML, questo parametro è 0.</span><span class="sxs-lookup"><span data-stu-id="a7164-122">If the client is not a DDEML application, this parameter is 0.</span></span>

</dd> <dt>

<span data-ttu-id="a7164-123">*dwData2*</span><span class="sxs-lookup"><span data-stu-id="a7164-123">*dwData2*</span></span> 
</dt> <dd>

<span data-ttu-id="a7164-124">Specifica se il client è la stessa istanza dell'applicazione del server.</span><span class="sxs-lookup"><span data-stu-id="a7164-124">Specifies whether the client is the same application instance as the server.</span></span> <span data-ttu-id="a7164-125">Se il parametro è 1, il client è la stessa istanza.</span><span class="sxs-lookup"><span data-stu-id="a7164-125">If the parameter is 1, the client is the same instance.</span></span> <span data-ttu-id="a7164-126">Se il parametro è 0, il client è un'istanza diversa.</span><span class="sxs-lookup"><span data-stu-id="a7164-126">If the parameter is 0, the client is a different instance.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a7164-127">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a7164-127">Return value</span></span>

<span data-ttu-id="a7164-128">Una funzione di callback del server deve restituire **true** per consentire al client di stabilire una conversazione con il nome del servizio e la coppia di nomi di argomento specificati oppure la funzione deve restituire **false** per negare la conversazione.</span><span class="sxs-lookup"><span data-stu-id="a7164-128">A server callback function should return **TRUE** to allow the client to establish a conversation on the specified service name and topic name pair, or the function should return **FALSE** to deny the conversation.</span></span> <span data-ttu-id="a7164-129">Se la funzione di callback restituisce **true** e una conversazione viene stabilita correttamente, il sistema passa l'handle di conversazione al server eseguendo una [**XTYP \_ Connect \_ Confirm**](xtyp-connect-confirm.md) Transaction per la funzione di callback del server, a meno che il server non abbia specificato il flag **CBF \_ Skip \_ Connect \_ confirms** nella funzione [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .</span><span class="sxs-lookup"><span data-stu-id="a7164-129">If the callback function returns **TRUE** and a conversation is successfully established, the system passes the conversation handle to the server by issuing an [**XTYP\_CONNECT\_CONFIRM**](xtyp-connect-confirm.md) transaction to the server's callback function (unless the server specified the **CBF\_SKIP\_CONNECT\_CONFIRMS** flag in the [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) function).</span></span>

## <a name="remarks"></a><span data-ttu-id="a7164-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="a7164-130">Remarks</span></span>

<span data-ttu-id="a7164-131">Questa transazione viene filtrata se l'applicazione server ha specificato il flag **CBF \_ Fail \_ Connections** nella funzione [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .</span><span class="sxs-lookup"><span data-stu-id="a7164-131">This transaction is filtered if the server application specified the **CBF\_FAIL\_CONNECTIONS** flag in the [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) function.</span></span>

<span data-ttu-id="a7164-132">Un server non è in grado di bloccare questo tipo di transazione. il codice restituito del **\_ blocco CBR** viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="a7164-132">A server cannot block this transaction type; the **CBR\_BLOCK** return code is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7164-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a7164-133">Requirements</span></span>



| <span data-ttu-id="a7164-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="a7164-134">Requirement</span></span> | <span data-ttu-id="a7164-135">Valore</span><span class="sxs-lookup"><span data-stu-id="a7164-135">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7164-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a7164-136">Minimum supported client</span></span><br/> | <span data-ttu-id="a7164-137">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a7164-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="a7164-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a7164-138">Minimum supported server</span></span><br/> | <span data-ttu-id="a7164-139">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a7164-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="a7164-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a7164-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="a7164-141"><dt>DDEML. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a7164-141"><dt>Ddeml.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a7164-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a7164-142">See also</span></span>

<dl> <dt>

<span data-ttu-id="a7164-143">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="a7164-143">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="a7164-144">**CONVCONTEXT**</span><span class="sxs-lookup"><span data-stu-id="a7164-144">**CONVCONTEXT**</span></span>](/windows/win32/api/ddeml/ns-ddeml-convcontext)
</dt> <dt>

[<span data-ttu-id="a7164-145">**DdeConnect**</span><span class="sxs-lookup"><span data-stu-id="a7164-145">**DdeConnect**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect)
</dt> <dt>

[<span data-ttu-id="a7164-146">**DdeInitialize**</span><span class="sxs-lookup"><span data-stu-id="a7164-146">**DdeInitialize**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

<span data-ttu-id="a7164-147">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="a7164-147">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="a7164-148">Libreria di gestione Dynamic Data Exchange</span><span class="sxs-lookup"><span data-stu-id="a7164-148">Dynamic Data Exchange Management Library</span></span>](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

