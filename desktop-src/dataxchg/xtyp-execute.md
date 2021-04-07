---
title: Transazione XTYP_EXECUTE (DDEML. h)
description: Un client utilizza XTYP \_ Execute Transaction per inviare una stringa di comando al server. Una funzione di callback del server Dynamic Data Exchange (DDE), DdeCallback, riceve questa transazione quando un client specifica XTYP \_ Execute nella funzione DdeClientTransaction.
ms.assetid: 6001eb7d-59c0-49ec-97ce-26132891188c
keywords:
- Scambio di dati delle transazioni XTYP_EXECUTE
topic_type:
- apiref
api_name:
- XTYP_EXECUTE
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ff08bfa60d07f3b8333f1de808359f77984cbba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048619"
---
# <a name="xtyp_execute-transaction"></a><span data-ttu-id="81cf9-105">XTYP \_ Execute Transaction</span><span class="sxs-lookup"><span data-stu-id="81cf9-105">XTYP\_EXECUTE transaction</span></span>

<span data-ttu-id="81cf9-106">Un client utilizza **XTYP \_ Execute** Transaction per inviare una stringa di comando al server.</span><span class="sxs-lookup"><span data-stu-id="81cf9-106">A client uses the **XTYP\_EXECUTE** transaction to send a command string to the server.</span></span> <span data-ttu-id="81cf9-107">Una funzione di callback del server Dynamic Data Exchange (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), riceve questa transazione quando un client specifica **XTYP \_ Execute** nella funzione [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) .</span><span class="sxs-lookup"><span data-stu-id="81cf9-107">A Dynamic Data Exchange (DDE) server callback function, [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), receives this transaction when a client specifies **XTYP\_EXECUTE** in the [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) function.</span></span>


```C++
#define     XCLASS_FLAGS             0x4000
#define     XTYP_EXECUTE            (0x0050 | XCLASS_FLAGS         )
```



## <a name="parameters"></a><span data-ttu-id="81cf9-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="81cf9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81cf9-109">*uType*</span><span class="sxs-lookup"><span data-stu-id="81cf9-109">*uType*</span></span> 
</dt> <dd>

<span data-ttu-id="81cf9-110">Tipo di transazione.</span><span class="sxs-lookup"><span data-stu-id="81cf9-110">The transaction type.</span></span>

</dd> <dt>

<span data-ttu-id="81cf9-111">*uFmt*</span><span class="sxs-lookup"><span data-stu-id="81cf9-111">*uFmt*</span></span> 
</dt> <dd>

<span data-ttu-id="81cf9-112">Non usato.</span><span class="sxs-lookup"><span data-stu-id="81cf9-112">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="81cf9-113">*hconv*</span><span class="sxs-lookup"><span data-stu-id="81cf9-113">*hconv*</span></span> 
</dt> <dd>

<span data-ttu-id="81cf9-114">Handle per la conversazione.</span><span class="sxs-lookup"><span data-stu-id="81cf9-114">A handle to the conversation.</span></span>

</dd> <dt>

<span data-ttu-id="81cf9-115">*hsz1*</span><span class="sxs-lookup"><span data-stu-id="81cf9-115">*hsz1*</span></span> 
</dt> <dd>

<span data-ttu-id="81cf9-116">Handle per il nome dell'argomento.</span><span class="sxs-lookup"><span data-stu-id="81cf9-116">A handle to the topic name.</span></span>

</dd> <dt>

<span data-ttu-id="81cf9-117">*hsz2*</span><span class="sxs-lookup"><span data-stu-id="81cf9-117">*hsz2*</span></span> 
</dt> <dd>

<span data-ttu-id="81cf9-118">Non usato.</span><span class="sxs-lookup"><span data-stu-id="81cf9-118">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="81cf9-119">*hdata*</span><span class="sxs-lookup"><span data-stu-id="81cf9-119">*hdata*</span></span> 
</dt> <dd>

<span data-ttu-id="81cf9-120">Handle per la stringa di comando.</span><span class="sxs-lookup"><span data-stu-id="81cf9-120">A handle to the command string.</span></span>

</dd> <dt>

<span data-ttu-id="81cf9-121">*dwData1*</span><span class="sxs-lookup"><span data-stu-id="81cf9-121">*dwData1*</span></span> 
</dt> <dd>

<span data-ttu-id="81cf9-122">Non usato.</span><span class="sxs-lookup"><span data-stu-id="81cf9-122">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="81cf9-123">*dwData2*</span><span class="sxs-lookup"><span data-stu-id="81cf9-123">*dwData2*</span></span> 
</dt> <dd>

<span data-ttu-id="81cf9-124">Non usato.</span><span class="sxs-lookup"><span data-stu-id="81cf9-124">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81cf9-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="81cf9-125">Return value</span></span>

