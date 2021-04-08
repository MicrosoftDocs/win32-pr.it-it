---
title: Transazione XTYP_UNREGISTER (DDEML. h)
description: Una funzione di callback Dynamic Data Exchange (DDE), DdeCallback, riceve la \_ transazione di annullamento della registrazione di XTYP ogni volta che un'applicazione server DDEML (Dynamic Data Exchange Management Library) usa la funzione DdeNameService per annullare la registrazione di un nome di servizio o ogni volta che un'applicazione non DDEML che supporta l'argomento di sistema viene terminata.
ms.assetid: a57a5d53-7919-4698-8c84-6142dd29bb2a
keywords:
- Scambio di dati delle transazioni XTYP_UNREGISTER
topic_type:
- apiref
api_name:
- XTYP_UNREGISTER
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eeba96b26c019aa0a3050a83f726745b749efa96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742871"
---
# <a name="xtyp_unregister-transaction"></a><span data-ttu-id="b248b-104">XTYP \_ Annulla registrazione transazione</span><span class="sxs-lookup"><span data-stu-id="b248b-104">XTYP\_UNREGISTER transaction</span></span>

<span data-ttu-id="b248b-105">Una funzione di callback Dynamic Data Exchange (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), riceve la transazione di **annullamento della \_ registrazione di XTYP** ogni volta che un'applicazione server DDEML (Dynamic Data Exchange Management Library) usa la funzione [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) per annullare la registrazione di un nome di servizio o ogni volta che un'applicazione non DDEML che supporta l'argomento di sistema viene terminata.</span><span class="sxs-lookup"><span data-stu-id="b248b-105">A Dynamic Data Exchange (DDE) callback function, [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), receives the **XTYP\_UNREGISTER** transaction whenever a Dynamic Data Exchange Management Library (DDEML) server application uses the [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) function to unregister a service name, or whenever a non-DDEML application that supports the System topic is terminated.</span></span>


```C++
#define     XCLASS_NOTIFICATION      0x8000
#define     XTYPF_NOBLOCK            0x0002
#define     XTYP_UNREGISTER         (0x00D0 | XCLASS_NOTIFICATION | XTYPF_NOBLOCK)
```



## <a name="parameters"></a><span data-ttu-id="b248b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b248b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b248b-107">*uType*</span><span class="sxs-lookup"><span data-stu-id="b248b-107">*uType*</span></span> 
</dt> <dd>

<span data-ttu-id="b248b-108">Tipo di transazione.</span><span class="sxs-lookup"><span data-stu-id="b248b-108">The transaction type.</span></span>

</dd> <dt>

<span data-ttu-id="b248b-109">*uFmt*</span><span class="sxs-lookup"><span data-stu-id="b248b-109">*uFmt*</span></span> 
</dt> <dd>

<span data-ttu-id="b248b-110">Non usato.</span><span class="sxs-lookup"><span data-stu-id="b248b-110">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="b248b-111">*hconv*</span><span class="sxs-lookup"><span data-stu-id="b248b-111">*hconv*</span></span> 
</dt> <dd>

<span data-ttu-id="b248b-112">Non usato.</span><span class="sxs-lookup"><span data-stu-id="b248b-112">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="b248b-113">*hsz1*</span><span class="sxs-lookup"><span data-stu-id="b248b-113">*hsz1*</span></span> 
</dt> <dd>

<span data-ttu-id="b248b-114">Handle per il nome del servizio di base di cui viene annullata la registrazione.</span><span class="sxs-lookup"><span data-stu-id="b248b-114">A handle to the base service name being unregistered.</span></span>

</dd> <dt>

<span data-ttu-id="b248b-115">*hsz2*</span><span class="sxs-lookup"><span data-stu-id="b248b-115">*hsz2*</span></span> 
</dt> <dd>

<span data-ttu-id="b248b-116">Handle per il nome del servizio specifico dell'istanza di cui viene annullata la registrazione.</span><span class="sxs-lookup"><span data-stu-id="b248b-116">A handle to the instance-specific service name being unregistered.</span></span>

</dd> <dt>

<span data-ttu-id="b248b-117">*hdata*</span><span class="sxs-lookup"><span data-stu-id="b248b-117">*hdata*</span></span> 
</dt> <dd>

<span data-ttu-id="b248b-118">Non usato.</span><span class="sxs-lookup"><span data-stu-id="b248b-118">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="b248b-119">*dwData1*</span><span class="sxs-lookup"><span data-stu-id="b248b-119">*dwData1*</span></span> 
</dt> <dd>

<span data-ttu-id="b248b-120">Non usato.</span><span class="sxs-lookup"><span data-stu-id="b248b-120">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="b248b-121">*dwData2*</span><span class="sxs-lookup"><span data-stu-id="b248b-121">*dwData2*</span></span> 
</dt> <dd>

<span data-ttu-id="b248b-122">Non usato.</span><span class="sxs-lookup"><span data-stu-id="b248b-122">Not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b248b-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="b248b-123">Remarks</span></span>

<span data-ttu-id="b248b-124">Questa transazione viene filtrata se l'applicazione ha specificato il flag **CBF \_ Skip \_ registrations** nella funzione [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .</span><span class="sxs-lookup"><span data-stu-id="b248b-124">This transaction is filtered if the application specified the **CBF\_SKIP\_REGISTRATIONS** flag in the [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) function.</span></span>

<span data-ttu-id="b248b-125">Un'applicazione non può bloccare questo tipo di transazione. il \_ codice restituito del blocco CBR viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="b248b-125">A application cannot block this transaction type; the CBR\_BLOCK return code is ignored.</span></span>

<span data-ttu-id="b248b-126">Un'applicazione deve utilizzare il parametro *hsz1* per rimuovere il nome del servizio dall'elenco dei server disponibili per l'utente.</span><span class="sxs-lookup"><span data-stu-id="b248b-126">An application should use the *hsz1* parameter to remove the service name from the list of servers available to the user.</span></span> <span data-ttu-id="b248b-127">Un'applicazione deve utilizzare il parametro *hsz2* per identificare l'istanza dell'applicazione terminata.</span><span class="sxs-lookup"><span data-stu-id="b248b-127">An application should use the *hsz2* parameter to identify which application instance has terminated.</span></span>

## <a name="requirements"></a><span data-ttu-id="b248b-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b248b-128">Requirements</span></span>



| <span data-ttu-id="b248b-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="b248b-129">Requirement</span></span> | <span data-ttu-id="b248b-130">Valore</span><span class="sxs-lookup"><span data-stu-id="b248b-130">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b248b-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b248b-131">Minimum supported client</span></span><br/> | <span data-ttu-id="b248b-132">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b248b-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="b248b-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b248b-133">Minimum supported server</span></span><br/> | <span data-ttu-id="b248b-134">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b248b-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="b248b-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b248b-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="b248b-136"><dt>DDEML. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b248b-136"><dt>Ddeml.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b248b-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b248b-137">See also</span></span>

<dl> <dt>

<span data-ttu-id="b248b-138">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="b248b-138">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b248b-139">**DdeInitialize**</span><span class="sxs-lookup"><span data-stu-id="b248b-139">**DdeInitialize**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

[<span data-ttu-id="b248b-140">**DdeNameService**</span><span class="sxs-lookup"><span data-stu-id="b248b-140">**DdeNameService**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice)
</dt> <dt>

<span data-ttu-id="b248b-141">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="b248b-141">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="b248b-142">Libreria di gestione Dynamic Data Exchange</span><span class="sxs-lookup"><span data-stu-id="b248b-142">Dynamic Data Exchange Management Library</span></span>](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

