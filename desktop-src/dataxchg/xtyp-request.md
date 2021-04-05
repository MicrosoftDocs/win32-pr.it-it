---
title: Transazione XTYP_REQUEST (DDEML. h)
description: Un client utilizza la \_ transazione di richiesta XTYP per richiedere dati da un server. Una funzione di callback del server Dynamic Data Exchange (DDE), DdeCallback, riceve questa transazione quando un client specifica \_ la richiesta XTYP nella funzione DdeClientTransaction.
ms.assetid: e776b995-6a64-4398-9e29-c151f3ef4c1d
keywords:
- Scambio di dati delle transazioni XTYP_REQUEST
topic_type:
- apiref
api_name:
- XTYP_REQUEST
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32e902c1525a8837f6ace6ef9bceb0607a608cda
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740327"
---
# <a name="xtyp_request-transaction"></a><span data-ttu-id="11689-105">\_Transazione di richiesta XTYP</span><span class="sxs-lookup"><span data-stu-id="11689-105">XTYP\_REQUEST transaction</span></span>

<span data-ttu-id="11689-106">Un client utilizza la transazione di **\_ richiesta XTYP** per richiedere dati da un server.</span><span class="sxs-lookup"><span data-stu-id="11689-106">A client uses the **XTYP\_REQUEST** transaction to request data from a server.</span></span> <span data-ttu-id="11689-107">Una funzione di callback del server Dynamic Data Exchange (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), riceve questa transazione quando un client specifica la **\_ richiesta XTYP** nella funzione [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) .</span><span class="sxs-lookup"><span data-stu-id="11689-107">A Dynamic Data Exchange (DDE) server callback function, [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), receives this transaction when a client specifies **XTYP\_REQUEST** in the [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) function.</span></span>


```C++
#define     XCLASS_DATA              0x2000
#define     XTYP_REQUEST            (0x00B0 | XCLASS_DATA          )
```



## <a name="parameters"></a><span data-ttu-id="11689-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="11689-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11689-109">*uType*</span><span class="sxs-lookup"><span data-stu-id="11689-109">*uType*</span></span> 
</dt> <dd>

<span data-ttu-id="11689-110">Tipo di transazione.</span><span class="sxs-lookup"><span data-stu-id="11689-110">The transaction type.</span></span>

</dd> <dt>

<span data-ttu-id="11689-111">*uFmt*</span><span class="sxs-lookup"><span data-stu-id="11689-111">*uFmt*</span></span> 
</dt> <dd>

<span data-ttu-id="11689-112">Formato in cui il server deve inviare i dati al client.</span><span class="sxs-lookup"><span data-stu-id="11689-112">The format in which the server should submit data to the client.</span></span>

</dd> <dt>

<span data-ttu-id="11689-113">*hconv*</span><span class="sxs-lookup"><span data-stu-id="11689-113">*hconv*</span></span> 
</dt> <dd>

<span data-ttu-id="11689-114">Handle per la conversazione.</span><span class="sxs-lookup"><span data-stu-id="11689-114">A handle to the conversation.</span></span>

</dd> <dt>

<span data-ttu-id="11689-115">*hsz1*</span><span class="sxs-lookup"><span data-stu-id="11689-115">*hsz1*</span></span> 
</dt> <dd>

<span data-ttu-id="11689-116">Handle per il nome dell'argomento.</span><span class="sxs-lookup"><span data-stu-id="11689-116">A handle to the topic name.</span></span>

</dd> <dt>

<span data-ttu-id="11689-117">*hsz2*</span><span class="sxs-lookup"><span data-stu-id="11689-117">*hsz2*</span></span> 
</dt> <dd>

<span data-ttu-id="11689-118">Handle per il nome dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="11689-118">A handle to the item name.</span></span>

</dd> <dt>

<span data-ttu-id="11689-119">*hdata*</span><span class="sxs-lookup"><span data-stu-id="11689-119">*hdata*</span></span> 
</dt> <dd>

<span data-ttu-id="11689-120">Non usato.</span><span class="sxs-lookup"><span data-stu-id="11689-120">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="11689-121">*dwData1*</span><span class="sxs-lookup"><span data-stu-id="11689-121">*dwData1*</span></span> 
</dt> <dd>

<span data-ttu-id="11689-122">Non usato.</span><span class="sxs-lookup"><span data-stu-id="11689-122">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="11689-123">*dwData2*</span><span class="sxs-lookup"><span data-stu-id="11689-123">*dwData2*</span></span> 
</dt> <dd>