<span data-ttu-id="81cf9-126">Una funzione di callback del server deve restituire **\_ fack DDE** se elabora questa transazione, **DDE \_ FBUSY** se è troppo occupato per elaborare la transazione o **\_ FNOTPROCESSED DDE** se rifiuta questa transazione.</span><span class="sxs-lookup"><span data-stu-id="81cf9-126">A server callback function should return **DDE\_FACK** if it processes this transaction, **DDE\_FBUSY** if it is too busy to process this transaction, or **DDE\_FNOTPROCESSED** if it rejects this transaction.</span></span>

## <a name="remarks"></a><span data-ttu-id="81cf9-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="81cf9-127">Remarks</span></span>

<span data-ttu-id="81cf9-128">Questa transazione viene filtrata se l'applicazione server specificata il flag **CBF \_ Fail \_ executes** nella funzione [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .</span><span class="sxs-lookup"><span data-stu-id="81cf9-128">This transaction is filtered if the server application specified the **CBF\_FAIL\_EXECUTES** flag in the [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) function.</span></span>

<span data-ttu-id="81cf9-129">Un'applicazione deve liberare l'handle di dati ottenuto durante la transazione.</span><span class="sxs-lookup"><span data-stu-id="81cf9-129">An application must free the data handle obtained during this transaction.</span></span> <span data-ttu-id="81cf9-130">Un'applicazione, tuttavia, deve copiare la stringa di comando associata all'handle di dati se l'applicazione deve elaborare la stringa dopo che la funzione di callback restituisce.</span><span class="sxs-lookup"><span data-stu-id="81cf9-130">An application must, however, copy the command string associated with the data handle if the application must process the string after the callback function returns.</span></span> <span data-ttu-id="81cf9-131">Un'applicazione può usare la funzione [**DdeGetData**](/windows/desktop/api/Ddeml/nf-ddeml-ddegetdata) per copiare i dati.</span><span class="sxs-lookup"><span data-stu-id="81cf9-131">An application can use the [**DdeGetData**](/windows/desktop/api/Ddeml/nf-ddeml-ddegetdata) function to copy the data.</span></span>

<span data-ttu-id="81cf9-132">Poiché la maggior parte delle applicazioni client prevede che un'applicazione server esegua in modo sincrono un' **\_ esecuzione XTYP** , un server deve tentare di eseguire tutte le elaborazioni di **XTYP \_ Execute** Transaction dall'interno della funzione di callback DDE oppure restituendo il codice restituito del **\_ blocco CBR** .</span><span class="sxs-lookup"><span data-stu-id="81cf9-132">Because most client applications expect a server application to perform an **XTYP\_EXECUTE** transaction synchronously, a server should attempt to perform all processing of the **XTYP\_EXECUTE** transaction either from within the DDE callback function or by returning the **CBR\_BLOCK** return code.</span></span> <span data-ttu-id="81cf9-133">Se il parametro *hData* è un comando che indica al server di terminare, il server deve eseguire tale operazione dopo l'elaborazione di **XTYP \_ Execute** Transaction.</span><span class="sxs-lookup"><span data-stu-id="81cf9-133">If the *hdata* parameter is a command that instructs the server to terminate, the server should do so after processing the **XTYP\_EXECUTE** transaction.</span></span>

## <a name="requirements"></a><span data-ttu-id="81cf9-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="81cf9-134">Requirements</span></span>



| <span data-ttu-id="81cf9-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="81cf9-135">Requirement</span></span> | <span data-ttu-id="81cf9-136">Valore</span><span class="sxs-lookup"><span data-stu-id="81cf9-136">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81cf9-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="81cf9-137">Minimum supported client</span></span><br/> | <span data-ttu-id="81cf9-138">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="81cf9-138">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="81cf9-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="81cf9-139">Minimum supported server</span></span><br/> | <span data-ttu-id="81cf9-140">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="81cf9-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="81cf9-141">Intestazione</span><span class="sxs-lookup"><span data-stu-id="81cf9-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="81cf9-142"><dt>DDEML. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="81cf9-142"><dt>Ddeml.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81cf9-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="81cf9-143">See also</span></span>

<dl> <dt>

<span data-ttu-id="81cf9-144">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="81cf9-144">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="81cf9-145">**DdeClientTransaction**</span><span class="sxs-lookup"><span data-stu-id="81cf9-145">**DdeClientTransaction**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)
</dt> <dt>

[<span data-ttu-id="81cf9-146">**DdeGetData**</span><span class="sxs-lookup"><span data-stu-id="81cf9-146">**DdeGetData**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddegetdata)
</dt> <dt>

[<span data-ttu-id="81cf9-147">**DdeInitialize**</span><span class="sxs-lookup"><span data-stu-id="81cf9-147">**DdeInitialize**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

<span data-ttu-id="81cf9-148">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="81cf9-148">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="81cf9-149">Libreria di gestione Dynamic Data Exchange</span><span class="sxs-lookup"><span data-stu-id="81cf9-149">Dynamic Data Exchange Management Library</span></span>](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

