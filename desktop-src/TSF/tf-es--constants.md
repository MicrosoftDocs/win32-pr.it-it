---
title: Costanti TF_ES_ (msctf. h)
description: Di seguito sono riportate le costanti utilizzate dal metodo RequestEditSession di ITfContext.
ms.assetid: 5498329f-3302-4f66-bdec-cab7db0cdc0e
topic_type:
- apiref
api_name:
- TF_ES_ASYNCDONTCARE
- TF_ES_SYNC
- TF_ES_READ
- TF_ES_READWRITE
- TF_ES_ASYNC
api_location:
- Msctf.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa8ed96adc1d6f6d66671e91f7a70bce856663e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302234"
---
# <a name="tf_es_-constants"></a><span data-ttu-id="6cf80-103">\_Costanti TF es \_ \*</span><span class="sxs-lookup"><span data-stu-id="6cf80-103">TF\_ES\_\* Constants</span></span>

<span data-ttu-id="6cf80-104">Di seguito sono riportate le costanti usate dal metodo [ITfContext:: RequestEditSession](/windows/desktop/api/Msctf/nf-msctf-itfcontext-requesteditsession) .</span><span class="sxs-lookup"><span data-stu-id="6cf80-104">The following are constants used by the [ITfContext::RequestEditSession](/windows/desktop/api/Msctf/nf-msctf-itfcontext-requesteditsession) method.</span></span>



