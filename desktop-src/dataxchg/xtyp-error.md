---
title: Transazione XTYP_ERROR (DDEML. h)
description: Una funzione di callback Dynamic Data Exchange (DDE), DdeCallback, riceve la \_ transazione di errore XTYP quando si verifica un errore critico.
ms.assetid: 710daa04-ed83-42e3-a55e-6ccf891a3d52
keywords:
- Scambio di dati delle transazioni XTYP_ERROR
topic_type:
- apiref
api_name:
- XTYP_ERROR
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebbad80cb23a37881e8954dee4a80a87f253e499
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301597"
---
# <a name="xtyp_error-transaction"></a><span data-ttu-id="f0760-104">\_Transazione di errore XTYP</span><span class="sxs-lookup"><span data-stu-id="f0760-104">XTYP\_ERROR transaction</span></span>

<span data-ttu-id="f0760-105">Una funzione di callback Dynamic Data Exchange (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), riceve la transazione di **\_ errore XTYP** quando si verifica un errore critico.</span><span class="sxs-lookup"><span data-stu-id="f0760-105">A Dynamic Data Exchange (DDE) callback function, [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), receives the **XTYP\_ERROR** transaction when a critical error occurs.</span></span>


```C++
#define     XCLASS_NOTIFICATION      0x8000
#define     XTYPF_NOBLOCK            0x0002
#define     XTYP_ERROR              (0x0000 | XCLASS_NOTIFICATION | XTYPF_NOBLOCK )
```



## <a name="parameters"></a><span data-ttu-id="f0760-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f0760-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0760-107">*uType*</span><span class="sxs-lookup"><span data-stu-id="f0760-107">*uType*</span></span> 
</dt> <dd>

<span data-ttu-id="f0760-108">Tipo di transazione.</span><span class="sxs-lookup"><span data-stu-id="f0760-108">The transaction type.</span></span>

</dd> <dt>

<span data-ttu-id="f0760-109">*uFmt*</span><span class="sxs-lookup"><span data-stu-id="f0760-109">*uFmt*</span></span> 
</dt> <dd>

<span data-ttu-id="f0760-110">Non usato.</span><span class="sxs-lookup"><span data-stu-id="f0760-110">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="f0760-111">*hconv*</span><span class="sxs-lookup"><span data-stu-id="f0760-111">*hconv*</span></span> 
</dt> <dd>

<span data-ttu-id="f0760-112">Handle per la conversazione associata all'errore.</span><span class="sxs-lookup"><span data-stu-id="f0760-112">A handle to the conversation associated with the error.</span></span> <span data-ttu-id="f0760-113">Questo parametro è **null** se l'errore non è associato a una conversazione.</span><span class="sxs-lookup"><span data-stu-id="f0760-113">This parameter is **NULL** if the error is not associated with a conversation.</span></span>

</dd> <dt>

<span data-ttu-id="f0760-114">*hsz1*</span><span class="sxs-lookup"><span data-stu-id="f0760-114">*hsz1*</span></span> 
</dt> <dd>

<span data-ttu-id="f0760-115">Non usato.</span><span class="sxs-lookup"><span data-stu-id="f0760-115">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="f0760-116">*hsz2*</span><span class="sxs-lookup"><span data-stu-id="f0760-116">*hsz2*</span></span> 
</dt> <dd>

<span data-ttu-id="f0760-117">Non usato.</span><span class="sxs-lookup"><span data-stu-id="f0760-117">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="f0760-118">*hdata*</span><span class="sxs-lookup"><span data-stu-id="f0760-118">*hdata*</span></span> 
</dt> <dd>

<span data-ttu-id="f0760-119">Non usato.</span><span class="sxs-lookup"><span data-stu-id="f0760-119">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="f0760-120">*dwData1*</span><span class="sxs-lookup"><span data-stu-id="f0760-120">*dwData1*</span></span> 
</dt> <dd>

<span data-ttu-id="f0760-121">Codice di errore nella parola di ordine inferiore.</span><span class="sxs-lookup"><span data-stu-id="f0760-121">The error code in the low-order word.</span></span> <span data-ttu-id="f0760-122">Attualmente, è supportato solo il codice di errore seguente.</span><span class="sxs-lookup"><span data-stu-id="f0760-122">Currently, only the following error code is supported.</span></span>



| <span data-ttu-id="f0760-123">Valore</span><span class="sxs-lookup"><span data-stu-id="f0760-123">Value</span></span>                                                                                                                                                                      | <span data-ttu-id="f0760-124">Significato</span><span class="sxs-lookup"><span data-stu-id="f0760-124">Meaning</span></span>                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span id="DMLERR_LOW_MEMORY"></span><span id="dmlerr_low_memory"></span><dl> <span data-ttu-id="f0760-125"><dt>**\_memoria insufficiente DMLERR \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f0760-125"><dt>**DMLERR\_LOW\_MEMORY**</dt></span></span> </dl> | <span data-ttu-id="f0760-126">Memoria insufficiente. è possibile che i dati Advise, poke o Execute vadano persi o che il sistema abbia esito negativo.</span><span class="sxs-lookup"><span data-stu-id="f0760-126">Memory is low; advise, poke, or execute data may be lost, or the system may fail.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="f0760-127">*dwData2*</span><span class="sxs-lookup"><span data-stu-id="f0760-127">*dwData2*</span></span> 
</dt> <dd>

<span data-ttu-id="f0760-128">Non usato.</span><span class="sxs-lookup"><span data-stu-id="f0760-128">Not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f0760-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="f0760-129">Remarks</span></span>

<span data-ttu-id="f0760-130">Un'applicazione non può bloccare questo tipo di transazione. il codice restituito del **\_ blocco CBR** viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="f0760-130">An application cannot block this transaction type; the **CBR\_BLOCK** return code is ignored.</span></span> <span data-ttu-id="f0760-131">La libreria di gestione Dynamic Data Exchange (DDEML) tenta di liberare memoria rimuovendo le risorse non critiche.</span><span class="sxs-lookup"><span data-stu-id="f0760-131">The Dynamic Data Exchange Management Library (DDEML) attempts to free memory by removing noncritical resources.</span></span> <span data-ttu-id="f0760-132">Un'applicazione che dispone di conversazioni bloccate dovrebbe sbloccarle.</span><span class="sxs-lookup"><span data-stu-id="f0760-132">An application that has blocked conversations should unblock them.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0760-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f0760-133">Requirements</span></span>



| <span data-ttu-id="f0760-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="f0760-134">Requirement</span></span> | <span data-ttu-id="f0760-135">Valore</span><span class="sxs-lookup"><span data-stu-id="f0760-135">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0760-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f0760-136">Minimum supported client</span></span><br/> | <span data-ttu-id="f0760-137">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f0760-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="f0760-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f0760-138">Minimum supported server</span></span><br/> | <span data-ttu-id="f0760-139">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f0760-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="f0760-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f0760-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="f0760-141"><dt>DDEML. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f0760-141"><dt>Ddeml.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0760-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f0760-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0760-143">Panoramica della libreria di gestione Dynamic Data Exchange</span><span class="sxs-lookup"><span data-stu-id="f0760-143">Dynamic Data Exchange Management Library Overview</span></span>](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

