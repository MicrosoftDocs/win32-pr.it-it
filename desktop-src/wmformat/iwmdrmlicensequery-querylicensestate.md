---
title: Metodo IWMDRMLicenseQuery QueryLicenseState (wmdrmsdk. h)
description: Il metodo QueryLicenseState esegue una query nell'archivio licenze locale per ottenere informazioni sulle licenze che si applicano a un ID chiave per uno o più diritti specifici.
ms.assetid: 17f40c56-2266-4c94-9e95-a33a92ddef74
keywords:
- Metodo QueryLicenseState Windows Media Format
- Metodo QueryLicenseState Windows Media Format, interfaccia IWMDRMLicenseQuery
- Interfaccia IWMDRMLicenseQuery-formato Windows Media, metodo QueryLicenseState
topic_type:
- apiref
api_name:
- IWMDRMLicenseQuery.QueryLicenseState
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e101d4ad9b5405906d05ba5e5f230326a1a3f13a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325559"
---
# <a name="iwmdrmlicensequeryquerylicensestate-method"></a><span data-ttu-id="bdbb4-106">Metodo IWMDRMLicenseQuery:: QueryLicenseState</span><span class="sxs-lookup"><span data-stu-id="bdbb4-106">IWMDRMLicenseQuery::QueryLicenseState method</span></span>

<span data-ttu-id="bdbb4-107">Il metodo **QueryLicenseState** esegue una query nell'archivio licenze locale per ottenere informazioni sulle licenze che si applicano a un ID chiave per uno o più diritti specifici.</span><span class="sxs-lookup"><span data-stu-id="bdbb4-107">The **QueryLicenseState** method queries the local license store for license information that applies to a Key ID for one or more specific rights.</span></span>

## <a name="syntax"></a><span data-ttu-id="bdbb4-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bdbb4-108">Syntax</span></span>


```C++
HRESULT QueryLicenseState(
  [in]  BSTR                   bstrKID,
  [in]  DWORD                  cActionsToQuery,
  [in]  BSTR                   rgbstrActionsToQuery[],
  [out] DRM_LICENSE_STATE_DATA rgResultStateData[]
);
```



## <a name="parameters"></a><span data-ttu-id="bdbb4-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="bdbb4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bdbb4-110">*bstrKID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bdbb4-110">*bstrKID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bdbb4-111">ID chiave per cui eseguire una query.</span><span class="sxs-lookup"><span data-stu-id="bdbb4-111">Key ID for which to query.</span></span> <span data-ttu-id="bdbb4-112">Verranno valutate solo le licenze che si applicano a questo ID chiave.</span><span class="sxs-lookup"><span data-stu-id="bdbb4-112">Only licenses that apply to this Key ID will be evaluated.</span></span>

</dd> <dt>

<span data-ttu-id="bdbb4-113">*cActionsToQuery* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bdbb4-113">*cActionsToQuery* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bdbb4-114">Il numero di azioni per cui eseguire una query.</span><span class="sxs-lookup"><span data-stu-id="bdbb4-114">The number of actions for which to query.</span></span> <span data-ttu-id="bdbb4-115">Questo valore deve essere impostato sul numero di elementi nelle matrici passate per i parametri *rgbstrActionsToQuery* e *rgResultStateData* .</span><span class="sxs-lookup"><span data-stu-id="bdbb4-115">This value must be set to the number of elements in the arrays passed for the *rgbstrActionsToQuery* and *rgResultStateData* parameters.</span></span>

</dd> <dt>

<span data-ttu-id="bdbb4-116">*\[ rgbstrActionsToQuery \]* \[in\]</span><span class="sxs-lookup"><span data-stu-id="bdbb4-116">*rgbstrActionsToQuery\[\]* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bdbb4-117">Matrice di uno o più diritti per i quali eseguire una query.</span><span class="sxs-lookup"><span data-stu-id="bdbb4-117">Array of one or more rights for which to query.</span></span> <span data-ttu-id="bdbb4-118">Questa matrice deve contenere il numero di elementi specificato da *cActionsToQuery*.</span><span class="sxs-lookup"><span data-stu-id="bdbb4-118">This array must contain as many elements as specified by *cActionsToQuery*.</span></span> <span data-ttu-id="bdbb4-119">Ogni elemento deve essere impostato su una delle seguenti costanti.</span><span class="sxs-lookup"><span data-stu-id="bdbb4-119">Each element must be set to one of the following constants.</span></span>