<span data-ttu-id="11689-124">Non usato.</span><span class="sxs-lookup"><span data-stu-id="11689-124">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11689-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="11689-125">Return value</span></span>

<span data-ttu-id="11689-126">Il server deve chiamare la funzione [**DdeCreateDataHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle) per creare un handle di dati che identifichi i dati e quindi restituire l'handle.</span><span class="sxs-lookup"><span data-stu-id="11689-126">The server should call the [**DdeCreateDataHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle) function to create a data handle that identifies the data and then return the handle.</span></span> <span data-ttu-id="11689-127">Il server deve restituire **null** se non è in grado di completare la transazione.</span><span class="sxs-lookup"><span data-stu-id="11689-127">The server should return **NULL** if it is unable to complete the transaction.</span></span> <span data-ttu-id="11689-128">Se il server restituisce **null**, il client riceverà un \_ flag FNOTPROCESSED DDE.</span><span class="sxs-lookup"><span data-stu-id="11689-128">If the server returns **NULL**, the client will receive a DDE\_FNOTPROCESSED flag.</span></span>

## <a name="remarks"></a><span data-ttu-id="11689-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="11689-129">Remarks</span></span>

<span data-ttu-id="11689-130">Questa transazione viene filtrata se l'applicazione server ha specificato il flag **CBF \_ Fail \_** requests nella funzione [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .</span><span class="sxs-lookup"><span data-stu-id="11689-130">This transaction is filtered if the server application specified the **CBF\_FAIL\_REQUESTS** flag in the [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) function.</span></span>

<span data-ttu-id="11689-131">Se la risposta a questa transazione richiede una lunga elaborazione, il server può restituire il \_ codice del blocco CBR per sospendere le transazioni future sulla conversazione corrente, quindi elaborare la transazione in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="11689-131">If responding to this transaction requires lengthy processing, the server can return the CBR\_BLOCK return code to suspend future transactions on the current conversation and then process the transaction asynchronously.</span></span> <span data-ttu-id="11689-132">Al termine del server e se i dati sono pronti per il passaggio al client, il server può chiamare la funzione [**DdeEnableCallback**](/windows/desktop/api/Ddeml/nf-ddeml-ddeenablecallback) per riprendere la conversazione.</span><span class="sxs-lookup"><span data-stu-id="11689-132">When the server has finished and the data is ready to pass to the client, the server can call the [**DdeEnableCallback**](/windows/desktop/api/Ddeml/nf-ddeml-ddeenablecallback) function to resume the conversation.</span></span>

## <a name="requirements"></a><span data-ttu-id="11689-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="11689-133">Requirements</span></span>



| <span data-ttu-id="11689-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="11689-134">Requirement</span></span> | <span data-ttu-id="11689-135">Valore</span><span class="sxs-lookup"><span data-stu-id="11689-135">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11689-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="11689-136">Minimum supported client</span></span><br/> | <span data-ttu-id="11689-137">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="11689-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="11689-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="11689-138">Minimum supported server</span></span><br/> | <span data-ttu-id="11689-139">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="11689-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="11689-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="11689-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="11689-141"><dt>DDEML. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="11689-141"><dt>Ddeml.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11689-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="11689-142">See also</span></span>

<dl> <dt>

<span data-ttu-id="11689-143">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="11689-143">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="11689-144">**DdeClientTransaction**</span><span class="sxs-lookup"><span data-stu-id="11689-144">**DdeClientTransaction**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)
</dt> <dt>

[<span data-ttu-id="11689-145">**DdeCreateDataHandle**</span><span class="sxs-lookup"><span data-stu-id="11689-145">**DdeCreateDataHandle**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle)
</dt> <dt>

[<span data-ttu-id="11689-146">**DdeEnableCallback**</span><span class="sxs-lookup"><span data-stu-id="11689-146">**DdeEnableCallback**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeenablecallback)
</dt> <dt>

[<span data-ttu-id="11689-147">**DdeInitialize**</span><span class="sxs-lookup"><span data-stu-id="11689-147">**DdeInitialize**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

<span data-ttu-id="11689-148">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="11689-148">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="11689-149">Libreria di gestione Dynamic Data Exchange</span><span class="sxs-lookup"><span data-stu-id="11689-149">Dynamic Data Exchange Management Library</span></span>](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

