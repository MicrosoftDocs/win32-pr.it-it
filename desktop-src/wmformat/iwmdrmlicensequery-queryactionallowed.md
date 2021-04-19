---
title: Metodo IWMDRMLicenseQuery QueryActionAllowed (wmdrmsdk. h)
description: Il metodo QueryActionAllowed esegue una query sull'archivio licenze locale per recuperare lo stato della licenza per una o più azioni DRM applicabili a un ID chiave specificato.
ms.assetid: 814c2850-c036-4c44-a64e-861e88f16fb1
keywords:
- Metodo QueryActionAllowed Windows Media Format
- Metodo QueryActionAllowed Windows Media Format, interfaccia IWMDRMLicenseQuery
- Interfaccia IWMDRMLicenseQuery-formato Windows Media, metodo QueryActionAllowed
topic_type:
- apiref
api_name:
- IWMDRMLicenseQuery.QueryActionAllowed
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6564062fc9f76a840b37f6e134e960480d67a2ee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329269"
---
# <a name="iwmdrmlicensequeryqueryactionallowed-method"></a><span data-ttu-id="3dd7b-106">Metodo IWMDRMLicenseQuery:: QueryActionAllowed</span><span class="sxs-lookup"><span data-stu-id="3dd7b-106">IWMDRMLicenseQuery::QueryActionAllowed method</span></span>

<span data-ttu-id="3dd7b-107">Il metodo **QueryActionAllowed** esegue una query sull'archivio licenze locale per recuperare lo stato della licenza per una o più azioni DRM applicabili a un ID chiave specificato.</span><span class="sxs-lookup"><span data-stu-id="3dd7b-107">The **QueryActionAllowed** method performs a query on the local license store to retrieve the license status for one or more DRM actions that apply to a specified Key ID.</span></span>

## <a name="syntax"></a><span data-ttu-id="3dd7b-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3dd7b-108">Syntax</span></span>


```C++
HRESULT QueryActionAllowed(
  [in]  BSTR  bstrKID,
  [in]  BSTR  bstrMinReqIndivVersion,
  [in]  DWORD cActionsToQuery,
  [in]  BSTR  rgbstrActionsToQuery[],
  [out] DWORD rgdwQueryResult[]
);
```



## <a name="parameters"></a><span data-ttu-id="3dd7b-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="3dd7b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3dd7b-110">*bstrKID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3dd7b-110">*bstrKID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3dd7b-111">ID chiave per cui eseguire una query.</span><span class="sxs-lookup"><span data-stu-id="3dd7b-111">Key ID for which to query.</span></span> <span data-ttu-id="3dd7b-112">Verranno valutate solo le licenze che si applicano a questo ID chiave.</span><span class="sxs-lookup"><span data-stu-id="3dd7b-112">Only licenses that apply to this Key ID will be evaluated.</span></span>

</dd> <dt>

<span data-ttu-id="3dd7b-113">*bstrMinReqIndivVersion* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3dd7b-113">*bstrMinReqIndivVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3dd7b-114">Versione di sicurezza minima specificata nell'intestazione del file ASF.</span><span class="sxs-lookup"><span data-stu-id="3dd7b-114">The minimum security version specified in the header of the ASF file.</span></span> <span data-ttu-id="3dd7b-115">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="3dd7b-115">This parameter is optional.</span></span> <span data-ttu-id="3dd7b-116">Passare **null** per eseguire la query senza queste informazioni.</span><span class="sxs-lookup"><span data-stu-id="3dd7b-116">Pass **NULL** to perform the query without this information.</span></span>

</dd> <dt>

<span data-ttu-id="3dd7b-117">*cActionsToQuery* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3dd7b-117">*cActionsToQuery* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3dd7b-118">Il numero di azioni per cui eseguire una query.</span><span class="sxs-lookup"><span data-stu-id="3dd7b-118">The number of actions for which to query.</span></span> <span data-ttu-id="3dd7b-119">Questo valore deve essere impostato sul numero di elementi nelle matrici passate per i parametri *rgbstrActionsToQuery* e *rgdwQueryResult* .</span><span class="sxs-lookup"><span data-stu-id="3dd7b-119">This value must be set to the number of elements in the arrays passed for the *rgbstrActionsToQuery* and *rgdwQueryResult* parameters.</span></span>

</dd> <dt>