| <span data-ttu-id="bdbb4-120">Costante</span><span class="sxs-lookup"><span data-stu-id="bdbb4-120">Constant</span></span>                                        | <span data-ttu-id="bdbb4-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bdbb4-121">Description</span></span>                                                                                                                                        |
|-------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bdbb4-122">g \_ wszWMDRM \_ LicenseState \_ backup</span><span class="sxs-lookup"><span data-stu-id="bdbb4-122">g\_wszWMDRM\_LicenseState\_Backup</span></span>               | <span data-ttu-id="bdbb4-123">Includere per eseguire una query per informazioni dettagliate sul diritto di eseguire il backup e il ripristino della licenza.</span><span class="sxs-lookup"><span data-stu-id="bdbb4-123">Include to query for the details about the right to back up and restore the license.</span></span>                                                               |
| <span data-ttu-id="bdbb4-124">g \_ wszWMDRM \_ LicenseState \_ CollaborativePlay</span><span class="sxs-lookup"><span data-stu-id="bdbb4-124">g\_wszWMDRM\_LicenseState\_CollaborativePlay</span></span>    | <span data-ttu-id="bdbb4-125">Includere per eseguire una query per informazioni dettagliate sul diritto di condividere il contenuto con un gruppo di utenti come parte di uno scenario di riproduzione collaborativo.</span><span class="sxs-lookup"><span data-stu-id="bdbb4-125">Include to query for the details about the right to share the content with a group of users as part of a collaborative playback scenario.</span></span>          |
| <span data-ttu-id="bdbb4-126">g \_ wszWMDRM \_ LicenseState \_ Copy</span><span class="sxs-lookup"><span data-stu-id="bdbb4-126">g\_wszWMDRM\_LicenseState\_Copy</span></span>                 | <span data-ttu-id="bdbb4-127">Includere per eseguire una query per informazioni dettagliate sul diritto di copiare il contenuto in dispositivi esterni o supporti.</span><span class="sxs-lookup"><span data-stu-id="bdbb4-127">Include to query for the details about the right to copy the content to external devices or media.</span></span>                                                 |
| <span data-ttu-id="bdbb4-128">g \_ wszWMDRM \_ LicenseState \_ CopyToCD</span><span class="sxs-lookup"><span data-stu-id="bdbb4-128">g\_wszWMDRM\_LicenseState\_CopyToCD</span></span>             | <span data-ttu-id="bdbb4-129">Includere per eseguire una query per informazioni dettagliate sul diritto di copiare il contenuto in CD.</span><span class="sxs-lookup"><span data-stu-id="bdbb4-129">Include to query for the details about the right to copy the content to CD.</span></span>                                                                        |
| <span data-ttu-id="bdbb4-130">g \_ wszWMDRM \_ LicenseState \_ CopyToNonSDMIDevice</span><span class="sxs-lookup"><span data-stu-id="bdbb4-130">g\_wszWMDRM\_LicenseState\_CopyToNonSDMIDevice</span></span>  | <span data-ttu-id="bdbb4-131">Includere per eseguire una query per informazioni dettagliate sul diritto di copiare il contenuto in un dispositivo che non supporta l'iniziativa Secure Digital Media Initiative (SDMI).</span><span class="sxs-lookup"><span data-stu-id="bdbb4-131">Include to query for the details about the right to copy the content to a device that does not support the secure digital media initiative (SDMI).</span></span> |
| <span data-ttu-id="bdbb4-132">g \_ wszWMDRM \_ LicenseState \_ CopyToSDMIDevice</span><span class="sxs-lookup"><span data-stu-id="bdbb4-132">g\_wszWMDRM\_LicenseState\_CopyToSDMIDevice</span></span>     | <span data-ttu-id="bdbb4-133">Includere per eseguire una query per informazioni dettagliate sul diritto di copiare il contenuto in un dispositivo che supporta SDMI.</span><span class="sxs-lookup"><span data-stu-id="bdbb4-133">Include to query for the details about the right to copy the content to a device that supports the SDMI.</span></span>                                           |
| <span data-ttu-id="bdbb4-134">g \_ wszWMDRM \_ LicenseState \_ CreateThumbnailImage</span><span class="sxs-lookup"><span data-stu-id="bdbb4-134">g\_wszWMDRM\_LicenseState\_CreateThumbnailImage</span></span> | <span data-ttu-id="bdbb4-135">Includere per eseguire una query per informazioni dettagliate sul diritto di creare un'immagine di anteprima dal contenuto.</span><span class="sxs-lookup"><span data-stu-id="bdbb4-135">Include to query for the details about the right to create a thumbnail image from the content.</span></span>                                                     |
| <span data-ttu-id="bdbb4-136">\_ \_ riproduzione LicenseState g \_ wszWMDRM</span><span class="sxs-lookup"><span data-stu-id="bdbb4-136">g\_wszWMDRM\_LicenseState\_Playback</span></span>             | <span data-ttu-id="bdbb4-137">Includere per eseguire una query per informazioni dettagliate sul diritto di riprodurre il contenuto.</span><span class="sxs-lookup"><span data-stu-id="bdbb4-137">Include to query for the details about the right to play the content.</span></span>                                                                              |
| <span data-ttu-id="bdbb4-138">g \_ wszWMDRM \_ LicenseState \_ PlaylistBurn</span><span class="sxs-lookup"><span data-stu-id="bdbb4-138">g\_wszWMDRM\_LicenseState\_PlaylistBurn</span></span>         | <span data-ttu-id="bdbb4-139">Includere per eseguire una query per informazioni dettagliate sul diritto di copiare il contenuto in CD come parte di una playlist.</span><span class="sxs-lookup"><span data-stu-id="bdbb4-139">Include to query for the details about the right to copy the content to CD as part of a playlist.</span></span>                                                  |



 

