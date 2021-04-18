---
title: Transazione XTYP_ADVDATA (DDEML. h)
description: Informa il client che il valore dell'elemento di dati è stato modificato. La funzione di callback del client Dynamic Data Exchange (DDE), DdeCallback, riceve questa transazione dopo aver stabilito un ciclo di notifica con un server.
ms.assetid: c6e61785-b98c-4ffa-9d23-339e1c66cb4d
keywords:
- Scambio di dati delle transazioni XTYP_ADVDATA
topic_type:
- apiref
api_name:
- XTYP_ADVDATA
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8359e34388d185200b5f30c4554e138cc1f6b94a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301093"
---
# <a name="xtyp_advdata-transaction"></a><span data-ttu-id="f3ef1-105">\_Transazione ADVDATA XTYP</span><span class="sxs-lookup"><span data-stu-id="f3ef1-105">XTYP\_ADVDATA transaction</span></span>

<span data-ttu-id="f3ef1-106">Informa il client che il valore dell'elemento di dati è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="f3ef1-106">Informs the client that the value of the data item has changed.</span></span> <span data-ttu-id="f3ef1-107">La funzione di callback del client Dynamic Data Exchange (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), riceve questa transazione dopo aver stabilito un ciclo di notifica con un server.</span><span class="sxs-lookup"><span data-stu-id="f3ef1-107">The Dynamic Data Exchange (DDE) client callback function, [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), receives this transaction after establishing an advise loop with a server.</span></span>


```C++
#define     XCLASS_FLAGS             0x4000
#define     XTYP_ADVDATA            (0x0010 | XCLASS_FLAGS         )
```



## <a name="parameters"></a><span data-ttu-id="f3ef1-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="f3ef1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3ef1-109">*uType*</span><span class="sxs-lookup"><span data-stu-id="f3ef1-109">*uType*</span></span> 
</dt> <dd>

<span data-ttu-id="f3ef1-110">Tipo di transazione.</span><span class="sxs-lookup"><span data-stu-id="f3ef1-110">The transaction type.</span></span>

</dd> <dt>

<span data-ttu-id="f3ef1-111">*uFmt*</span><span class="sxs-lookup"><span data-stu-id="f3ef1-111">*uFmt*</span></span> 
</dt> <dd>

<span data-ttu-id="f3ef1-112">Formato Atom dei dati inviati dal server.</span><span class="sxs-lookup"><span data-stu-id="f3ef1-112">The format atom of the data sent from the server.</span></span>

</dd> <dt>

<span data-ttu-id="f3ef1-113">*hconv*</span><span class="sxs-lookup"><span data-stu-id="f3ef1-113">*hconv*</span></span> 
</dt> <dd>

<span data-ttu-id="f3ef1-114">Handle per la conversazione.</span><span class="sxs-lookup"><span data-stu-id="f3ef1-114">A handle to the conversation.</span></span>

</dd> <dt>

<span data-ttu-id="f3ef1-115">*hsz1*</span><span class="sxs-lookup"><span data-stu-id="f3ef1-115">*hsz1*</span></span> 
</dt> <dd>

<span data-ttu-id="f3ef1-116">Handle per il nome dell'argomento.</span><span class="sxs-lookup"><span data-stu-id="f3ef1-116">A handle to the topic name.</span></span>

</dd> <dt>

<span data-ttu-id="f3ef1-117">*hsz2*</span><span class="sxs-lookup"><span data-stu-id="f3ef1-117">*hsz2*</span></span> 
</dt> <dd>

<span data-ttu-id="f3ef1-118">Handle per il nome dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="f3ef1-118">A handle to the item name.</span></span>

</dd> <dt>

<span data-ttu-id="f3ef1-119">*hdata*</span><span class="sxs-lookup"><span data-stu-id="f3ef1-119">*hdata*</span></span> 
</dt> <dd>

<span data-ttu-id="f3ef1-120">Handle per i dati associati alla coppia nome argomento e nome elemento.</span><span class="sxs-lookup"><span data-stu-id="f3ef1-120">A handle to the data associated with the topic name and item name pair.</span></span> <span data-ttu-id="f3ef1-121">Questo parametro è **null** se il client ha specificato il flag **\_ NoData XTYPF** quando ha richiesto il ciclo di notifica.</span><span class="sxs-lookup"><span data-stu-id="f3ef1-121">This parameter is **NULL** if the client specified the **XTYPF\_NODATA** flag when it requested the advise loop.</span></span>

