---
title: Transazione XTYP_ADVREQ (DDEML. h)
description: La \_ transazione XTYP ADVREQ informa il server che una transazione advise è in attesa nella coppia nome argomento e nome elemento specificato e che i dati corrispondenti alla coppia nome argomento e nome elemento sono stati modificati.
ms.assetid: 9bd43e61-cbd6-4d53-bab3-90e85819b16b
keywords:
- Scambio di dati delle transazioni XTYP_ADVREQ
topic_type:
- apiref
api_name:
- XTYP_ADVREQ
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2884e838268342ab10c556c6ae3cfc8349ed5d2c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400686"
---
# <a name="xtyp_advreq-transaction"></a><span data-ttu-id="c2403-104">\_Transazione ADVREQ XTYP</span><span class="sxs-lookup"><span data-stu-id="c2403-104">XTYP\_ADVREQ transaction</span></span>

<span data-ttu-id="c2403-105">La transazione **XTYP \_ ADVREQ** informa il server che una transazione advise è in attesa nella coppia nome argomento e nome elemento specificato e che i dati corrispondenti alla coppia nome argomento e nome elemento sono stati modificati.</span><span class="sxs-lookup"><span data-stu-id="c2403-105">The **XTYP\_ADVREQ** transaction informs the server that an advise transaction is outstanding on the specified topic name and item name pair and that data corresponding to the topic name and item name pair has changed.</span></span> <span data-ttu-id="c2403-106">Il sistema invia questa transazione alla funzione di callback Dynamic Data Exchange (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), dopo che il server chiama la funzione [**DdePostAdvise**](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise) .</span><span class="sxs-lookup"><span data-stu-id="c2403-106">The system sends this transaction to the Dynamic Data Exchange (DDE) callback function, [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), after the server calls the [**DdePostAdvise**](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise) function.</span></span>


```C++
#define     XCLASS_DATA              0x2000
#define     XTYPF_NOBLOCK            0x0002
#define     XTYP_ADVREQ             (0x0020 | XCLASS_DATA | XTYPF_NOBLOCK )
```



## <a name="parameters"></a><span data-ttu-id="c2403-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="c2403-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2403-108">*uType*</span><span class="sxs-lookup"><span data-stu-id="c2403-108">*uType*</span></span> 
</dt> <dd>

<span data-ttu-id="c2403-109">Tipo di transazione.</span><span class="sxs-lookup"><span data-stu-id="c2403-109">The transaction type.</span></span>

</dd> <dt>

<span data-ttu-id="c2403-110">*uFmt*</span><span class="sxs-lookup"><span data-stu-id="c2403-110">*uFmt*</span></span> 
</dt> <dd>

<span data-ttu-id="c2403-111">Formato in cui i dati devono essere inviati al client.</span><span class="sxs-lookup"><span data-stu-id="c2403-111">The format in which the data should be submitted to the client.</span></span>

</dd> <dt>

<span data-ttu-id="c2403-112">*hconv*</span><span class="sxs-lookup"><span data-stu-id="c2403-112">*hconv*</span></span> 
</dt> <dd>

<span data-ttu-id="c2403-113">Handle per la conversazione.</span><span class="sxs-lookup"><span data-stu-id="c2403-113">A handle to the conversation.</span></span>

</dd> <dt>

<span data-ttu-id="c2403-114">*hsz1*</span><span class="sxs-lookup"><span data-stu-id="c2403-114">*hsz1*</span></span> 
</dt> <dd>

<span data-ttu-id="c2403-115">Handle per il nome dell'argomento.</span><span class="sxs-lookup"><span data-stu-id="c2403-115">A handle to the topic name.</span></span>

</dd> <dt>

<span data-ttu-id="c2403-116">*hsz2*</span><span class="sxs-lookup"><span data-stu-id="c2403-116">*hsz2*</span></span> 
</dt> <dd>

<span data-ttu-id="c2403-117">Handle per il nome dell'elemento che è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="c2403-117">A handle to the item name that has changed.</span></span>

</dd> <dt>

<span data-ttu-id="c2403-118">*hdata*</span><span class="sxs-lookup"><span data-stu-id="c2403-118">*hdata*</span></span> 
</dt> <dd>

<span data-ttu-id="c2403-119">Non usato.</span><span class="sxs-lookup"><span data-stu-id="c2403-119">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="c2403-120">*dwData1*</span><span class="sxs-lookup"><span data-stu-id="c2403-120">*dwData1*</span></span> 
</dt> <dd>

