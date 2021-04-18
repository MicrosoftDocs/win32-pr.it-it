---
title: Transazione XTYP_XACT_COMPLETE (DDEML. h)
description: Una funzione di callback client di Dynamic Data Exchange (DDE), DdeCallback, riceve \_ la \_ transazione XTYP XACT complete quando una transazione asincrona, avviata da una chiamata alla funzione DdeClientTransaction, è stata completata.
ms.assetid: d34a6fab-0e3c-44fe-b25f-7011228fe261
keywords:
- Scambio di dati delle transazioni XTYP_XACT_COMPLETE
topic_type:
- apiref
api_name:
- XTYP_XACT_COMPLETE
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03a81869270a771836c4dd5c1a6b300f148ea13d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301280"
---
# <a name="xtyp_xact_complete-transaction"></a><span data-ttu-id="f7241-104">\_ \_ Transazione completa XTYP XACT</span><span class="sxs-lookup"><span data-stu-id="f7241-104">XTYP\_XACT\_COMPLETE transaction</span></span>

<span data-ttu-id="f7241-105">Una funzione di callback client di Dynamic Data Exchange (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), riceve la transazione **XTYP \_ XACT \_ complete** quando una transazione asincrona, avviata da una chiamata alla funzione [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) , è stata completata.</span><span class="sxs-lookup"><span data-stu-id="f7241-105">A Dynamic Data Exchange (DDE) client callback function, [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), receives the **XTYP\_XACT\_COMPLETE** transaction when an asynchronous transaction, initiated by a call to the [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) function, has completed.</span></span>


```C++
#define     XCLASS_NOTIFICATION      0x8000
#define     XTYP_XACT_COMPLETE      (0x0080 | XCLASS_NOTIFICATION  )
```



## <a name="parameters"></a><span data-ttu-id="f7241-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f7241-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7241-107">*uType*</span><span class="sxs-lookup"><span data-stu-id="f7241-107">*uType*</span></span> 
</dt> <dd>

<span data-ttu-id="f7241-108">Tipo di transazione.</span><span class="sxs-lookup"><span data-stu-id="f7241-108">The transaction type.</span></span>

</dd> <dt>

<span data-ttu-id="f7241-109">*uFmt*</span><span class="sxs-lookup"><span data-stu-id="f7241-109">*uFmt*</span></span> 
</dt> <dd>

<span data-ttu-id="f7241-110">Il formato dei dati associati alla transazione completata (se applicabile) o **null** se non è stato scambiato alcun dato durante la transazione.</span><span class="sxs-lookup"><span data-stu-id="f7241-110">The format of the data associated with the completed transaction (if applicable) or **NULL** if no data was exchanged during the transaction.</span></span>

</dd> <dt>

<span data-ttu-id="f7241-111">*hconv*</span><span class="sxs-lookup"><span data-stu-id="f7241-111">*hconv*</span></span> 
</dt> <dd>

<span data-ttu-id="f7241-112">Handle per la conversazione.</span><span class="sxs-lookup"><span data-stu-id="f7241-112">A handle to the conversation.</span></span>

</dd> <dt>

<span data-ttu-id="f7241-113">*hsz1*</span><span class="sxs-lookup"><span data-stu-id="f7241-113">*hsz1*</span></span> 
</dt> <dd>

<span data-ttu-id="f7241-114">Handle per il nome dell'argomento necessario per la transazione completata.</span><span class="sxs-lookup"><span data-stu-id="f7241-114">A handle to the topic name involved in the completed transaction.</span></span>

</dd> <dt>

<span data-ttu-id="f7241-115">*hsz2*</span><span class="sxs-lookup"><span data-stu-id="f7241-115">*hsz2*</span></span> 
</dt> <dd>

<span data-ttu-id="f7241-116">Handle per il nome dell'elemento richiesto nella transazione completata.</span><span class="sxs-lookup"><span data-stu-id="f7241-116">A handle to the item name involved in the completed transaction.</span></span>

</dd> <dt>

<span data-ttu-id="f7241-117">*hdata*</span><span class="sxs-lookup"><span data-stu-id="f7241-117">*hdata*</span></span> 
</dt> <dd>

