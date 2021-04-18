---
title: Metodo IWMDRMSecurity PerformSecurityUpdate (wmdrmsdk. h)
description: Il metodo PerformSecurityUpdate avvia un aggiornamento della sicurezza per il sottosistema DRM nel computer locale.
ms.assetid: e450a1e3-6024-4c00-9978-fbc88fde2101
keywords:
- Metodo PerformSecurityUpdate Windows Media Format
- Metodo PerformSecurityUpdate Windows Media Format, interfaccia IWMDRMSecurity
- Interfaccia IWMDRMSecurity-formato Windows Media, metodo PerformSecurityUpdate
topic_type:
- apiref
api_name:
- IWMDRMSecurity.PerformSecurityUpdate
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a34a1e92edd279655737a2e8f3b7ce4e77e27fd5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325535"
---
# <a name="iwmdrmsecurityperformsecurityupdate-method"></a><span data-ttu-id="e7217-106">IWMDRMSecurity::P metodo erformSecurityUpdate</span><span class="sxs-lookup"><span data-stu-id="e7217-106">IWMDRMSecurity::PerformSecurityUpdate method</span></span>

<span data-ttu-id="e7217-107">Il metodo **PerformSecurityUpdate** avvia un aggiornamento della sicurezza per il sottosistema DRM nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="e7217-107">The **PerformSecurityUpdate** method initiates a security update to the DRM subsystem on the local computer.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7217-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e7217-108">Syntax</span></span>


```C++
HRESULT PerformSecurityUpdate(
  [in]  DWORD    dwFlags,
  [out] IUnknown **ppunkCancelationCookie
);
```



## <a name="parameters"></a><span data-ttu-id="e7217-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="e7217-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7217-110">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e7217-110">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7217-111">Opzione di aggiornamento espressa come uno dei flag seguenti.</span><span class="sxs-lookup"><span data-stu-id="e7217-111">Update option expressed as one of the following flags.</span></span>



| <span data-ttu-id="e7217-112">Flag</span><span class="sxs-lookup"><span data-stu-id="e7217-112">Flag</span></span>                                          | <span data-ttu-id="e7217-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e7217-113">Description</span></span>                                                                                     |
|-----------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7217-114">sicurezza di WMDRM \_ \_ eseguire \_ indiv</span><span class="sxs-lookup"><span data-stu-id="e7217-114">WMDRM\_SECURITY\_PERFORM\_INDIV</span></span>               | <span data-ttu-id="e7217-115">Fa in modo che il componente DRM venga individualizzato solo se la versione del client non è aggiornata.</span><span class="sxs-lookup"><span data-stu-id="e7217-115">Causes the DRM component to be individualized only if the version of the client is out of date.</span></span> |
| <span data-ttu-id="e7217-116">\_sicurezza WMDRM \_ eseguire l' \_ aggiornamento delle revoche \_</span><span class="sxs-lookup"><span data-stu-id="e7217-116">WMDRM\_SECURITY\_PERFORM\_REVOCATION\_REFRESH</span></span> | <span data-ttu-id="e7217-117">Causa l'aggiornamento degli elenchi di revoche nel computer client.</span><span class="sxs-lookup"><span data-stu-id="e7217-117">Causes the revocation lists on the client computer to be updated.</span></span>                               |
| <span data-ttu-id="e7217-118">WMDRM \_ Security \_ esegue \_ Force \_ indiv</span><span class="sxs-lookup"><span data-stu-id="e7217-118">WMDRM\_SECURITY\_PERFORM\_FORCE\_INDIV</span></span>        | <span data-ttu-id="e7217-119">Fa in modo che il componente DRM venga individualizzato anche se la versione del client è aggiornata.</span><span class="sxs-lookup"><span data-stu-id="e7217-119">Causes the DRM component to be individualized even if the version of the client is up to date.</span></span>  |



 

</dd> <dt>

<span data-ttu-id="e7217-120">*ppunkCancelationCookie* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="e7217-120">*ppunkCancelationCookie* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e7217-121">Indirizzo di una variabile che riceve un puntatore a un oggetto che può essere utilizzato per annullare questa operazione.</span><span class="sxs-lookup"><span data-stu-id="e7217-121">Address of a variable that receives a pointer to an object that can be used to cancel this operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7217-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e7217-122">Return value</span></span>

<span data-ttu-id="e7217-123">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="e7217-123">The method returns an **HRESULT**.</span></span> <span data-ttu-id="e7217-124">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="e7217-124">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="e7217-125">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="e7217-125">Return code</span></span>                                                                          | <span data-ttu-id="e7217-126">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e7217-126">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="e7217-127"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e7217-127"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="e7217-128">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="e7217-128">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e7217-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="e7217-129">Remarks</span></span>

<span data-ttu-id="e7217-130">Questo metodo viene eseguito in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="e7217-130">This method executes asynchronously.</span></span> <span data-ttu-id="e7217-131">Viene restituito immediatamente dopo la chiamata di e quindi genera eventi a seconda del flag impostato nel parametro *dwFlags* .</span><span class="sxs-lookup"><span data-stu-id="e7217-131">It returns immediately after being called and then generates events depending on the flag set in the *dwFlags* parameter.</span></span>