<span data-ttu-id="c2403-121">Conteggio, nella parola di basso livello, delle transazioni **\_ ADVREQ XTYP** che rimangono per essere elaborate nello stesso argomento, elemento e nome di formato impostati nel contesto della chiamata corrente alla funzione [**DdePostAdvise**](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise) .</span><span class="sxs-lookup"><span data-stu-id="c2403-121">The count, in the low-order word, of **XTYP\_ADVREQ** transactions that remain to be processed on the same topic, item, and format name set within the context of the current call to the [**DdePostAdvise**](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise) function.</span></span> <span data-ttu-id="c2403-122">Il conteggio è zero se la transazione **XTYP \_ ADVREQ** corrente è l'ultima.</span><span class="sxs-lookup"><span data-stu-id="c2403-122">The count is zero if the current **XTYP\_ADVREQ** transaction is the last one.</span></span> <span data-ttu-id="c2403-123">Un server può utilizzare questo conteggio per determinare se creare un handle di dati **HDATA \_ APPOWNED** per i dati di notifica.</span><span class="sxs-lookup"><span data-stu-id="c2403-123">A server can use this count to determine whether to create an **HDATA\_APPOWNED** data handle to the advise data.</span></span>

<span data-ttu-id="c2403-124">La parola meno ordinata è impostata su **CADV \_ LATEACK** se il DDEML ha emesso la transazione **XTYP \_ ADVREQ** a causa di un messaggio di ACK DDE in arrivo tardivo \_ da un client che è più veloce dal server.</span><span class="sxs-lookup"><span data-stu-id="c2403-124">The low-order word is set to **CADV\_LATEACK** if the DDEML issued the **XTYP\_ADVREQ** transaction because of a late-arriving DDE\_ACK message from a client being outrun by the server.</span></span>

<span data-ttu-id="c2403-125">La parola più ordinata non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="c2403-125">The high-order word is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c2403-126">*dwData2*</span><span class="sxs-lookup"><span data-stu-id="c2403-126">*dwData2*</span></span> 
</dt> <dd>

<span data-ttu-id="c2403-127">Non usato.</span><span class="sxs-lookup"><span data-stu-id="c2403-127">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2403-128">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c2403-128">Return value</span></span>

<span data-ttu-id="c2403-129">Il server deve prima chiamare la funzione [**DdeCreateDataHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle) per creare un handle di dati che identifichi i dati modificati e quindi restituire l'handle.</span><span class="sxs-lookup"><span data-stu-id="c2403-129">The server should first call the [**DdeCreateDataHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle) function to create a data handle that identifies the changed data and then return the handle.</span></span> <span data-ttu-id="c2403-130">Il server deve restituire **null** se non è in grado di completare la transazione.</span><span class="sxs-lookup"><span data-stu-id="c2403-130">The server should return **NULL** if it is unable to complete the transaction.</span></span>

## <a name="remarks"></a><span data-ttu-id="c2403-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="c2403-131">Remarks</span></span>

<span data-ttu-id="c2403-132">Un server non è in grado di bloccare questo tipo di transazione. il codice restituito del **\_ blocco CBR** viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="c2403-132">A server cannot block this transaction type; the **CBR\_BLOCK** return code is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2403-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c2403-133">Requirements</span></span>



| <span data-ttu-id="c2403-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="c2403-134">Requirement</span></span> | <span data-ttu-id="c2403-135">Valore</span><span class="sxs-lookup"><span data-stu-id="c2403-135">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2403-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c2403-136">Minimum supported client</span></span><br/> | <span data-ttu-id="c2403-137">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c2403-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="c2403-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c2403-138">Minimum supported server</span></span><br/> | <span data-ttu-id="c2403-139">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c2403-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="c2403-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c2403-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="c2403-141"><dt>DDEML. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c2403-141"><dt>Ddeml.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2403-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c2403-142">See also</span></span>

<dl> <dt>

<span data-ttu-id="c2403-143">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="c2403-143">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c2403-144">**DdeCreateDataHandle**</span><span class="sxs-lookup"><span data-stu-id="c2403-144">**DdeCreateDataHandle**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle)
</dt> <dt>

[<span data-ttu-id="c2403-145">**DdeInitialize**</span><span class="sxs-lookup"><span data-stu-id="c2403-145">**DdeInitialize**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

[<span data-ttu-id="c2403-146">**DdePostAdvise**</span><span class="sxs-lookup"><span data-stu-id="c2403-146">**DdePostAdvise**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise)
</dt> <dt>

<span data-ttu-id="c2403-147">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="c2403-147">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="c2403-148">Libreria di gestione Dynamic Data Exchange</span><span class="sxs-lookup"><span data-stu-id="c2403-148">Dynamic Data Exchange Management Library</span></span>](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

