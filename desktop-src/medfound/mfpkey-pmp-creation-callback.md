---
description: Imposta un callback che crea la sessione multimediale PMP durante la risoluzione dell'origine.
ms.assetid: 7277C5E0-BB91-4EEA-9529-64E66D179CDC
title: Proprietà MFPKEY_PMP_Creation_Callback (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2b18e04a15e035a9e4dc04a4039ce230342031a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226996"
---
# <a name="mfpkey_pmp_creation_callback-property"></a><span data-ttu-id="172de-103">Proprietà di callback per la \_ creazione di MFPKEY PMP \_ \_</span><span class="sxs-lookup"><span data-stu-id="172de-103">MFPKEY\_PMP\_Creation\_Callback property</span></span>

<span data-ttu-id="172de-104">Imposta un callback che crea la [sessione multimediale PMP](pmp-media-session.md) durante la risoluzione dell'origine.</span><span class="sxs-lookup"><span data-stu-id="172de-104">Sets a callback that creates the [PMP Media Session](pmp-media-session.md) during source resolution.</span></span>



<span data-ttu-id="172de-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="172de-105">Data type</span></span>

<span data-ttu-id="172de-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="172de-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="172de-107">membro PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="172de-107">PROPVARIANT member</span></span>

<span data-ttu-id="172de-108">\**IUnknown \** _</span><span class="sxs-lookup"><span data-stu-id="172de-108">\**IUnknown\** _</span></span>

<span data-ttu-id="172de-109">VT \_ sconosciuto</span><span class="sxs-lookup"><span data-stu-id="172de-109">VT\_UNKNOWN</span></span>

<span data-ttu-id="172de-110">_ *punkVal*\*</span><span class="sxs-lookup"><span data-stu-id="172de-110">_ *punkVal*\*</span></span>



## <a name="remarks"></a><span data-ttu-id="172de-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="172de-111">Remarks</span></span>

<span data-ttu-id="172de-112">Alcuni contenuti protetti potrebbero richiedere l'uso di questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="172de-112">Some protected content might require the use of this property.</span></span> <span data-ttu-id="172de-113">In tal caso, il processo di risoluzione dell'origine ha esito negativo con il codice di errore **MF \_ E la \_ risoluzione \_ richiede il \_ \_ \_ callback di creazione PMP**.</span><span class="sxs-lookup"><span data-stu-id="172de-113">If so, the source resolution process fails with the error code **MF\_E\_RESOLUTION\_REQUIRES\_PMP\_CREATION\_CALLBACK**.</span></span>

<span data-ttu-id="172de-114">Per usare questa proprietà, eseguire le operazioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="172de-114">To use this property, do the following.</span></span>

1.  <span data-ttu-id="172de-115">Chiamare [**PSCreateMemoryPropertyStore**](/windows/win32/api/propsys/nf-propsys-pscreatememorypropertystore) per creare un archivio delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="172de-115">Call [**PSCreateMemoryPropertyStore**](/windows/win32/api/propsys/nf-propsys-pscreatememorypropertystore) to create a property store.</span></span>
2.  <span data-ttu-id="172de-116">Implementare l'interfaccia di callback [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) .</span><span class="sxs-lookup"><span data-stu-id="172de-116">Implement the [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) callback interface.</span></span>
3.  <span data-ttu-id="172de-117">Impostare la \_ \_ \_ proprietà di callback per la creazione di MFPKEY PMP nell'archivio delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="172de-117">Set the MFPKEY\_PMP\_Creation\_Callback property on the property store.</span></span> <span data-ttu-id="172de-118">Il valore è un puntatore all'implementazione di [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) .</span><span class="sxs-lookup"><span data-stu-id="172de-118">The value is a pointer to the [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) implementation.</span></span>
4.  <span data-ttu-id="172de-119">Chiamare [**IMFSourceResolver:: BeginCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl).</span><span class="sxs-lookup"><span data-stu-id="172de-119">Call [**IMFSourceResolver::BeginCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl).</span></span> <span data-ttu-id="172de-120">Passare un puntatore all'archivio delle proprietà nel parametro *pProps* .</span><span class="sxs-lookup"><span data-stu-id="172de-120">Pass in a pointer to the property store in the *pProps* parameter.</span></span>

<span data-ttu-id="172de-121">Nel metodo [**IMFAsyncCallback:: Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) dell'interfaccia di callback eseguire le operazioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="172de-121">In the [**IMFAsyncCallback::Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) method of your callback interface, do the following.</span></span>

1.  <span data-ttu-id="172de-122">Chiamare [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) per creare la [sessione multimediale PMP](pmp-media-session.md).</span><span class="sxs-lookup"><span data-stu-id="172de-122">Call [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) to create the [PMP Media Session](pmp-media-session.md).</span></span>
2.  <span data-ttu-id="172de-123">Chiamare [**IMFGetService:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) sulla sessione multimediale PMP in un puntatore all'interfaccia [**IMFPMPHost**](/windows/desktop/api/mfidl/nn-mfidl-imfpmphost) .</span><span class="sxs-lookup"><span data-stu-id="172de-123">Call [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) on the PMP Media Session to a pointer to the [**IMFPMPHost**](/windows/desktop/api/mfidl/nn-mfidl-imfpmphost) interface.</span></span>
3.  <span data-ttu-id="172de-124">Chiamare [**IMFAsyncResult:: GetState**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getstate) sull'oggetto risultato passato nel parametro *pAsyncResult* di [**IMFAsyncCallback:: Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke).</span><span class="sxs-lookup"><span data-stu-id="172de-124">Call [**IMFAsyncResult::GetState**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getstate) on the result object that is passed in the *pAsyncResult* parameter of [**IMFAsyncCallback::Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke).</span></span> <span data-ttu-id="172de-125">Eseguire una query sul puntatore [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) restituito per l'interfaccia [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) .</span><span class="sxs-lookup"><span data-stu-id="172de-125">Query the returned [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) pointer for the [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) interface.</span></span>
4.  <span data-ttu-id="172de-126">Chiamare [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) con i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="172de-126">Call [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) with the following parameters:</span></span>
    -   <span data-ttu-id="172de-127">*dwQueue*: **MFASYNC \_ coda di callback \_ \_ standard**</span><span class="sxs-lookup"><span data-stu-id="172de-127">*dwQueue*: **MFASYNC\_CALLBACK\_QUEUE\_STANDARD**</span></span>
    -   <span data-ttu-id="172de-128">*pCallback*: puntatore [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) ottenuto nel passaggio 3.</span><span class="sxs-lookup"><span data-stu-id="172de-128">*pCallback*: The [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) pointer obtained in step 3.</span></span>
    -   <span data-ttu-id="172de-129">*pState*: puntatore [**IMFPMPHost**](/windows/desktop/api/mfidl/nn-mfidl-imfpmphost) ottenuto nel passaggio 2.</span><span class="sxs-lookup"><span data-stu-id="172de-129">*pState*: The [**IMFPMPHost**](/windows/desktop/api/mfidl/nn-mfidl-imfpmphost) pointer obtained in step 2.</span></span>

## <a name="requirements"></a><span data-ttu-id="172de-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="172de-130">Requirements</span></span>



| <span data-ttu-id="172de-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="172de-131">Requirement</span></span> | <span data-ttu-id="172de-132">Valore</span><span class="sxs-lookup"><span data-stu-id="172de-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="172de-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="172de-133">Minimum supported client</span></span><br/> | <span data-ttu-id="172de-134">App desktop di Windows 8 app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="172de-134">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="172de-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="172de-135">Minimum supported server</span></span><br/> | <span data-ttu-id="172de-136">App UWP per \[ app desktop di Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="172de-136">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="172de-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="172de-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="172de-138"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="172de-138"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="172de-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="172de-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="172de-140">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="172de-140">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="172de-141">Sessione multimediale PMP</span><span class="sxs-lookup"><span data-stu-id="172de-141">PMP Media Session</span></span>](pmp-media-session.md)
</dt> <dt>

[<span data-ttu-id="172de-142">Percorso supporto protetto</span><span class="sxs-lookup"><span data-stu-id="172de-142">Protected Media Path</span></span>](protected-media-path.md)
</dt> <dt>

[<span data-ttu-id="172de-143">Resolver di origine</span><span class="sxs-lookup"><span data-stu-id="172de-143">Source Resolver</span></span>](source-resolver.md)
</dt> </dl>

 

 
