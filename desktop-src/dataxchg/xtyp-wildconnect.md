---
title: Transazione XTYP_WILDCONNECT (DDEML. h)
description: Consente a un client di stabilire una conversazione su ognuna delle coppie nome servizio e nome argomento del server che corrispondono al nome del servizio e al nome dell'argomento specificati.
ms.assetid: 4651e14f-ca13-412e-853d-326a13db78e4
keywords:
- Scambio di dati delle transazioni XTYP_WILDCONNECT
topic_type:
- apiref
api_name:
- XTYP_WILDCONNECT
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc63d6c367aebc440418beaabb0a06f05b0df967
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301595"
---
# <a name="xtyp_wildconnect-transaction"></a><span data-ttu-id="390a6-104">\_Transazione WILDCONNECT XTYP</span><span class="sxs-lookup"><span data-stu-id="390a6-104">XTYP\_WILDCONNECT transaction</span></span>

<span data-ttu-id="390a6-105">Consente a un client di stabilire una conversazione su ognuna delle coppie nome servizio e nome argomento del server che corrispondono al nome del servizio e al nome dell'argomento specificati.</span><span class="sxs-lookup"><span data-stu-id="390a6-105">Enables a client to establish a conversation on each of the server's service name and topic name pairs that match the specified service name and topic name.</span></span> <span data-ttu-id="390a6-106">Una funzione di callback del server Dynamic Data Exchange (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), riceve questa transazione quando un client specifica un nome di servizio **null** , un nome di argomento **null** o entrambi in una chiamata alla funzione [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) o [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) .</span><span class="sxs-lookup"><span data-stu-id="390a6-106">A Dynamic Data Exchange (DDE) server callback function, [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), receives this transaction when a client specifies a **NULL** service name, a **NULL** topic name, or both in a call to the [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) or [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) function.</span></span>


```C++
#define     XCLASS_DATA              0x2000
#define     XTYPF_NOBLOCK            0x0002
#define     XTYP_WILDCONNECT        (0x00E0 | XCLASS_DATA | XTYPF_NOBLOCK)
```



## <a name="parameters"></a><span data-ttu-id="390a6-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="390a6-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="390a6-108">*uType*</span><span class="sxs-lookup"><span data-stu-id="390a6-108">*uType*</span></span> 
</dt> <dd>

<span data-ttu-id="390a6-109">Tipo di transazione.</span><span class="sxs-lookup"><span data-stu-id="390a6-109">The transaction type.</span></span>

</dd> <dt>

<span data-ttu-id="390a6-110">*uFmt*</span><span class="sxs-lookup"><span data-stu-id="390a6-110">*uFmt*</span></span> 
</dt> <dd>

<span data-ttu-id="390a6-111">Non usato.</span><span class="sxs-lookup"><span data-stu-id="390a6-111">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="390a6-112">*hconv*</span><span class="sxs-lookup"><span data-stu-id="390a6-112">*hconv*</span></span> 
</dt> <dd>

<span data-ttu-id="390a6-113">Non usato.</span><span class="sxs-lookup"><span data-stu-id="390a6-113">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="390a6-114">*hsz1*</span><span class="sxs-lookup"><span data-stu-id="390a6-114">*hsz1*</span></span> 
</dt> <dd>

<span data-ttu-id="390a6-115">Handle per il nome dell'argomento.</span><span class="sxs-lookup"><span data-stu-id="390a6-115">A handle to the topic name.</span></span> <span data-ttu-id="390a6-116">Se questo parametro è **null**, il client richiede una conversazione su tutti i nomi di argomento supportati dal server.</span><span class="sxs-lookup"><span data-stu-id="390a6-116">If this parameter is **NULL**, the client is requesting a conversation on all topic names that the server supports.</span></span>

</dd> <dt>

<span data-ttu-id="390a6-117">*hsz2*</span><span class="sxs-lookup"><span data-stu-id="390a6-117">*hsz2*</span></span> 
</dt> <dd>

<span data-ttu-id="390a6-118">Handle per il nome del servizio.</span><span class="sxs-lookup"><span data-stu-id="390a6-118">A handle to the service name.</span></span> <span data-ttu-id="390a6-119">Se questo parametro è **null**, il client richiede una conversazione su tutti i nomi di servizio supportati dal server.</span><span class="sxs-lookup"><span data-stu-id="390a6-119">If this parameter is **NULL**, the client is requesting a conversation on all service names that the server supports.</span></span>

</dd> <dt>

<span data-ttu-id="390a6-120">*hdata*</span><span class="sxs-lookup"><span data-stu-id="390a6-120">*hdata*</span></span> 
</dt> <dd>

<span data-ttu-id="390a6-121">Non usato.</span><span class="sxs-lookup"><span data-stu-id="390a6-121">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="390a6-122">*dwData1*</span><span class="sxs-lookup"><span data-stu-id="390a6-122">*dwData1*</span></span> 
</dt> <dd>

<span data-ttu-id="390a6-123">Puntatore a una struttura [**CONVCONTEXT**](/windows/win32/api/ddeml/ns-ddeml-convcontext) che contiene informazioni di contesto per la conversazione.</span><span class="sxs-lookup"><span data-stu-id="390a6-123">A pointer to a [**CONVCONTEXT**](/windows/win32/api/ddeml/ns-ddeml-convcontext) structure that contains context information for the conversation.</span></span> <span data-ttu-id="390a6-124">Se il client non è un'applicazione DDEML, questo parametro è impostato su 0.</span><span class="sxs-lookup"><span data-stu-id="390a6-124">If the client is not a DDEML application, this parameter is set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="390a6-125">*dwData2*</span><span class="sxs-lookup"><span data-stu-id="390a6-125">*dwData2*</span></span> 
</dt> <dd>

