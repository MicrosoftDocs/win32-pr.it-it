---
title: Transazione XTYP_ADVSTOP (DDEML. h)
description: Un client usa la \_ transazione XTYP ADVSTOP per terminare un ciclo di notifica con un server. Una funzione di callback del server Dynamic Data Exchange (DDE), DdeCallback, riceve questa transazione quando un client specifica XTYP \_ ADVSTOP nella funzione DdeClientTransaction.
ms.assetid: 67dfa463-6a44-43a5-93be-a39c19c87c1c
keywords:
- Scambio di dati delle transazioni XTYP_ADVSTOP
topic_type:
- apiref
api_name:
- XTYP_ADVSTOP
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61292683377cd6c7243c3e41c5dbd9332a671163
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301772"
---
# <a name="xtyp_advstop-transaction"></a><span data-ttu-id="3aa8a-105">\_Transazione ADVSTOP XTYP</span><span class="sxs-lookup"><span data-stu-id="3aa8a-105">XTYP\_ADVSTOP transaction</span></span>

<span data-ttu-id="3aa8a-106">Un client usa la transazione **XTYP \_ ADVSTOP** per terminare un ciclo di notifica con un server.</span><span class="sxs-lookup"><span data-stu-id="3aa8a-106">A client uses the **XTYP\_ADVSTOP** transaction to end an advise loop with a server.</span></span> <span data-ttu-id="3aa8a-107">Una funzione di callback del server Dynamic Data Exchange (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), riceve questa transazione quando un client specifica **XTYP \_ ADVSTOP** nella funzione [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) .</span><span class="sxs-lookup"><span data-stu-id="3aa8a-107">A Dynamic Data Exchange (DDE) server callback function, [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), receives this transaction when a client specifies **XTYP\_ADVSTOP** in the [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) function.</span></span>


```C++
#define     XCLASS_NOTIFICATION      0x8000
#define     XTYP_ADVSTOP            (0x0040 | XCLASS_NOTIFICATION)
```



## <a name="parameters"></a><span data-ttu-id="3aa8a-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="3aa8a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3aa8a-109">*uType*</span><span class="sxs-lookup"><span data-stu-id="3aa8a-109">*uType*</span></span> 
</dt> <dd>

<span data-ttu-id="3aa8a-110">Tipo di transazione.</span><span class="sxs-lookup"><span data-stu-id="3aa8a-110">The transaction type.</span></span>

</dd> <dt>

<span data-ttu-id="3aa8a-111">*uFmt*</span><span class="sxs-lookup"><span data-stu-id="3aa8a-111">*uFmt*</span></span> 
</dt> <dd>

<span data-ttu-id="3aa8a-112">Formato dati associato al ciclo di notifica terminato.</span><span class="sxs-lookup"><span data-stu-id="3aa8a-112">The data format associated with the advise loop being ended.</span></span>

</dd> <dt>

<span data-ttu-id="3aa8a-113">*hconv*</span><span class="sxs-lookup"><span data-stu-id="3aa8a-113">*hconv*</span></span> 
</dt> <dd>

<span data-ttu-id="3aa8a-114">Handle per la conversazione.</span><span class="sxs-lookup"><span data-stu-id="3aa8a-114">A handle to the conversation.</span></span>

</dd> <dt>

<span data-ttu-id="3aa8a-115">*hsz1*</span><span class="sxs-lookup"><span data-stu-id="3aa8a-115">*hsz1*</span></span> 
</dt> <dd>

<span data-ttu-id="3aa8a-116">Handle per il nome dell'argomento.</span><span class="sxs-lookup"><span data-stu-id="3aa8a-116">A handle to the topic name.</span></span>

</dd> <dt>

<span data-ttu-id="3aa8a-117">*hsz2*</span><span class="sxs-lookup"><span data-stu-id="3aa8a-117">*hsz2*</span></span> 
</dt> <dd>

<span data-ttu-id="3aa8a-118">Handle per il nome dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="3aa8a-118">A handle to the item name.</span></span>

</dd> <dt>

<span data-ttu-id="3aa8a-119">*hdata*</span><span class="sxs-lookup"><span data-stu-id="3aa8a-119">*hdata*</span></span> 
</dt> <dd>

<span data-ttu-id="3aa8a-120">Non usato.</span><span class="sxs-lookup"><span data-stu-id="3aa8a-120">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="3aa8a-121">*dwData1*</span><span class="sxs-lookup"><span data-stu-id="3aa8a-121">*dwData1*</span></span> 
</dt> <dd>

<span data-ttu-id="3aa8a-122">Non usato.</span><span class="sxs-lookup"><span data-stu-id="3aa8a-122">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="3aa8a-123">*dwData2*</span><span class="sxs-lookup"><span data-stu-id="3aa8a-123">*dwData2*</span></span> 
</dt> <dd>

<span data-ttu-id="3aa8a-124">Non usato.</span><span class="sxs-lookup"><span data-stu-id="3aa8a-124">Not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3aa8a-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="3aa8a-125">Remarks</span></span>

<span data-ttu-id="3aa8a-126">Questa transazione viene filtrata se l'applicazione server ha specificato il flag **CBF \_ Fail \_ advises** nella funzione [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .</span><span class="sxs-lookup"><span data-stu-id="3aa8a-126">This transaction is filtered if the server application specified the **CBF\_FAIL\_ADVISES** flag in the [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="3aa8a-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3aa8a-127">Requirements</span></span>



| <span data-ttu-id="3aa8a-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="3aa8a-128">Requirement</span></span> | <span data-ttu-id="3aa8a-129">Valore</span><span class="sxs-lookup"><span data-stu-id="3aa8a-129">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3aa8a-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3aa8a-130">Minimum supported client</span></span><br/> | <span data-ttu-id="3aa8a-131">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3aa8a-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="3aa8a-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3aa8a-132">Minimum supported server</span></span><br/> | <span data-ttu-id="3aa8a-133">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3aa8a-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="3aa8a-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3aa8a-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="3aa8a-135"><dt>DDEML. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3aa8a-135"><dt>Ddeml.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3aa8a-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3aa8a-136">See also</span></span>

<dl> <dt>

<span data-ttu-id="3aa8a-137">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="3aa8a-137">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="3aa8a-138">**DdeClientTransaction**</span><span class="sxs-lookup"><span data-stu-id="3aa8a-138">**DdeClientTransaction**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)
</dt> <dt>

[<span data-ttu-id="3aa8a-139">**DdeInitialize**</span><span class="sxs-lookup"><span data-stu-id="3aa8a-139">**DdeInitialize**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

[<span data-ttu-id="3aa8a-140">**DdePostAdvise**</span><span class="sxs-lookup"><span data-stu-id="3aa8a-140">**DdePostAdvise**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise)
</dt> <dt>

<span data-ttu-id="3aa8a-141">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="3aa8a-141">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="3aa8a-142">Libreria di gestione Dynamic Data Exchange</span><span class="sxs-lookup"><span data-stu-id="3aa8a-142">Dynamic Data Exchange Management Library</span></span>](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

