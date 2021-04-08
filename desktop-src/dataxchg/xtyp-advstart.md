---
title: Transazione XTYP_ADVSTART (DDEML. h)
description: Un client utilizza la \_ transazione XTYP ADVSTART per stabilire un ciclo di notifica con un server.
ms.assetid: 8911e722-5656-4ca6-8b0a-6bdf8281611a
keywords:
- Scambio di dati delle transazioni XTYP_ADVSTART
topic_type:
- apiref
api_name:
- XTYP_ADVSTART
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 852351ad902a0552ee012d6c1e5c4d61501e6e58
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741858"
---
# <a name="xtyp_advstart-transaction"></a><span data-ttu-id="d8ee8-104">\_Transazione ADVSTART XTYP</span><span class="sxs-lookup"><span data-stu-id="d8ee8-104">XTYP\_ADVSTART transaction</span></span>

<span data-ttu-id="d8ee8-105">Un client utilizza la transazione **XTYP \_ ADVSTART** per stabilire un ciclo di notifica con un server.</span><span class="sxs-lookup"><span data-stu-id="d8ee8-105">A client uses the **XTYP\_ADVSTART** transaction to establish an advise loop with a server.</span></span> <span data-ttu-id="d8ee8-106">Una funzione di callback del server Dynamic Data Exchange (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), riceve questa transazione quando un client specifica **XTYP \_ ADVSTART** come parametro *wType* della funzione [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) .</span><span class="sxs-lookup"><span data-stu-id="d8ee8-106">A Dynamic Data Exchange (DDE) server callback function, [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), receives this transaction when a client specifies **XTYP\_ADVSTART** as the *wType* parameter of the [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) function.</span></span>


```C++
#define     XCLASS_BOOL              0x1000
#define     XTYP_ADVSTART           (0x0030 | XCLASS_BOOL          )
```



## <a name="parameters"></a><span data-ttu-id="d8ee8-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="d8ee8-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8ee8-108">*uType*</span><span class="sxs-lookup"><span data-stu-id="d8ee8-108">*uType*</span></span> 
</dt> <dd>

<span data-ttu-id="d8ee8-109">Tipo di transazione.</span><span class="sxs-lookup"><span data-stu-id="d8ee8-109">The transaction type.</span></span>

</dd> <dt>

<span data-ttu-id="d8ee8-110">*uFmt*</span><span class="sxs-lookup"><span data-stu-id="d8ee8-110">*uFmt*</span></span> 
</dt> <dd>

<span data-ttu-id="d8ee8-111">Formato dati richiesto dal client.</span><span class="sxs-lookup"><span data-stu-id="d8ee8-111">The data format requested by the client.</span></span>

</dd> <dt>

<span data-ttu-id="d8ee8-112">*hconv*</span><span class="sxs-lookup"><span data-stu-id="d8ee8-112">*hconv*</span></span> 
</dt> <dd>

<span data-ttu-id="d8ee8-113">Handle per la conversazione.</span><span class="sxs-lookup"><span data-stu-id="d8ee8-113">A handle to the conversation.</span></span>

</dd> <dt>

<span data-ttu-id="d8ee8-114">*hsz1*</span><span class="sxs-lookup"><span data-stu-id="d8ee8-114">*hsz1*</span></span> 
</dt> <dd>

<span data-ttu-id="d8ee8-115">Handle per il nome dell'argomento.</span><span class="sxs-lookup"><span data-stu-id="d8ee8-115">A handle to the topic name.</span></span>

</dd> <dt>

<span data-ttu-id="d8ee8-116">*hsz2*</span><span class="sxs-lookup"><span data-stu-id="d8ee8-116">*hsz2*</span></span> 
</dt> <dd>

<span data-ttu-id="d8ee8-117">Handle per il nome dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="d8ee8-117">A handle to the item name.</span></span>

</dd> <dt>

<span data-ttu-id="d8ee8-118">*hdata*</span><span class="sxs-lookup"><span data-stu-id="d8ee8-118">*hdata*</span></span> 
</dt> <dd>

<span data-ttu-id="d8ee8-119">Non usato.</span><span class="sxs-lookup"><span data-stu-id="d8ee8-119">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="d8ee8-120">*dwData1*</span><span class="sxs-lookup"><span data-stu-id="d8ee8-120">*dwData1*</span></span> 
</dt> <dd>

<span data-ttu-id="d8ee8-121">Non usato.</span><span class="sxs-lookup"><span data-stu-id="d8ee8-121">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="d8ee8-122">*dwData2*</span><span class="sxs-lookup"><span data-stu-id="d8ee8-122">*dwData2*</span></span> 
</dt> <dd>

