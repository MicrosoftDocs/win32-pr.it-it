---
title: Transazione XTYP_DISCONNECT (DDEML. h)
description: La funzione di callback Dynamic Data Exchange (DDE) di un'applicazione, DdeCallback, riceve la \_ transazione di disconnessione XTYP quando il partner dell'applicazione in una conversazione usa la funzione DdeDisconnect per terminare la conversazione.
ms.assetid: 22a9ec63-8a74-4829-ad02-d07dd0e8fa9b
keywords:
- Scambio di dati delle transazioni XTYP_DISCONNECT
topic_type:
- apiref
api_name:
- XTYP_DISCONNECT
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38e73bc0446989ac572a27f394e594924573711d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740330"
---
# <a name="xtyp_disconnect-transaction"></a><span data-ttu-id="2bd8c-104">\_Transazione disconnessione XTYP</span><span class="sxs-lookup"><span data-stu-id="2bd8c-104">XTYP\_DISCONNECT transaction</span></span>

<span data-ttu-id="2bd8c-105">La funzione di callback Dynamic Data Exchange (DDE) di un'applicazione, [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), riceve la transazione di **\_ disconnessione XTYP** quando il partner dell'applicazione in una conversazione usa la funzione [**DdeDisconnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddedisconnect) per terminare la conversazione.</span><span class="sxs-lookup"><span data-stu-id="2bd8c-105">An application's Dynamic Data Exchange (DDE) callback function, [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), receives the **XTYP\_DISCONNECT** transaction when the application's partner in a conversation uses the [**DdeDisconnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddedisconnect) function to terminate the conversation.</span></span>


```C++
#define     XCLASS_NOTIFICATION      0x8000
#define     XTYPF_NOBLOCK            0x0002
#define     XTYP_DISCONNECT         (0x00C0 | XCLASS_NOTIFICATION | XTYPF_NOBLOCK)
```



## <a name="parameters"></a><span data-ttu-id="2bd8c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="2bd8c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2bd8c-107">*uType*</span><span class="sxs-lookup"><span data-stu-id="2bd8c-107">*uType*</span></span> 
</dt> <dd>

<span data-ttu-id="2bd8c-108">Tipo di transazione.</span><span class="sxs-lookup"><span data-stu-id="2bd8c-108">The transaction type.</span></span>

</dd> <dt>

<span data-ttu-id="2bd8c-109">*uFmt*</span><span class="sxs-lookup"><span data-stu-id="2bd8c-109">*uFmt*</span></span> 
</dt> <dd>

<span data-ttu-id="2bd8c-110">Non usato.</span><span class="sxs-lookup"><span data-stu-id="2bd8c-110">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="2bd8c-111">*hconv*</span><span class="sxs-lookup"><span data-stu-id="2bd8c-111">*hconv*</span></span> 
</dt> <dd>

<span data-ttu-id="2bd8c-112">Handle a che la conversazione è stata terminata.</span><span class="sxs-lookup"><span data-stu-id="2bd8c-112">A handle to that the conversation was terminated.</span></span>

</dd> <dt>

<span data-ttu-id="2bd8c-113">*hsz1*</span><span class="sxs-lookup"><span data-stu-id="2bd8c-113">*hsz1*</span></span> 
</dt> <dd>

<span data-ttu-id="2bd8c-114">Non usato.</span><span class="sxs-lookup"><span data-stu-id="2bd8c-114">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="2bd8c-115">*hsz2*</span><span class="sxs-lookup"><span data-stu-id="2bd8c-115">*hsz2*</span></span> 
</dt> <dd>

<span data-ttu-id="2bd8c-116">Non usato.</span><span class="sxs-lookup"><span data-stu-id="2bd8c-116">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="2bd8c-117">*hdata*</span><span class="sxs-lookup"><span data-stu-id="2bd8c-117">*hdata*</span></span> 
</dt> <dd>

<span data-ttu-id="2bd8c-118">Non usato.</span><span class="sxs-lookup"><span data-stu-id="2bd8c-118">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="2bd8c-119">*dwData1*</span><span class="sxs-lookup"><span data-stu-id="2bd8c-119">*dwData1*</span></span> 
</dt> <dd>