</dd> <dt>

<span data-ttu-id="f3ef1-122">*dwData1*</span><span class="sxs-lookup"><span data-stu-id="f3ef1-122">*dwData1*</span></span> 
</dt> <dd>

<span data-ttu-id="f3ef1-123">Non usato.</span><span class="sxs-lookup"><span data-stu-id="f3ef1-123">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="f3ef1-124">*dwData2*</span><span class="sxs-lookup"><span data-stu-id="f3ef1-124">*dwData2*</span></span> 
</dt> <dd>

<span data-ttu-id="f3ef1-125">Non usato.</span><span class="sxs-lookup"><span data-stu-id="f3ef1-125">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3ef1-126">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f3ef1-126">Return value</span></span>

<span data-ttu-id="f3ef1-127">Una funzione di callback DDE deve **restituire \_ fack DDE** se elabora questa transazione, **\_ FBUSY DDE** se è troppo occupato per elaborare la transazione o **\_ FNOTPROCESSED DDE** se rifiuta questa transazione.</span><span class="sxs-lookup"><span data-stu-id="f3ef1-127">A DDE callback function should return **DDE\_FACK** if it processes this transaction, **DDE\_FBUSY** if it is too busy to process this transaction, or **DDE\_FNOTPROCESSED** if it rejects this transaction.</span></span>

## <a name="remarks"></a><span data-ttu-id="f3ef1-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="f3ef1-128">Remarks</span></span>

<span data-ttu-id="f3ef1-129">Un'applicazione non deve liberare l'handle di dati ottenuto durante la transazione.</span><span class="sxs-lookup"><span data-stu-id="f3ef1-129">An application must not free the data handle obtained during this transaction.</span></span> <span data-ttu-id="f3ef1-130">Un'applicazione, tuttavia, deve copiare i dati associati all'handle di dati se l'applicazione deve elaborare i dati dopo la restituzione della funzione di callback.</span><span class="sxs-lookup"><span data-stu-id="f3ef1-130">An application must, however, copy the data associated with the data handle if the application must process the data after the callback function returns.</span></span> <span data-ttu-id="f3ef1-131">Un'applicazione può usare la funzione [**DdeGetData**](/windows/desktop/api/Ddeml/nf-ddeml-ddegetdata) per copiare i dati.</span><span class="sxs-lookup"><span data-stu-id="f3ef1-131">An application can use the [**DdeGetData**](/windows/desktop/api/Ddeml/nf-ddeml-ddegetdata) function to copy the data.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3ef1-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f3ef1-132">Requirements</span></span>



| <span data-ttu-id="f3ef1-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="f3ef1-133">Requirement</span></span> | <span data-ttu-id="f3ef1-134">Valore</span><span class="sxs-lookup"><span data-stu-id="f3ef1-134">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3ef1-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f3ef1-135">Minimum supported client</span></span><br/> | <span data-ttu-id="f3ef1-136">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f3ef1-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="f3ef1-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f3ef1-137">Minimum supported server</span></span><br/> | <span data-ttu-id="f3ef1-138">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f3ef1-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="f3ef1-139">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f3ef1-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="f3ef1-140"><dt>DDEML. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f3ef1-140"><dt>Ddeml.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3ef1-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f3ef1-141">See also</span></span>

<dl> <dt>

<span data-ttu-id="f3ef1-142">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="f3ef1-142">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f3ef1-143">**DdeClientTransaction**</span><span class="sxs-lookup"><span data-stu-id="f3ef1-143">**DdeClientTransaction**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)
</dt> <dt>

[<span data-ttu-id="f3ef1-144">**DdeGetData**</span><span class="sxs-lookup"><span data-stu-id="f3ef1-144">**DdeGetData**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddegetdata)
</dt> <dt>

[<span data-ttu-id="f3ef1-145">**DdePostAdvise**</span><span class="sxs-lookup"><span data-stu-id="f3ef1-145">**DdePostAdvise**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise)
</dt> <dt>

<span data-ttu-id="f3ef1-146">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="f3ef1-146">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="f3ef1-147">Libreria di gestione Dynamic Data Exchange</span><span class="sxs-lookup"><span data-stu-id="f3ef1-147">Dynamic Data Exchange Management Library</span></span>](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