<span data-ttu-id="390a6-126">Specifica se il client è la stessa istanza dell'applicazione del server.</span><span class="sxs-lookup"><span data-stu-id="390a6-126">Specifies whether the client is the same application instance as the server.</span></span> <span data-ttu-id="390a6-127">Se il parametro è 1, il client è la stessa istanza.</span><span class="sxs-lookup"><span data-stu-id="390a6-127">If the parameter is 1, the client is same instance.</span></span> <span data-ttu-id="390a6-128">Se il parametro è 0, il client è un'istanza diversa.</span><span class="sxs-lookup"><span data-stu-id="390a6-128">If the parameter is 0, the client is a different instance.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="390a6-129">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="390a6-129">Return value</span></span>

<span data-ttu-id="390a6-130">Il server deve restituire un handle di dati che identifichi una matrice di strutture [**HSZPAIR**](/windows/win32/api/ddeml/ns-ddeml-hszpair) .</span><span class="sxs-lookup"><span data-stu-id="390a6-130">The server should return a data handle that identifies an array of [**HSZPAIR**](/windows/win32/api/ddeml/ns-ddeml-hszpair) structures.</span></span> <span data-ttu-id="390a6-131">La matrice deve contenere una struttura per ogni coppia nome-servizio e nome-argomento che corrisponde alla coppia nome-servizio e nome-argomento richiesta dal client.</span><span class="sxs-lookup"><span data-stu-id="390a6-131">The array should contain one structure for each service-name and topic-name pair that matches the service-name and topic-name pair requested by the client.</span></span> <span data-ttu-id="390a6-132">La matrice deve terminare con un handle di stringa **null** .</span><span class="sxs-lookup"><span data-stu-id="390a6-132">The array must be terminated by a **NULL** string handle.</span></span> <span data-ttu-id="390a6-133">Il sistema invia la transazione di [**\_ \_ conferma XTYP Connect**](xtyp-connect-confirm.md) al server per confermare ogni conversazione e passare gli handle di conversazione al server.</span><span class="sxs-lookup"><span data-stu-id="390a6-133">The system sends the [**XTYP\_CONNECT\_CONFIRM**](xtyp-connect-confirm.md) transaction to the server to confirm each conversation and to pass the conversation handles to the server.</span></span> <span data-ttu-id="390a6-134">Il server non riceverà queste conferme se ha specificato il flag **CBF \_ Skip \_ Connect \_ confirms** nella funzione [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .</span><span class="sxs-lookup"><span data-stu-id="390a6-134">The server will not receive these confirmations if it specified the **CBF\_SKIP\_CONNECT\_CONFIRMS** flag in the [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) function.</span></span>

<span data-ttu-id="390a6-135">Il server deve restituire **null** per rifiutare la **transazione \_ WILDCONNECT XTYP** .</span><span class="sxs-lookup"><span data-stu-id="390a6-135">The server should return **NULL** to refuse the **XTYP\_WILDCONNECT** transaction.</span></span>

## <a name="remarks"></a><span data-ttu-id="390a6-136">Commenti</span><span class="sxs-lookup"><span data-stu-id="390a6-136">Remarks</span></span>

<span data-ttu-id="390a6-137">Questa transazione viene filtrata se l'applicazione server ha specificato il flag **CBF \_ Fail \_ Connections** nella funzione [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .</span><span class="sxs-lookup"><span data-stu-id="390a6-137">This transaction is filtered if the server application specified the **CBF\_FAIL\_CONNECTIONS** flag in the [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) function.</span></span>

<span data-ttu-id="390a6-138">Un server non è in grado di bloccare questo tipo di transazione. il \_ codice restituito del blocco CBR viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="390a6-138">A server cannot block this transaction type; the CBR\_BLOCK return code is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="390a6-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="390a6-139">Requirements</span></span>



| <span data-ttu-id="390a6-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="390a6-140">Requirement</span></span> | <span data-ttu-id="390a6-141">Valore</span><span class="sxs-lookup"><span data-stu-id="390a6-141">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="390a6-142">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="390a6-142">Minimum supported client</span></span><br/> | <span data-ttu-id="390a6-143">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="390a6-143">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="390a6-144">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="390a6-144">Minimum supported server</span></span><br/> | <span data-ttu-id="390a6-145">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="390a6-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="390a6-146">Intestazione</span><span class="sxs-lookup"><span data-stu-id="390a6-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="390a6-147"><dt>DDEML. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="390a6-147"><dt>Ddeml.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="390a6-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="390a6-148">See also</span></span>

<dl> <dt>

<span data-ttu-id="390a6-149">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="390a6-149">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="390a6-150">**CONVCONTEXT**</span><span class="sxs-lookup"><span data-stu-id="390a6-150">**CONVCONTEXT**</span></span>](/windows/win32/api/ddeml/ns-ddeml-convcontext)
</dt> <dt>

[<span data-ttu-id="390a6-151">**DdeConnect**</span><span class="sxs-lookup"><span data-stu-id="390a6-151">**DdeConnect**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect)
</dt> <dt>

[<span data-ttu-id="390a6-152">**DdeInitialize**</span><span class="sxs-lookup"><span data-stu-id="390a6-152">**DdeInitialize**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

[<span data-ttu-id="390a6-153">**HSZPAIR**</span><span class="sxs-lookup"><span data-stu-id="390a6-153">**HSZPAIR**</span></span>](/windows/win32/api/ddeml/ns-ddeml-hszpair)
</dt> <dt>

<span data-ttu-id="390a6-154">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="390a6-154">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="390a6-155">Libreria di gestione Dynamic Data Exchange</span><span class="sxs-lookup"><span data-stu-id="390a6-155">Dynamic Data Exchange Management Library</span></span>](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