<span data-ttu-id="e7217-132">Per l'individualizzazione (flag impostato su WMDRM \_ Security eseguire \_ \_ indiv o WMDRM \_ Security \_ Esegui \_ Force \_ indiv), una serie di eventi **MEWMDRMIndividualizationProgress** viene generata seguito da un evento **MEWMDRMIndividualizationCompleted** al termine dell'elaborazione.</span><span class="sxs-lookup"><span data-stu-id="e7217-132">For individualization (flag set to WMDRM\_SECURITY\_PERFORM\_INDIV or WMDRM\_SECURITY\_PERFORM\_FORCE\_INDIV), a series of **MEWMDRMIndividualizationProgress** events is generated followed by an **MEWMDRMIndividualizationCompleted** event when processing is complete.</span></span> <span data-ttu-id="e7217-133">Il valore di ogni evento **MEWMDRMIndividualizationProgress** ottenuto chiamando **IMFMediaEvent:: GetValue** è un puntatore **IUnknown** .</span><span class="sxs-lookup"><span data-stu-id="e7217-133">The value of each of the **MEWMDRMIndividualizationProgress** events obtained by calling **IMFMediaEvent::GetValue** is an **IUnknown** pointer.</span></span> <span data-ttu-id="e7217-134">È possibile chiamare il metodo **QueryInterface** dell'interfaccia **IUnknown** recuperata per ottenere un'istanza dell'interfaccia [**IWMDRMIndividualizationStatus**](iwmdrmindividualizationstatus.md) .</span><span class="sxs-lookup"><span data-stu-id="e7217-134">You can call the **QueryInterface** method of the retrieved **IUnknown** interface to get an instance of the [**IWMDRMIndividualizationStatus**](iwmdrmindividualizationstatus.md) interface.</span></span>

<span data-ttu-id="e7217-135">Per aggiornare gli elenchi di revoche (flag impostato su WMDRM \_ Security \_ eseguire l' \_ aggiornamento delle revoche \_ ), viene generato un evento **MEWMDRMREvocationDownloadCompleted** al termine dell'elaborazione.</span><span class="sxs-lookup"><span data-stu-id="e7217-135">For refreshing the revocation lists (flag set to WMDRM\_SECURITY\_PERFORM\_REVOCATION\_REFRESH), an **MEWMDRMREvocationDownloadCompleted** event is generated when processing is complete.</span></span>

> [!Note]  
> <span data-ttu-id="e7217-136">Quando **PerformSecurityUpdate** completa l'individualizzazione, gli unici oggetti esistenti che riflettono il nuovo stato individualizzato sono quelli che ereditano da **IWMDRMSecurity**.</span><span class="sxs-lookup"><span data-stu-id="e7217-136">When **PerformSecurityUpdate** completes individualization, the only existing objects that will reflect the new individualized state are those that inherit from **IWMDRMSecurity**.</span></span> <span data-ttu-id="e7217-137">Tutti gli altri oggetti esistenti non verranno aggiornati.</span><span class="sxs-lookup"><span data-stu-id="e7217-137">All other existing objects will not be updated.</span></span> <span data-ttu-id="e7217-138">È necessario rilasciare e ricreare altri oggetti in modo che riflettano il nuovo stato individualizzato.</span><span class="sxs-lookup"><span data-stu-id="e7217-138">You must release and re-create any other objects so that they will reflect the new individualized state.</span></span>

 

<span data-ttu-id="e7217-139">Per ulteriori informazioni sull'utilizzo dei metodi asincroni delle API estese del client Windows Media DRM, vedere [utilizzo del modello di eventi Media Foundation](using-the-media-foundation-model.md).</span><span class="sxs-lookup"><span data-stu-id="e7217-139">For more information about using the asynchronous methods of the Windows Media DRM Client Extended APIs, see [Using the Media Foundation Event Model](using-the-media-foundation-model.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e7217-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e7217-140">Requirements</span></span>



| <span data-ttu-id="e7217-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="e7217-141">Requirement</span></span> | <span data-ttu-id="e7217-142">Valore</span><span class="sxs-lookup"><span data-stu-id="e7217-142">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e7217-143">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e7217-143">Header</span></span><br/>  | <dl> <span data-ttu-id="e7217-144"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="e7217-144"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="e7217-145">Libreria</span><span class="sxs-lookup"><span data-stu-id="e7217-145">Library</span></span><br/> | <dl> <span data-ttu-id="e7217-146"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e7217-146"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7217-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e7217-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7217-148">**Revoca e rinnovo automatici dei componenti**</span><span class="sxs-lookup"><span data-stu-id="e7217-148">**Automated Component Revocation and Renewal**</span></span>](automated-component-revocation-and-renewal.md)
</dt> <dt>

[<span data-ttu-id="e7217-149">**Esempio di individualizzazione DRM**</span><span class="sxs-lookup"><span data-stu-id="e7217-149">**DRM Individualization Example**</span></span>](drm-individualization-example.md)
</dt> <dt>

[<span data-ttu-id="e7217-150">**Interfaccia IWMDRMSecurity**</span><span class="sxs-lookup"><span data-stu-id="e7217-150">**IWMDRMSecurity Interface**</span></span>](iwmdrmsecurity.md)
</dt> <dt>

[<span data-ttu-id="e7217-151">**Esecuzione dell'individualizzazione DRM**</span><span class="sxs-lookup"><span data-stu-id="e7217-151">**Performing DRM Individualization**</span></span>](performing-drm-individualization.md)
</dt> </dl>

 

 





