---
description: Il metodo SetBandwidthInfo imposta le informazioni sulla larghezza di banda.
ms.assetid: bf5db456-ea67-4a65-a681-df0741f73fc9
title: 'Metodo ITConnection:: SetBandwidthInfo (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c17054743f6d47775e994dbfe3b80c7afe1ab68
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326495"
---
# <a name="itconnectionsetbandwidthinfo-method"></a><span data-ttu-id="4137f-103">Metodo ITConnection:: SetBandwidthInfo</span><span class="sxs-lookup"><span data-stu-id="4137f-103">ITConnection::SetBandwidthInfo method</span></span>

<span data-ttu-id="4137f-104">\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="4137f-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="4137f-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="4137f-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="4137f-106">Il metodo **SetBandwidthInfo** imposta le informazioni sulla larghezza di banda.</span><span class="sxs-lookup"><span data-stu-id="4137f-106">The **SetBandwidthInfo** method sets the bandwidth information.</span></span>

## <a name="syntax"></a><span data-ttu-id="4137f-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4137f-107">Syntax</span></span>


```C++
HRESULT SetBandwidthInfo(
  [in] BSTR   pModifier,
  [in] DOUBLE Bandwidth
);
```



## <a name="parameters"></a><span data-ttu-id="4137f-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="4137f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4137f-109">*pModifier* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4137f-109">*pModifier* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4137f-110">Puntatore a un **BSTR** che indica l'ambito della larghezza di banda da impostare.</span><span class="sxs-lookup"><span data-stu-id="4137f-110">Pointer to a **BSTR** indicating the scope of the bandwidth being set.</span></span> <span data-ttu-id="4137f-111">Per ulteriori informazioni, vedere la sezione Osservazioni successiva.</span><span class="sxs-lookup"><span data-stu-id="4137f-111">For more information, see the following Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="4137f-112">*Larghezza di banda* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4137f-112">*Bandwidth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4137f-113">Banda.</span><span class="sxs-lookup"><span data-stu-id="4137f-113">Bandwidth.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4137f-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4137f-114">Return value</span></span>

<span data-ttu-id="4137f-115">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="4137f-115">This method can return one of these values.</span></span>



| <span data-ttu-id="4137f-116">Valore</span><span class="sxs-lookup"><span data-stu-id="4137f-116">Value</span></span>                                                                                         | <span data-ttu-id="4137f-117">Significato</span><span class="sxs-lookup"><span data-stu-id="4137f-117">Meaning</span></span>                                                           |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| <dl> <span data-ttu-id="4137f-118"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="4137f-118"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="4137f-119">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="4137f-119">Method succeeded.</span></span><br/>                                      |
| <dl> <span data-ttu-id="4137f-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="4137f-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="4137f-121">Il parametro *pModifier* o *Bandwidth* non è valido.</span><span class="sxs-lookup"><span data-stu-id="4137f-121">The *pModifier* or *Bandwidth* parameter is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="4137f-122"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="4137f-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="4137f-123">La memoria disponibile non è sufficiente per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="4137f-123">Insufficient memory exists to perform the operation.</span></span><br/>   |
| <dl> <span data-ttu-id="4137f-124"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="4137f-124"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="4137f-125">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="4137f-125">Unspecified error.</span></span><br/>                                     |
| <dl> <span data-ttu-id="4137f-126"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="4137f-126"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="4137f-127">Questo metodo non è ancora implementato.</span><span class="sxs-lookup"><span data-stu-id="4137f-127">This method is not yet implemented.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="4137f-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="4137f-128">Remarks</span></span>

<span data-ttu-id="4137f-129">L'applicazione deve usare [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) per allocare memoria per il parametro *PModifier* e usare [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) per liberare la memoria quando la variabile non è più necessaria.</span><span class="sxs-lookup"><span data-stu-id="4137f-129">The application must use [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) to allocate memory for the *pModifier* parameter and use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory when the variable is no longer needed.</span></span>

<span data-ttu-id="4137f-130">Riferimento: RFC 2327.</span><span class="sxs-lookup"><span data-stu-id="4137f-130">Reference: RFC 2327.</span></span>

<span data-ttu-id="4137f-131">Il modificatore della larghezza di banda sarà in genere CT o come:</span><span class="sxs-lookup"><span data-stu-id="4137f-131">The bandwidth modifier will normally be either CT or AS:</span></span>