</dd> <dt>

<span data-ttu-id="bdbb4-140">*\[ rgResultStateData \]* in \[ uscita\]</span><span class="sxs-lookup"><span data-stu-id="bdbb4-140">*rgResultStateData\[\]* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bdbb4-141">Matrice di una o più strutture di [**dati di \_ stato delle licenze \_ \_ DRM**](drmdrm-license-state-data.md) che ricevono le informazioni sullo stato della licenza che si applicano a destra nell'elemento corrispondente del parametro *rgbstrActionsToQuery* .</span><span class="sxs-lookup"><span data-stu-id="bdbb4-141">Array of one or more [**DRM\_LICENSE\_STATE\_DATA**](drmdrm-license-state-data.md) structures that receive the license state information that applies to the right in the corresponding element of the *rgbstrActionsToQuery* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bdbb4-142">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bdbb4-142">Return value</span></span>

<span data-ttu-id="bdbb4-143">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="bdbb4-143">The method returns an **HRESULT**.</span></span> <span data-ttu-id="bdbb4-144">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="bdbb4-144">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="bdbb4-145">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="bdbb4-145">Return code</span></span>                                                                          | <span data-ttu-id="bdbb4-146">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bdbb4-146">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="bdbb4-147"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="bdbb4-147"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="bdbb4-148">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="bdbb4-148">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="bdbb4-149">Commenti</span><span class="sxs-lookup"><span data-stu-id="bdbb4-149">Remarks</span></span>

<span data-ttu-id="bdbb4-150">Verrà eseguita la ricerca e la valutazione di tutte le licenze valide per l'ID chiave specificato.</span><span class="sxs-lookup"><span data-stu-id="bdbb4-150">All licenses that apply to the specified Key ID will be searched and evaluated.</span></span> <span data-ttu-id="bdbb4-151">I risultati sono aggregati, pertanto ogni **struttura \_ \_ \_ dei dati di stato delle licenze DRM** può contenere informazioni di più licenze.</span><span class="sxs-lookup"><span data-stu-id="bdbb4-151">The results are aggregated, so each **DRM\_LICENSE\_STATE\_DATA** structure may contain information from multiple licenses.</span></span>

## <a name="requirements"></a><span data-ttu-id="bdbb4-152">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bdbb4-152">Requirements</span></span>



| <span data-ttu-id="bdbb4-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="bdbb4-153">Requirement</span></span> | <span data-ttu-id="bdbb4-154">Valore</span><span class="sxs-lookup"><span data-stu-id="bdbb4-154">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bdbb4-155">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bdbb4-155">Header</span></span><br/>  | <dl> <span data-ttu-id="bdbb4-156"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="bdbb4-156"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="bdbb4-157">Libreria</span><span class="sxs-lookup"><span data-stu-id="bdbb4-157">Library</span></span><br/> | <dl> <span data-ttu-id="bdbb4-158"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bdbb4-158"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bdbb4-159">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bdbb4-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bdbb4-160">**Interfaccia IWMDRMLicenseQuery**</span><span class="sxs-lookup"><span data-stu-id="bdbb4-160">**IWMDRMLicenseQuery Interface**</span></span>](iwmdrmlicensequery.md)
</dt> </dl>

 

 





