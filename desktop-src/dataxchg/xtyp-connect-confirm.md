---
title: Transazione XTYP_CONNECT_CONFIRM (DDEML. h)
description: Una funzione di callback del server Dynamic Data Exchange (DDE), DdeCallback, riceve la \_ conferma della transazione XTYP Connect \_ per confermare che è stata stabilita una conversazione con un client e per fornire al server l'handle di conversazione.
ms.assetid: 4db67539-9322-44d7-bf2b-749bd6cfcbb4
keywords:
- Scambio di dati delle transazioni XTYP_CONNECT_CONFIRM
topic_type:
- apiref
api_name:
- XTYP_CONNECT_CONFIRM
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e880dfffc7f7825c99ab9e4e3bf980baa978b786
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400684"
---
# <a name="xtyp_connect_confirm-transaction"></a><span data-ttu-id="1f38d-104">\_ \_ Conferma transazione connessione XTYP</span><span class="sxs-lookup"><span data-stu-id="1f38d-104">XTYP\_CONNECT\_CONFIRM transaction</span></span>

<span data-ttu-id="1f38d-105">Una funzione di callback del server Dynamic Data Exchange (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), riceve la conferma della transazione **XTYP \_ Connect \_** per confermare che è stata stabilita una conversazione con un client e per fornire al server l'handle di conversazione.</span><span class="sxs-lookup"><span data-stu-id="1f38d-105">A Dynamic Data Exchange (DDE) server callback function, [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), receives the **XTYP\_CONNECT\_CONFIRM** transaction to confirm that a conversation has been established with a client and to provide the server with the conversation handle.</span></span> <span data-ttu-id="1f38d-106">Questa transazione viene inviata dal sistema come risultato di una transazione [**XTYP \_ Connect**](xtyp-connect.md) o [**XTYP \_ WILDCONNECT**](xtyp-wildconnect.md) precedente.</span><span class="sxs-lookup"><span data-stu-id="1f38d-106">The system sends this transaction as a result of a previous [**XTYP\_CONNECT**](xtyp-connect.md) or [**XTYP\_WILDCONNECT**](xtyp-wildconnect.md) transaction.</span></span>


```C++
#define     XTYPF_NOBLOCK            0x0002
#define     XCLASS_NOTIFICATION      0x8000
#define     XTYP_CONNECT_CONFIRM    (0x0070 | XCLASS_NOTIFICATION | XTYPF_NOBLOCK)
```



## <a name="parameters"></a><span data-ttu-id="1f38d-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="1f38d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f38d-108">*uType*</span><span class="sxs-lookup"><span data-stu-id="1f38d-108">*uType*</span></span> 
</dt> <dd>

<span data-ttu-id="1f38d-109">Tipo di transazione.</span><span class="sxs-lookup"><span data-stu-id="1f38d-109">The transaction type.</span></span>

</dd> <dt>

<span data-ttu-id="1f38d-110">*uFmt*</span><span class="sxs-lookup"><span data-stu-id="1f38d-110">*uFmt*</span></span> 
</dt> <dd>

<span data-ttu-id="1f38d-111">Non usato.</span><span class="sxs-lookup"><span data-stu-id="1f38d-111">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="1f38d-112">*hconv*</span><span class="sxs-lookup"><span data-stu-id="1f38d-112">*hconv*</span></span> 
</dt> <dd>

<span data-ttu-id="1f38d-113">Handle per la nuova conversazione.</span><span class="sxs-lookup"><span data-stu-id="1f38d-113">A handle to the new conversation.</span></span>

</dd> <dt>

<span data-ttu-id="1f38d-114">*hsz1*</span><span class="sxs-lookup"><span data-stu-id="1f38d-114">*hsz1*</span></span> 
</dt> <dd>

<span data-ttu-id="1f38d-115">Handle per il nome dell'argomento in cui è stata stabilita la conversazione.</span><span class="sxs-lookup"><span data-stu-id="1f38d-115">A handle to the topic name on which the conversation has been established.</span></span>

</dd> <dt>

<span data-ttu-id="1f38d-116">*hsz2*</span><span class="sxs-lookup"><span data-stu-id="1f38d-116">*hsz2*</span></span> 
</dt> <dd>

