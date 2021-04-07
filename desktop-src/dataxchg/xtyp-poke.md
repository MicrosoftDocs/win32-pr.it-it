---
title: Transazione XTYP_POKE (DDEML. h)
description: Un client utilizza la \_ transazione poke XTYP per inviare dati non richiesti al server. Una funzione di callback del server Dynamic Data Exchange (DDE), DdeCallback, riceve questa transazione quando un client specifica XTYP \_ poke nella funzione DdeClientTransaction.
ms.assetid: 63c6115e-24f8-4f35-8397-8be63110b21f
keywords:
- Scambio di dati delle transazioni XTYP_POKE
topic_type:
- apiref
api_name:
- XTYP_POKE
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e538f72b7a736ed9be5cf3e1d83e8729f42ef83d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964131"
---
# <a name="xtyp_poke-transaction"></a><span data-ttu-id="c8528-105">\_Transazione poke XTYP</span><span class="sxs-lookup"><span data-stu-id="c8528-105">XTYP\_POKE transaction</span></span>

<span data-ttu-id="c8528-106">Un client utilizza la **transazione \_ poke XTYP** per inviare dati non richiesti al server.</span><span class="sxs-lookup"><span data-stu-id="c8528-106">A client uses the **XTYP\_POKE** transaction to send unsolicited data to the server.</span></span> <span data-ttu-id="c8528-107">Una funzione di callback del server Dynamic Data Exchange (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), riceve questa transazione quando un client specifica **XTYP \_ poke** nella funzione [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) .</span><span class="sxs-lookup"><span data-stu-id="c8528-107">A Dynamic Data Exchange (DDE) server callback function, [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), receives this transaction when a client specifies **XTYP\_POKE** in the [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) function.</span></span>


```C++
#define     XCLASS_FLAGS             0x4000
#define     XTYP_POKE               (0x0090 | XCLASS_FLAGS         )
```



## <a name="parameters"></a><span data-ttu-id="c8528-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="c8528-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8528-109">*uType*</span><span class="sxs-lookup"><span data-stu-id="c8528-109">*uType*</span></span> 
</dt> <dd>

<span data-ttu-id="c8528-110">Tipo di transazione.</span><span class="sxs-lookup"><span data-stu-id="c8528-110">The transaction type.</span></span>

</dd> <dt>

<span data-ttu-id="c8528-111">*uFmt*</span><span class="sxs-lookup"><span data-stu-id="c8528-111">*uFmt*</span></span> 
</dt> <dd>

<span data-ttu-id="c8528-112">Il formato dei dati inviati dal server.</span><span class="sxs-lookup"><span data-stu-id="c8528-112">The format of the data sent from the server.</span></span>

</dd> <dt>

<span data-ttu-id="c8528-113">*hconv*</span><span class="sxs-lookup"><span data-stu-id="c8528-113">*hconv*</span></span> 
</dt> <dd>

<span data-ttu-id="c8528-114">Handle per la conversazione.</span><span class="sxs-lookup"><span data-stu-id="c8528-114">A handle to the conversation.</span></span>

</dd> <dt>

<span data-ttu-id="c8528-115">*hsz1*</span><span class="sxs-lookup"><span data-stu-id="c8528-115">*hsz1*</span></span> 
</dt> <dd>

<span data-ttu-id="c8528-116">Handle per il nome dell'argomento.</span><span class="sxs-lookup"><span data-stu-id="c8528-116">A handle to the topic name.</span></span>

</dd> <dt>

<span data-ttu-id="c8528-117">*hsz2*</span><span class="sxs-lookup"><span data-stu-id="c8528-117">*hsz2*</span></span> 
</dt> <dd>

<span data-ttu-id="c8528-118">Handle per il nome dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="c8528-118">A handle to the item name.</span></span>

</dd> <dt>

<span data-ttu-id="c8528-119">*hdata*</span><span class="sxs-lookup"><span data-stu-id="c8528-119">*hdata*</span></span> 
</dt> <dd>

<span data-ttu-id="c8528-120">Handle per i dati inviati dal client al server.</span><span class="sxs-lookup"><span data-stu-id="c8528-120">A handle to the data that the client is sending to the server.</span></span>

</dd> <dt>

<span data-ttu-id="c8528-121">*dwData1*</span><span class="sxs-lookup"><span data-stu-id="c8528-121">*dwData1*</span></span> 
</dt> <dd>

<span data-ttu-id="c8528-122">Non usato.</span><span class="sxs-lookup"><span data-stu-id="c8528-122">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="c8528-123">*dwData2*</span><span class="sxs-lookup"><span data-stu-id="c8528-123">*dwData2*</span></span> 
</dt> <dd>

<span data-ttu-id="c8528-124">Non usato.</span><span class="sxs-lookup"><span data-stu-id="c8528-124">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8528-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c8528-125">Return value</span></span>

<span data-ttu-id="c8528-126">Una funzione di callback del server deve restituire il flag **\_ fack DDE** se elabora questa transazione, il flag **\_ FBUSY DDE** se è troppo occupato per elaborare la transazione o il flag **\_ FNOTPROCESSED DDE** se rifiuta questa transazione.</span><span class="sxs-lookup"><span data-stu-id="c8528-126">A server callback function should return the **DDE\_FACK** flag if it processes this transaction, the **DDE\_FBUSY** flag if it is too busy to process this transaction, or the **DDE\_FNOTPROCESSED** flag if it rejects this transaction.</span></span>

## <a name="remarks"></a><span data-ttu-id="c8528-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="c8528-127">Remarks</span></span>

<span data-ttu-id="c8528-128">Questa transazione viene filtrata se l'applicazione server ha specificato il flag **CBF \_ Fail \_ pokes** nella funzione [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .</span><span class="sxs-lookup"><span data-stu-id="c8528-128">This transaction is filtered if the server application specified the **CBF\_FAIL\_POKES** flag in the [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8528-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c8528-129">Requirements</span></span>



| <span data-ttu-id="c8528-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="c8528-130">Requirement</span></span> | <span data-ttu-id="c8528-131">Valore</span><span class="sxs-lookup"><span data-stu-id="c8528-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8528-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c8528-132">Minimum supported client</span></span><br/> | <span data-ttu-id="c8528-133">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c8528-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="c8528-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c8528-134">Minimum supported server</span></span><br/> | <span data-ttu-id="c8528-135">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c8528-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="c8528-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c8528-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="c8528-137"><dt>DDEML. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c8528-137"><dt>Ddeml.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8528-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c8528-138">See also</span></span>

<dl> <dt>

<span data-ttu-id="c8528-139">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="c8528-139">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c8528-140">**DdeClientTransaction**</span><span class="sxs-lookup"><span data-stu-id="c8528-140">**DdeClientTransaction**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)
</dt> <dt>

[<span data-ttu-id="c8528-141">**DdeInitialize**</span><span class="sxs-lookup"><span data-stu-id="c8528-141">**DdeInitialize**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

<span data-ttu-id="c8528-142">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="c8528-142">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="c8528-143">Libreria di gestione Dynamic Data Exchange</span><span class="sxs-lookup"><span data-stu-id="c8528-143">Dynamic Data Exchange Management Library</span></span>](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