<span data-ttu-id="d8ee8-123">Non usato.</span><span class="sxs-lookup"><span data-stu-id="d8ee8-123">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8ee8-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d8ee8-124">Return value</span></span>

<span data-ttu-id="d8ee8-125">Una funzione di callback del server deve restituire **true** per consentire un ciclo di notifica sul nome dell'argomento e sulla coppia di nomi di elemento specificati oppure su **false** per negare il ciclo di notifica.</span><span class="sxs-lookup"><span data-stu-id="d8ee8-125">A server callback function should return **TRUE** to allow an advise loop on the specified topic name and item name pair, or **FALSE** to deny the advise loop.</span></span> <span data-ttu-id="d8ee8-126">Se la funzione di callback restituisce **true**, tutte le chiamate successive alla funzione [**DdePostAdvise**](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise) da parte del server nella stessa coppia nome argomento e nome elemento fanno sì che il sistema invii le transazioni [**\_ ADVREQ XTYP**](xtyp-advreq.md) al server.</span><span class="sxs-lookup"><span data-stu-id="d8ee8-126">If the callback function returns **TRUE**, any subsequent calls to the [**DdePostAdvise**](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise) function by the server on the same topic name and item name pair causes the system to send [**XTYP\_ADVREQ**](xtyp-advreq.md) transactions to the server.</span></span>

## <a name="remarks"></a><span data-ttu-id="d8ee8-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="d8ee8-127">Remarks</span></span>

<span data-ttu-id="d8ee8-128">Se un client richiede un ciclo di notifica per un nome di argomento, un nome di elemento e un formato dati per un ciclo di notifica già stabilito, la libreria di gestione Dynamic Data Exchange (DDEML) non crea un ciclo di notifica duplicato, ma modifica i flag del ciclo di notifica (**XTYPF \_ ACKREQ** e **XTYPF \_ NoData**) in modo che corrispondano alla richiesta più recente.</span><span class="sxs-lookup"><span data-stu-id="d8ee8-128">If a client requests an advise loop on a topic name, item name, and data format for an advise loop that is already established, the Dynamic Data Exchange Management Library (DDEML) does not create a duplicate advise loop but instead alters the advise loop flags (**XTYPF\_ACKREQ** and **XTYPF\_NODATA**) to match the latest request.</span></span>

<span data-ttu-id="d8ee8-129">Questa transazione viene filtrata se l'applicazione server ha specificato il flag **CBF \_ Fail \_ advises** nella funzione [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .</span><span class="sxs-lookup"><span data-stu-id="d8ee8-129">This transaction is filtered if the server application specified the **CBF\_FAIL\_ADVISES** flag in the [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8ee8-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d8ee8-130">Requirements</span></span>



| <span data-ttu-id="d8ee8-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="d8ee8-131">Requirement</span></span> | <span data-ttu-id="d8ee8-132">Valore</span><span class="sxs-lookup"><span data-stu-id="d8ee8-132">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8ee8-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d8ee8-133">Minimum supported client</span></span><br/> | <span data-ttu-id="d8ee8-134">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d8ee8-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="d8ee8-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d8ee8-135">Minimum supported server</span></span><br/> | <span data-ttu-id="d8ee8-136">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d8ee8-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="d8ee8-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d8ee8-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="d8ee8-138"><dt>DDEML. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d8ee8-138"><dt>Ddeml.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8ee8-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d8ee8-139">See also</span></span>

<dl> <dt>

<span data-ttu-id="d8ee8-140">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="d8ee8-140">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d8ee8-141">**DdeClientTransaction**</span><span class="sxs-lookup"><span data-stu-id="d8ee8-141">**DdeClientTransaction**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)
</dt> <dt>

[<span data-ttu-id="d8ee8-142">**DdeInitialize**</span><span class="sxs-lookup"><span data-stu-id="d8ee8-142">**DdeInitialize**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

[<span data-ttu-id="d8ee8-143">**DdePostAdvise**</span><span class="sxs-lookup"><span data-stu-id="d8ee8-143">**DdePostAdvise**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise)
</dt> <dt>

<span data-ttu-id="d8ee8-144">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="d8ee8-144">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="d8ee8-145">Libreria di gestione Dynamic Data Exchange</span><span class="sxs-lookup"><span data-stu-id="d8ee8-145">Dynamic Data Exchange Management Library</span></span>](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