<span data-ttu-id="1f38d-117">Handle per il nome del servizio in cui è stata stabilita la conversazione.</span><span class="sxs-lookup"><span data-stu-id="1f38d-117">A handle to the service name on which the conversation has been established.</span></span>

</dd> <dt>

<span data-ttu-id="1f38d-118">*hdata*</span><span class="sxs-lookup"><span data-stu-id="1f38d-118">*hdata*</span></span> 
</dt> <dd>

<span data-ttu-id="1f38d-119">Non usato.</span><span class="sxs-lookup"><span data-stu-id="1f38d-119">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="1f38d-120">*dwData1*</span><span class="sxs-lookup"><span data-stu-id="1f38d-120">*dwData1*</span></span> 
</dt> <dd>

<span data-ttu-id="1f38d-121">Non usato.</span><span class="sxs-lookup"><span data-stu-id="1f38d-121">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="1f38d-122">*dwData2*</span><span class="sxs-lookup"><span data-stu-id="1f38d-122">*dwData2*</span></span> 
</dt> <dd>

<span data-ttu-id="1f38d-123">Specifica se il client è la stessa istanza dell'applicazione del server.</span><span class="sxs-lookup"><span data-stu-id="1f38d-123">Specifies whether the client is the same application instance as the server.</span></span> <span data-ttu-id="1f38d-124">Se il parametro è 1, il client è la stessa istanza.</span><span class="sxs-lookup"><span data-stu-id="1f38d-124">If the parameter is 1, the client is the same instance.</span></span> <span data-ttu-id="1f38d-125">Se il parametro è 0, il client è un'istanza diversa.</span><span class="sxs-lookup"><span data-stu-id="1f38d-125">If the parameter is 0, the client is a different instance.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1f38d-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="1f38d-126">Remarks</span></span>

<span data-ttu-id="1f38d-127">Questa transazione viene filtrata se l'applicazione server specificata **CBF \_ Skip \_ Connect \_ conferma** flag nella funzione [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .</span><span class="sxs-lookup"><span data-stu-id="1f38d-127">This transaction is filtered if the server application specified the **CBF\_SKIP\_CONNECT\_CONFIRMS** flag in the [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) function.</span></span>

<span data-ttu-id="1f38d-128">Un server non è in grado di bloccare questo tipo di transazione. il codice restituito del **\_ blocco CBR** viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="1f38d-128">A server cannot block this transaction type; the **CBR\_BLOCK** return code is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f38d-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1f38d-129">Requirements</span></span>



| <span data-ttu-id="1f38d-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="1f38d-130">Requirement</span></span> | <span data-ttu-id="1f38d-131">Valore</span><span class="sxs-lookup"><span data-stu-id="1f38d-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f38d-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1f38d-132">Minimum supported client</span></span><br/> | <span data-ttu-id="1f38d-133">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="1f38d-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="1f38d-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1f38d-134">Minimum supported server</span></span><br/> | <span data-ttu-id="1f38d-135">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="1f38d-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="1f38d-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1f38d-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="1f38d-137"><dt>DDEML. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1f38d-137"><dt>Ddeml.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f38d-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1f38d-138">See also</span></span>

<dl> <dt>

<span data-ttu-id="1f38d-139">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="1f38d-139">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="1f38d-140">**DdeConnect**</span><span class="sxs-lookup"><span data-stu-id="1f38d-140">**DdeConnect**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect)
</dt> <dt>

[<span data-ttu-id="1f38d-141">**DdeConnectList**</span><span class="sxs-lookup"><span data-stu-id="1f38d-141">**DdeConnectList**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist)
</dt> <dt>

[<span data-ttu-id="1f38d-142">**DdeInitialize**</span><span class="sxs-lookup"><span data-stu-id="1f38d-142">**DdeInitialize**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

<span data-ttu-id="1f38d-143">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="1f38d-143">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="1f38d-144">Libreria di gestione Dynamic Data Exchange</span><span class="sxs-lookup"><span data-stu-id="1f38d-144">Dynamic Data Exchange Management Library</span></span>](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