<span data-ttu-id="2bd8c-120">Non usato.</span><span class="sxs-lookup"><span data-stu-id="2bd8c-120">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="2bd8c-121">*dwData2*</span><span class="sxs-lookup"><span data-stu-id="2bd8c-121">*dwData2*</span></span> 
</dt> <dd>

<span data-ttu-id="2bd8c-122">Specifica se i partner nella conversazione sono la stessa istanza dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="2bd8c-122">Specifies whether the partners in the conversation are the same application instance.</span></span> <span data-ttu-id="2bd8c-123">Se questo parametro è 1, i partner sono la stessa istanza.</span><span class="sxs-lookup"><span data-stu-id="2bd8c-123">If this parameter is 1, the partners are the same instance.</span></span> <span data-ttu-id="2bd8c-124">Se questo parametro è 0, i partner sono istanze diverse.</span><span class="sxs-lookup"><span data-stu-id="2bd8c-124">If this parameter is 0, the partners are different instances.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2bd8c-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="2bd8c-125">Remarks</span></span>

<span data-ttu-id="2bd8c-126">Questa transazione viene filtrata se l'applicazione ha specificato il flag **CBF \_ Skip \_ disconnectes** nella funzione [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .</span><span class="sxs-lookup"><span data-stu-id="2bd8c-126">This transaction is filtered if the application specified the **CBF\_SKIP\_DISCONNECTS** flag in the [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) function.</span></span>

<span data-ttu-id="2bd8c-127">L'applicazione può ottenere lo stato della conversazione terminata chiamando la funzione [**DdeQueryConvInfo**](/windows/desktop/api/Ddeml/nf-ddeml-ddequeryconvinfo) durante l'elaborazione della transazione.</span><span class="sxs-lookup"><span data-stu-id="2bd8c-127">The application can obtain the status of the terminated conversation by calling the [**DdeQueryConvInfo**](/windows/desktop/api/Ddeml/nf-ddeml-ddequeryconvinfo) function while processing this transaction.</span></span> <span data-ttu-id="2bd8c-128">L'handle di conversazione diventa non valido dopo la restituzione della funzione di callback.</span><span class="sxs-lookup"><span data-stu-id="2bd8c-128">The conversation handle becomes invalid after the callback function returns.</span></span>

<span data-ttu-id="2bd8c-129">Un'applicazione non può bloccare questo tipo di transazione. il codice restituito del **\_ blocco CBR** viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="2bd8c-129">An application cannot block this transaction type; the **CBR\_BLOCK** return code is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="2bd8c-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2bd8c-130">Requirements</span></span>



| <span data-ttu-id="2bd8c-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="2bd8c-131">Requirement</span></span> | <span data-ttu-id="2bd8c-132">Valore</span><span class="sxs-lookup"><span data-stu-id="2bd8c-132">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2bd8c-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2bd8c-133">Minimum supported client</span></span><br/> | <span data-ttu-id="2bd8c-134">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2bd8c-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="2bd8c-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2bd8c-135">Minimum supported server</span></span><br/> | <span data-ttu-id="2bd8c-136">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2bd8c-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="2bd8c-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2bd8c-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="2bd8c-138"><dt>DDEML. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2bd8c-138"><dt>Ddeml.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2bd8c-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2bd8c-139">See also</span></span>

<dl> <dt>

<span data-ttu-id="2bd8c-140">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="2bd8c-140">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="2bd8c-141">**DdeDisconnect**</span><span class="sxs-lookup"><span data-stu-id="2bd8c-141">**DdeDisconnect**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddedisconnect)
</dt> <dt>

[<span data-ttu-id="2bd8c-142">**DdeInitialize**</span><span class="sxs-lookup"><span data-stu-id="2bd8c-142">**DdeInitialize**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

[<span data-ttu-id="2bd8c-143">**DdeQueryConvInfo**</span><span class="sxs-lookup"><span data-stu-id="2bd8c-143">**DdeQueryConvInfo**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddequeryconvinfo)
</dt> <dt>

<span data-ttu-id="2bd8c-144">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="2bd8c-144">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="2bd8c-145">Libreria di gestione Dynamic Data Exchange</span><span class="sxs-lookup"><span data-stu-id="2bd8c-145">Dynamic Data Exchange Management Library</span></span>](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