<span data-ttu-id="f7241-118">Handle per i dati necessari nella transazione completata, se applicabile.</span><span class="sxs-lookup"><span data-stu-id="f7241-118">A handle to the data involved in the completed transaction, if applicable.</span></span> <span data-ttu-id="f7241-119">Se la transazione ha avuto esito positivo, ma non sono presenti dati, questo parametro è **true**.</span><span class="sxs-lookup"><span data-stu-id="f7241-119">If the transaction was successful but involved no data, this parameter is **TRUE**.</span></span> <span data-ttu-id="f7241-120">Questo parametro è **null** se la transazione ha avuto esito negativo.</span><span class="sxs-lookup"><span data-stu-id="f7241-120">This parameter is **NULL** if the transaction was unsuccessful.</span></span>

</dd> <dt>

<span data-ttu-id="f7241-121">*dwData1*</span><span class="sxs-lookup"><span data-stu-id="f7241-121">*dwData1*</span></span> 
</dt> <dd>

<span data-ttu-id="f7241-122">Identificatore della transazione completata.</span><span class="sxs-lookup"><span data-stu-id="f7241-122">The transaction identifier of the completed transaction.</span></span>

</dd> <dt>

<span data-ttu-id="f7241-123">*dwData2*</span><span class="sxs-lookup"><span data-stu-id="f7241-123">*dwData2*</span></span> 
</dt> <dd>

<span data-ttu-id="f7241-124">Eventuali flag di stato **DDE \_** applicabili nella parola bassa.</span><span class="sxs-lookup"><span data-stu-id="f7241-124">Any applicable **DDE\_** status flags in the low word.</span></span> <span data-ttu-id="f7241-125">Questo parametro fornisce supporto per le applicazioni che dipendono da bit **\_ APPSTATUS DDE** .</span><span class="sxs-lookup"><span data-stu-id="f7241-125">This parameter provides support for applications dependent on **DDE\_APPSTATUS** bits.</span></span> <span data-ttu-id="f7241-126">Si consiglia di non usare più questi bit per le applicazioni che potrebbero non essere supportate nelle versioni future del DDEML.</span><span class="sxs-lookup"><span data-stu-id="f7241-126">It is recommended that applications no longer use these bits   they may not be supported in future versions of the DDEML.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f7241-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="f7241-127">Remarks</span></span>

<span data-ttu-id="f7241-128">Un'applicazione non deve liberare l'handle di dati ottenuto durante la transazione.</span><span class="sxs-lookup"><span data-stu-id="f7241-128">An application must not free the data handle obtained during this transaction.</span></span> <span data-ttu-id="f7241-129">Un'applicazione, tuttavia, deve copiare i dati associati all'handle di dati se l'applicazione deve elaborare i dati dopo la restituzione della funzione di callback.</span><span class="sxs-lookup"><span data-stu-id="f7241-129">An application must, however, copy the data associated with the data handle if the application must process the data after the callback function returns.</span></span> <span data-ttu-id="f7241-130">Un'applicazione può usare la funzione [**DdeGetData**](/windows/desktop/api/Ddeml/nf-ddeml-ddegetdata) per copiare i dati.</span><span class="sxs-lookup"><span data-stu-id="f7241-130">An application can use the [**DdeGetData**](/windows/desktop/api/Ddeml/nf-ddeml-ddegetdata) function to copy the data.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7241-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f7241-131">Requirements</span></span>



| <span data-ttu-id="f7241-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="f7241-132">Requirement</span></span> | <span data-ttu-id="f7241-133">Valore</span><span class="sxs-lookup"><span data-stu-id="f7241-133">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7241-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f7241-134">Minimum supported client</span></span><br/> | <span data-ttu-id="f7241-135">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f7241-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="f7241-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f7241-136">Minimum supported server</span></span><br/> | <span data-ttu-id="f7241-137">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f7241-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="f7241-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f7241-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="f7241-139"><dt>DDEML. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f7241-139"><dt>Ddeml.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f7241-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f7241-140">See also</span></span>

<dl> <dt>

<span data-ttu-id="f7241-141">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="f7241-141">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f7241-142">**DdeClientTransaction**</span><span class="sxs-lookup"><span data-stu-id="f7241-142">**DdeClientTransaction**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)
</dt> <dt>

[<span data-ttu-id="f7241-143">**DdeGetData**</span><span class="sxs-lookup"><span data-stu-id="f7241-143">**DdeGetData**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddegetdata)
</dt> <dt>

<span data-ttu-id="f7241-144">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="f7241-144">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="f7241-145">Libreria di gestione Dynamic Data Exchange</span><span class="sxs-lookup"><span data-stu-id="f7241-145">Dynamic Data Exchange Management Library</span></span>](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