| <span data-ttu-id="6cf80-105">Costante/valore</span><span class="sxs-lookup"><span data-stu-id="6cf80-105">Constant/value</span></span>                                                                                                                                                                                                                              | <span data-ttu-id="6cf80-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6cf80-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                             |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_ES_ASYNCDONTCARE"></span><span id="tf_es_asyncdontcare"></span><dl> <span data-ttu-id="6cf80-107"><dt>**Tf \_ ES \_ ASYNCDONTCARE**</dt> <dt>(0)</dt></span><span class="sxs-lookup"><span data-stu-id="6cf80-107"><dt>**TF\_ES\_ASYNCDONTCARE**</dt> <dt>( 0 )</dt></span></span> </dl> | <span data-ttu-id="6cf80-108">La sessione di modifica può essere eseguita in modalità sincrona o asincrona, a discrezione del responsabile.</span><span class="sxs-lookup"><span data-stu-id="6cf80-108">The edit session can occur synchronously or asynchronously, at the discretion of the manager.</span></span> <span data-ttu-id="6cf80-109">Il responsabile tenterà di pianificare una sessione di modifica sincrona per migliorare le prestazioni.</span><span class="sxs-lookup"><span data-stu-id="6cf80-109">The manager will attempt to schedule a synchronous edit session for improved performance.</span></span> <span data-ttu-id="6cf80-110">Questo valore non può essere combinato con i \_ valori di sincronizzazione TF es \_ Async o TF \_ es \_ .</span><span class="sxs-lookup"><span data-stu-id="6cf80-110">This value cannot be combined with the TF\_ES\_ASYNC or TF\_ES\_SYNC values.</span></span><br/>                                                                         |
| <span id="TF_ES_SYNC"></span><span id="tf_es_sync"></span><dl> <span data-ttu-id="6cf80-111"><dt>**Tf \_ \_Sincronizzazione es**</dt> <dt>(0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="6cf80-111"><dt>**TF\_ES\_SYNC**</dt> <dt>( 0x1 )</dt></span></span> </dl>                          | <span data-ttu-id="6cf80-112">La sessione di modifica deve essere sincrona o la richiesta avrà esito negativo (con TF \_ E \_ sincrono).</span><span class="sxs-lookup"><span data-stu-id="6cf80-112">The edit session must be synchronous or the request will fail (with TF\_E\_SYNCHRONOUS).</span></span> <span data-ttu-id="6cf80-113">Questo flag deve essere usato solo in situazioni documentate, ad esempio la gestione delle sequenze di tasti, in cui può essere previsto che abbia esito positivo.</span><span class="sxs-lookup"><span data-stu-id="6cf80-113">This flag should only be used in documented situations (such as keystroke handling) where it can be expected to succeed.</span></span> <span data-ttu-id="6cf80-114">In caso contrario, la chiamata avrà probabilmente esito negativo.</span><span class="sxs-lookup"><span data-stu-id="6cf80-114">Otherwise the call will likely fail.</span></span> <span data-ttu-id="6cf80-115">Questo valore non può essere combinato con i \_ \_ valori asincroni TF es ASYNCDONTCARE o TF \_ es \_ .</span><span class="sxs-lookup"><span data-stu-id="6cf80-115">This value cannot be combined with the TF\_ES\_ASYNCDONTCARE or TF\_ES\_ASYNC values.</span></span><br/> |
| <span id="TF_ES_READ"></span><span id="tf_es_read"></span><dl> <span data-ttu-id="6cf80-116"><dt>**Tf \_ \_Lettura es**</dt> <dt>(0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="6cf80-116"><dt>**TF\_ES\_READ**</dt> <dt>( 0x2 )</dt></span></span> </dl>                          | <span data-ttu-id="6cf80-117">Richiede l'accesso in sola lettura al contesto.</span><span class="sxs-lookup"><span data-stu-id="6cf80-117">Requests read-only access to the context.</span></span><br/>                                                                                                                                                                                                                                                                                                    |
| <span id="TF_ES_READWRITE"></span><span id="tf_es_readwrite"></span><dl> <span data-ttu-id="6cf80-118"><dt>**Tf \_ ES \_ ReadWrite**</dt> <dt>(0x6)</dt></span><span class="sxs-lookup"><span data-stu-id="6cf80-118"><dt>**TF\_ES\_READWRITE**</dt> <dt>( 0x6 )</dt></span></span> </dl>           | <span data-ttu-id="6cf80-119">Richiede l'accesso in lettura/scrittura al contesto.</span><span class="sxs-lookup"><span data-stu-id="6cf80-119">Requests read/write access to the context.</span></span><br/>                                                                                                                                                                                                                                                                                                   |
| <span id="TF_ES_ASYNC"></span><span id="tf_es_async"></span><dl> <span data-ttu-id="6cf80-120"><dt>**Tf \_ ES \_ Async**</dt> <dt>(0x8)</dt></span><span class="sxs-lookup"><span data-stu-id="6cf80-120"><dt>**TF\_ES\_ASYNC**</dt> <dt>( 0x8 )</dt></span></span> </dl>                       | <span data-ttu-id="6cf80-121">La sessione di modifica deve essere asincrona o la richiesta avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="6cf80-121">The edit session must be asynchronous or the request will fail.</span></span> <span data-ttu-id="6cf80-122">Questo valore non può essere combinato con i \_ valori della sincronizzazione TF es \_ ASYNCDONTCARE o TF \_ es \_ .</span><span class="sxs-lookup"><span data-stu-id="6cf80-122">This value cannot be combined with the TF\_ES\_ASYNCDONTCARE or TF\_ES\_SYNC values.</span></span><br/>                                                                                                                                                                                         |



## <a name="requirements"></a><span data-ttu-id="6cf80-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6cf80-123">Requirements</span></span>



| <span data-ttu-id="6cf80-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="6cf80-124">Requirement</span></span> | <span data-ttu-id="6cf80-125">Valore</span><span class="sxs-lookup"><span data-stu-id="6cf80-125">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="6cf80-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6cf80-126">Minimum supported client</span></span><br/> | <span data-ttu-id="6cf80-127">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6cf80-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="6cf80-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6cf80-128">Minimum supported server</span></span><br/> | <span data-ttu-id="6cf80-129">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6cf80-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="6cf80-130">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="6cf80-130">Redistributable</span></span><br/>          | <span data-ttu-id="6cf80-131">TSF 1,0 su Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="6cf80-131">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                      |
| <span data-ttu-id="6cf80-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6cf80-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="6cf80-133"><dt>Msctf. h</dt></span><span class="sxs-lookup"><span data-stu-id="6cf80-133"><dt>Msctf.h</dt></span></span> </dl>   |
| <span data-ttu-id="6cf80-134">IDL</span><span class="sxs-lookup"><span data-stu-id="6cf80-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6cf80-135"><dt>Msctf. idl</dt></span><span class="sxs-lookup"><span data-stu-id="6cf80-135"><dt>Msctf.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6cf80-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6cf80-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6cf80-137">ITfContext:: RequestEditSession</span><span class="sxs-lookup"><span data-stu-id="6cf80-137">ITfContext::RequestEditSession</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcontext-requesteditsession)
</dt> </dl>

 

 