<span data-ttu-id="3dd7b-120">*\[ rgbstrActionsToQuery \]* \[in\]</span><span class="sxs-lookup"><span data-stu-id="3dd7b-120">*rgbstrActionsToQuery\[\]* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3dd7b-121">Matrice di uno o più diritti per i quali eseguire una query.</span><span class="sxs-lookup"><span data-stu-id="3dd7b-121">Array of one or more rights for which to query.</span></span> <span data-ttu-id="3dd7b-122">Questa matrice deve contenere il numero di elementi specificato da *cActionsToQuery*.</span><span class="sxs-lookup"><span data-stu-id="3dd7b-122">This array must contain as many elements as specified by *cActionsToQuery*.</span></span> <span data-ttu-id="3dd7b-123">Ogni elemento deve essere impostato su una delle seguenti costanti:</span><span class="sxs-lookup"><span data-stu-id="3dd7b-123">Each element must be set to one of the following constants:</span></span>



| <span data-ttu-id="3dd7b-124">Costante</span><span class="sxs-lookup"><span data-stu-id="3dd7b-124">Constant</span></span>                                         | <span data-ttu-id="3dd7b-125">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3dd7b-125">Description</span></span>                                                                      |
|--------------------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="3dd7b-126">\_ \_ riproduzione ActionAllowed g \_ wszWMDRM</span><span class="sxs-lookup"><span data-stu-id="3dd7b-126">g\_wszWMDRM\_ActionAllowed\_Playback</span></span>             | <span data-ttu-id="3dd7b-127">Includere per eseguire una query per il diritto di riprodurre il contenuto.</span><span class="sxs-lookup"><span data-stu-id="3dd7b-127">Include to query for the right to play the content.</span></span>                              |
| <span data-ttu-id="3dd7b-128">g \_ wszWMDRM \_ ActionAllowed \_ Copy</span><span class="sxs-lookup"><span data-stu-id="3dd7b-128">g\_wszWMDRM\_ActionAllowed\_Copy</span></span>                 | <span data-ttu-id="3dd7b-129">Includere per eseguire una query per il diritto di copiare il contenuto in dispositivi esterni o supporti.</span><span class="sxs-lookup"><span data-stu-id="3dd7b-129">Include to query for the right to copy the content to external devices or media.</span></span> |
| <span data-ttu-id="3dd7b-130">g \_ wszWMDRM \_ ActionAllowed \_ PlaylistBurn</span><span class="sxs-lookup"><span data-stu-id="3dd7b-130">g\_wszWMDRM\_ActionAllowed\_PlaylistBurn</span></span>         | <span data-ttu-id="3dd7b-131">Includere per eseguire una query per il diritto di copiare il contenuto in CD come parte di una playlist.</span><span class="sxs-lookup"><span data-stu-id="3dd7b-131">Include to query for the right to copy the content to CD as part of a playlist.</span></span>  |
| <span data-ttu-id="3dd7b-132">g \_ wszWMDRM \_ ActionAllowed \_ CreateThumbnailImage</span><span class="sxs-lookup"><span data-stu-id="3dd7b-132">g\_wszWMDRM\_ActionAllowed\_CreateThumbnailImage</span></span> | <span data-ttu-id="3dd7b-133">Includere per eseguire una query per il diritto di creare un'immagine di anteprima dal contenuto.</span><span class="sxs-lookup"><span data-stu-id="3dd7b-133">Include to query for the right to create a thumbnail image from the content.</span></span>     |
| <span data-ttu-id="3dd7b-134">g \_ wszWMDRM \_ ActionAllowed \_ CopyToCD</span><span class="sxs-lookup"><span data-stu-id="3dd7b-134">g\_wszWMDRM\_ActionAllowed\_CopyToCD</span></span>             | <span data-ttu-id="3dd7b-135">Includere per eseguire una query per il diritto di copiare il contenuto in CD.</span><span class="sxs-lookup"><span data-stu-id="3dd7b-135">Include to query for the right to copy the content to CD.</span></span>                        |



 

</dd> <dt>

<span data-ttu-id="3dd7b-136">*\[ rgdwQueryResult \]* in \[ uscita\]</span><span class="sxs-lookup"><span data-stu-id="3dd7b-136">*rgdwQueryResult\[\]* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3dd7b-137">Matrice di una o più variabili DWORD che ricevono i risultati della query per i diritti specificati da *rgbstrActionsToQuery*.</span><span class="sxs-lookup"><span data-stu-id="3dd7b-137">Array of one or more DWORD variables that receive the results of the query for the rights specified by *rgbstrActionsToQuery*.</span></span> <span data-ttu-id="3dd7b-138">Se è consentita un'azione, l'elemento corrispondente viene impostato su zero.</span><span class="sxs-lookup"><span data-stu-id="3dd7b-138">If an action is allowed, the corresponding element is set to zero.</span></span> <span data-ttu-id="3dd7b-139">Se un'azione non è consentita, l'elemento viene impostato su uno o più valori dell'enumerazione dei [**\_ \_ \_ \_ risultati delle query consentiti dell'azione DRM**](drm-action-allowed-query-results.md) combinati tramite l'operazione OR bit per bit.</span><span class="sxs-lookup"><span data-stu-id="3dd7b-139">If an action is not allowed, the element is set to one or more values of the [**DRM\_ACTION\_ALLOWED\_QUERY\_RESULTS**](drm-action-allowed-query-results.md) enumeration combined by using the bitwise OR operation.</span></span> <span data-ttu-id="3dd7b-140">Questa matrice deve contenere il numero di elementi specificato da *cActionsToQuery*.</span><span class="sxs-lookup"><span data-stu-id="3dd7b-140">This array must contain as many elements as specified by *cActionsToQuery*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3dd7b-141">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3dd7b-141">Return value</span></span>