<span data-ttu-id="4137f-132">**Totale conferenza CT:** Una larghezza di banda massima implicita è associata a ogni durata (TTL) in MBone o all'interno di una particolare area dell'ambito amministrativo multicast (i limiti della larghezza [*di*](t-tapgloss.md) banda di MBone rispetto a quelli TTL sono indicati nelle domande frequenti su MBone).</span><span class="sxs-lookup"><span data-stu-id="4137f-132">**CT Conference Total:** An implicit maximum bandwidth is associated with each [*time to live*](t-tapgloss.md) (TTL) on the Mbone or within a particular multicast administrative scope region (the Mbone bandwidth versus TTL limits are given in the MBone FAQ).</span></span> <span data-ttu-id="4137f-133">Se la larghezza di banda di una sessione o di un supporto in una sessione è diversa dalla larghezza di banda implicita dall'ambito, a \` b = CT:.. .' la riga deve essere fornita per la sessione, assegnando il limite superiore proposto alla larghezza di banda usata.</span><span class="sxs-lookup"><span data-stu-id="4137f-133">If the bandwidth of a session or media in a session is different from the bandwidth implicit from the scope, a \`b=CT:...' line should be supplied for the session giving the proposed upper limit to the bandwidth used.</span></span> <span data-ttu-id="4137f-134">Lo scopo principale di questa operazione è fornire un'idea approssimativa del modo in cui due o più conferenze possono coesistere simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="4137f-134">The primary purpose of this is to give an approximate idea as to whether two or more conferences can coexist simultaneously.</span></span>

<span data-ttu-id="4137f-135">**Come Application-Specific massimo:** La larghezza di banda viene interpretata come specifica dell'applicazione, ad esempio, sarà il concetto di larghezza di banda massima dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="4137f-135">**AS Application-Specific Maximum:** The bandwidth is interpreted to be application-specific, i.e., will be the application's concept of maximum bandwidth.</span></span> <span data-ttu-id="4137f-136">Normalmente questo coincide con quello impostato sul controllo "larghezza di banda massima" dell'applicazione, se applicabile.</span><span class="sxs-lookup"><span data-stu-id="4137f-136">Normally this will coincide with what is set on the application's "maximum bandwidth" control, if applicable.</span></span>

<span data-ttu-id="4137f-137">Si noti che CT fornisce una cifra della larghezza di banda totale per tutti i supporti in tutti i siti.</span><span class="sxs-lookup"><span data-stu-id="4137f-137">Note that CT gives a total bandwidth figure for all the media at all sites.</span></span> <span data-ttu-id="4137f-138">Come fornisce una quantità di larghezza di banda per un singolo supporto in un singolo sito, anche se possono essere presenti più siti che inviano simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="4137f-138">AS gives a bandwidth figure for a single media at a single site, although there may be many sites sending simultaneously.</span></span>

<span data-ttu-id="4137f-139">**Meccanismo di estensione:** I writer di strumenti possono definire modificatori della larghezza di banda sperimentali anteponendo i modificatori con "X-".</span><span class="sxs-lookup"><span data-stu-id="4137f-139">**Extension Mechanism:** Tool writers can define experimental bandwidth modifiers by prefixing their modifiers with "X-".</span></span>

## <a name="requirements"></a><span data-ttu-id="4137f-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4137f-140">Requirements</span></span>



| <span data-ttu-id="4137f-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="4137f-141">Requirement</span></span> | <span data-ttu-id="4137f-142">Valore</span><span class="sxs-lookup"><span data-stu-id="4137f-142">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4137f-143">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="4137f-143">TAPI version</span></span><br/> | <span data-ttu-id="4137f-144">Richiede TAPI 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="4137f-144">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="4137f-145">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4137f-145">Header</span></span><br/>       | <dl> <span data-ttu-id="4137f-146"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="4137f-146"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="4137f-147">Libreria</span><span class="sxs-lookup"><span data-stu-id="4137f-147">Library</span></span><br/>      | <dl> <span data-ttu-id="4137f-148"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4137f-148"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="4137f-149">DLL</span><span class="sxs-lookup"><span data-stu-id="4137f-149">DLL</span></span><br/>          | <dl> <span data-ttu-id="4137f-150"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4137f-150"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4137f-151">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4137f-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4137f-152">**ITConnection**</span><span class="sxs-lookup"><span data-stu-id="4137f-152">**ITConnection**</span></span>](itconnection.md)
</dt> </dl>

 