<span data-ttu-id="3dd7b-142">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="3dd7b-142">The method returns an **HRESULT**.</span></span> <span data-ttu-id="3dd7b-143">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="3dd7b-143">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="3dd7b-144">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="3dd7b-144">Return code</span></span>                                                                          | <span data-ttu-id="3dd7b-145">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3dd7b-145">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="3dd7b-146"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="3dd7b-146"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="3dd7b-147">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="3dd7b-147">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3dd7b-148">Commenti</span><span class="sxs-lookup"><span data-stu-id="3dd7b-148">Remarks</span></span>

<span data-ttu-id="3dd7b-149">Quando si eseguono query sui diritti di riproduzione e copia, si otterranno risultati più accurati impostando prima i parametri ambientali.</span><span class="sxs-lookup"><span data-stu-id="3dd7b-149">When querying for play and copy rights, you will get more accurate results by first setting environmental parameters.</span></span> <span data-ttu-id="3dd7b-150">Usare il metodo [**SetActionAllowedQueryParams**](iwmdrmlicensequery-setactionallowedqueryparams.md) per impostare i parametri ambientali.</span><span class="sxs-lookup"><span data-stu-id="3dd7b-150">Use the [**SetActionAllowedQueryParams**](iwmdrmlicensequery-setactionallowedqueryparams.md) method to set the environmental parameters.</span></span> <span data-ttu-id="3dd7b-151">I risultati delle query per il diritto Burn non sono interessati dai parametri ambientali; è possibile usare in modo sicuro le impostazioni predefinite.</span><span class="sxs-lookup"><span data-stu-id="3dd7b-151">The results of queries for the burn right are unaffected by the environmental parameters; you can safely use the defaults.</span></span>

<span data-ttu-id="3dd7b-152">I risultati restituiti dal metodo **QueryActionAllowed** sono aggregati da zero o più licenze nell'archivio licenze locale.</span><span class="sxs-lookup"><span data-stu-id="3dd7b-152">The results returned by the **QueryActionAllowed** method are aggregated from zero or more licenses in the local license store.</span></span> <span data-ttu-id="3dd7b-153">Il metodo non può eseguire ricerche in tutte le licenze valide per l'ID chiave se viene rilevato un risultato abilitato.</span><span class="sxs-lookup"><span data-stu-id="3dd7b-153">The method may not search all of the licenses that apply to the Key ID if it encounters an enabled result.</span></span>

## <a name="requirements"></a><span data-ttu-id="3dd7b-154">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3dd7b-154">Requirements</span></span>



| <span data-ttu-id="3dd7b-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="3dd7b-155">Requirement</span></span> | <span data-ttu-id="3dd7b-156">Valore</span><span class="sxs-lookup"><span data-stu-id="3dd7b-156">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3dd7b-157">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3dd7b-157">Header</span></span><br/>  | <dl> <span data-ttu-id="3dd7b-158"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="3dd7b-158"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="3dd7b-159">Libreria</span><span class="sxs-lookup"><span data-stu-id="3dd7b-159">Library</span></span><br/> | <dl> <span data-ttu-id="3dd7b-160"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3dd7b-160"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3dd7b-161">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3dd7b-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3dd7b-162">**Interfaccia IWMDRMLicenseQuery**</span><span class="sxs-lookup"><span data-stu-id="3dd7b-162">**IWMDRMLicenseQuery Interface**</span></span>](iwmdrmlicensequery.md)
</dt> <dt>

[<span data-ttu-id="3dd7b-163">**Esecuzione di query per ottenere informazioni semplici sui diritti**</span><span class="sxs-lookup"><span data-stu-id="3dd7b-163">**Querying for Simple Rights Information**</span></span>](querying-for-simple-rights-information.md)
</dt> </dl>

 

 





