---
title: Struttura DRM_LICENSE_STATE_DATA (wmdrmsdk. h)
description: La \_ \_ struttura dei dati di stato delle licenze DRM \_ contiene informazioni sulle restrizioni di licenza per un diritto DRM.
ms.assetid: 822d60ae-5d96-4577-8564-0e1adafa5dd5
keywords:
- Formato di Windows Media per la struttura DRM_LICENSE_STATE_DATA
- struttura Windows Media Format
topic_type:
- apiref
api_name:
- DRM_LICENSE_STATE_DATA
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b02f38b8f09b7b444949e9477635e6b8770fc168
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330587"
---
# <a name="drm_license_state_data-structure-wmdrmsdkh"></a><span data-ttu-id="5934a-105">Struttura DRM_LICENSE_STATE_DATA (wmdrmsdk. h)</span><span class="sxs-lookup"><span data-stu-id="5934a-105">DRM_LICENSE_STATE_DATA structure (Wmdrmsdk.h)</span></span>

<span data-ttu-id="5934a-106">La **struttura \_ \_ \_ dei dati di stato delle licenze DRM** contiene informazioni sulle restrizioni di licenza per un diritto DRM.</span><span class="sxs-lookup"><span data-stu-id="5934a-106">The **DRM\_LICENSE\_STATE\_DATA** structure contains information about the license restrictions for a DRM right.</span></span>

## <a name="syntax"></a><span data-ttu-id="5934a-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5934a-107">Syntax</span></span>


```C++
typedef struct DRM_LICENSE_STATE_DATA {
  DWORD                      dwStreamId;
  DRM_LICENSE_STATE_CATEGORY dwCategory;
  DWORD                      dwNumCounts;
  DWORD                      dwCount[4];
  DWORD                      dwNumDates;
  FILETIME                   datetime[4];
  DWORD                      dwVague;
} ;
```



## <a name="members"></a><span data-ttu-id="5934a-108">Members</span><span class="sxs-lookup"><span data-stu-id="5934a-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="5934a-109">**dwStreamId**</span><span class="sxs-lookup"><span data-stu-id="5934a-109">**dwStreamId**</span></span>
</dt> <dd>

<span data-ttu-id="5934a-110">Numero di flusso a cui si applica la licenza.</span><span class="sxs-lookup"><span data-stu-id="5934a-110">Stream number to which the license applies.</span></span> <span data-ttu-id="5934a-111">Deve essere 0, che indica che la licenza viene applicata a tutti i flussi del file.</span><span class="sxs-lookup"><span data-stu-id="5934a-111">Must be 0, which indicates that the license applies to all streams in the file.</span></span>

</dd> <dt>

<span data-ttu-id="5934a-112">**dwCategory**</span><span class="sxs-lookup"><span data-stu-id="5934a-112">**dwCategory**</span></span>
</dt> <dd>

<span data-ttu-id="5934a-113">Categoria di stringa da visualizzare.</span><span class="sxs-lookup"><span data-stu-id="5934a-113">Category of string to be displayed.</span></span> <span data-ttu-id="5934a-114">Vedere [**la \_ \_ \_ categoria dello stato della licenza DRM**](drmdrm-license-state-category.md) per i valori possibili e il relativo significato.</span><span class="sxs-lookup"><span data-stu-id="5934a-114">See [**DRM\_LICENSE\_STATE\_CATEGORY**](drmdrm-license-state-category.md) for possible values and their meaning.</span></span>

</dd> <dt>

<span data-ttu-id="5934a-115">**dwNumCounts**</span><span class="sxs-lookup"><span data-stu-id="5934a-115">**dwNumCounts**</span></span>
</dt> <dd>

<span data-ttu-id="5934a-116">Numero di elementi forniti in **dwCount**.</span><span class="sxs-lookup"><span data-stu-id="5934a-116">Number of items supplied in **dwCount**.</span></span> <span data-ttu-id="5934a-117">Questo valore è in genere 0 o 1.</span><span class="sxs-lookup"><span data-stu-id="5934a-117">This value is typically 0 or 1.</span></span>

</dd> <dt>

<span data-ttu-id="5934a-118">**dwCount \[ 4\]**</span><span class="sxs-lookup"><span data-stu-id="5934a-118">**dwCount\[4\]**</span></span>
</dt> <dd>

<span data-ttu-id="5934a-119">Matrice di 0 o 1 o più valori **DWORD** che rappresentano il numero di volte in cui è possibile eseguire l'azione specificata in **dwCategory** .</span><span class="sxs-lookup"><span data-stu-id="5934a-119">An array of 0 or 1 or more **DWORD** values that represent the number of times the action specified in **dwCategory** may be performed.</span></span> <span data-ttu-id="5934a-120">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="5934a-120">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="5934a-121">**dwNumDates**</span><span class="sxs-lookup"><span data-stu-id="5934a-121">**dwNumDates**</span></span>
</dt> <dd>

<span data-ttu-id="5934a-122">Numero di elementi forniti in **DateTime**.</span><span class="sxs-lookup"><span data-stu-id="5934a-122">Number of items supplied in **datetime**.</span></span> <span data-ttu-id="5934a-123">In genere, non vengono usate più di due date, ad esempio, con una licenza valida da una data fino a un'altra data.</span><span class="sxs-lookup"><span data-stu-id="5934a-123">Typically no more than two dates are used, for example, with a license that is valid from one date until another date.</span></span>

</dd> <dt>

<span data-ttu-id="5934a-124">**DateTime \[ 4\]**</span><span class="sxs-lookup"><span data-stu-id="5934a-124">**datetime\[4\]**</span></span>
</dt> <dd>

<span data-ttu-id="5934a-125">Matrice di una o più strutture **FILETIME** che rappresentano una o più date nella licenza.</span><span class="sxs-lookup"><span data-stu-id="5934a-125">An array of one or more **FILETIME** structures representing one or more dates in the license.</span></span> <span data-ttu-id="5934a-126">Il significato di una determinata data dipende dal valore di **dwCategory**.</span><span class="sxs-lookup"><span data-stu-id="5934a-126">The meaning of a particular date depends on the value of **dwCategory**.</span></span>

</dd> <dt>

<span data-ttu-id="5934a-127">**dwVague**</span><span class="sxs-lookup"><span data-stu-id="5934a-127">**dwVague**</span></span>
</dt> <dd>

<span data-ttu-id="5934a-128">Zero o più dei flag seguenti combinati con un **or** bit per bit:</span><span class="sxs-lookup"><span data-stu-id="5934a-128">Zero or more of the following flags combined with a bitwise **OR**:</span></span>



| <span data-ttu-id="5934a-129">Flag</span><span class="sxs-lookup"><span data-stu-id="5934a-129">Flag</span></span>                                    | <span data-ttu-id="5934a-130">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5934a-130">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5934a-131">\_dati di stato della licenza DRM \_ \_ \_ vaghi</span><span class="sxs-lookup"><span data-stu-id="5934a-131">DRM\_LICENSE\_STATE\_DATA\_VAGUE</span></span>        | <span data-ttu-id="5934a-132">Se impostato, potrebbero essere presenti più licenze valide per il contenuto.</span><span class="sxs-lookup"><span data-stu-id="5934a-132">If set, there may be more licenses that apply to the content.</span></span> <span data-ttu-id="5934a-133">L'unico modo per essere certi sulle singole licenze che si applicano a un ID chiave specifico è enumerare le licenze.</span><span class="sxs-lookup"><span data-stu-id="5934a-133">The only way to be certain about the individual licenses that apply to a given key ID is to enumerate the licenses.</span></span> <span data-ttu-id="5934a-134">A tale scopo, chiamare [**IWMDRMLicenseManagement:: CreateLicenseEnumeration**](iwmdrmlicensemanagement-createlicenseenumeration.md), passando l'ID chiave come parametro bstrKID.</span><span class="sxs-lookup"><span data-stu-id="5934a-134">To do this, call [**IWMDRMLicenseManagement::CreateLicenseEnumeration**](iwmdrmlicensemanagement-createlicenseenumeration.md), passing the key ID as the bstrKID parameter.</span></span> <span data-ttu-id="5934a-135">Usare quindi l'interfaccia IWMDRMLicense recuperata per esaminare le licenze.</span><span class="sxs-lookup"><span data-stu-id="5934a-135">Then use the retrieved IWMDRMLicense interface to examine the licenses.</span></span> |
| <span data-ttu-id="5934a-136">\_OPL dati di stato della licenza DRM \_ \_ \_ \_ presenti</span><span class="sxs-lookup"><span data-stu-id="5934a-136">DRM\_LICENSE\_STATE\_DATA\_OPL\_PRESENT</span></span> | <span data-ttu-id="5934a-137">Se impostata, la licenza include i livelli di protezione dell'output (OPLs) che devono essere recuperati e controllati rispetto alla destinazione dell'output dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="5934a-137">If set, the license includes output protection levels (OPLs) that must be retrieved and checked against the destination of your application's output.</span></span>                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="5934a-138">\_ \_ \_ \_ SAP presente dati di stato delle licenze DRM \_</span><span class="sxs-lookup"><span data-stu-id="5934a-138">DRM\_LICENSE\_STATE\_DATA\_SAP\_PRESENT</span></span> | <span data-ttu-id="5934a-139">Se impostato, il contenuto deve essere recapitato usando il percorso audio sicuro (SAP).</span><span class="sxs-lookup"><span data-stu-id="5934a-139">If set, the content must be delivered using secure audio path (SAP).</span></span>                                                                                                                                                                                                                                                                                                                                                                   |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5934a-140">Commenti</span><span class="sxs-lookup"><span data-stu-id="5934a-140">Remarks</span></span>

<span data-ttu-id="5934a-141">Questa struttura viene recuperata chiamando **IWMDRMLicenseQuery:: QueryLicenseState**.</span><span class="sxs-lookup"><span data-stu-id="5934a-141">This structure is retrieved by calling **IWMDRMLicenseQuery::QueryLicenseState**.</span></span>

<span data-ttu-id="5934a-142">Se **dwCategory** è **il \_ \_ \_ conteggio dello stato di licenza WM DRM \_ \_ da \_ fino a**, la matrice **DateTime** conterrà in genere due date: una data "from" e una data "until".</span><span class="sxs-lookup"><span data-stu-id="5934a-142">If **dwCategory** is **WM\_DRM\_LICENSE\_STATE\_COUNT\_FROM\_UNTIL**, then the **datetime** array will typically contain two dates: a "from" date and an "until" date.</span></span> <span data-ttu-id="5934a-143">È anche possibile specificare due coppie di date per creare licenze più complesse.</span><span class="sxs-lookup"><span data-stu-id="5934a-143">Two date pairs may also be specified to create more complex licenses.</span></span>

<span data-ttu-id="5934a-144">Gli elementi della matrice **dwCount** corrispondono agli intervalli di date o date specificati nella matrice **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="5934a-144">The elements of the **dwCount** array correspond to the dates or date ranges specified in the **datetime** array.</span></span> <span data-ttu-id="5934a-145">Se **dwCategory** è **il \_ \_ \_ conteggio dello stato di licenza WM DRM \_ \_ da \_ until** e **DateTime** contiene una coppia di date, **dwCount** conterrà un elemento.</span><span class="sxs-lookup"><span data-stu-id="5934a-145">If **dwCategory** is **WM\_DRM\_LICENSE\_STATE\_COUNT\_FROM\_UNTIL** and **datetime** contains one pair of dates, then **dwCount** will contain one element.</span></span> <span data-ttu-id="5934a-146">Se **DateTime** contiene due coppie di date (quattro elementi), **dwCount** deve contenere due elementi, uno per ogni coppia di date.</span><span class="sxs-lookup"><span data-stu-id="5934a-146">If **datetime** contains two date pairs (four elements), then **dwCount** should contain two elements, one for each date pair.</span></span>

<span data-ttu-id="5934a-147">In alcuni casi, è possibile che agli utenti sia stata rilasciata più di una licenza per un file.</span><span class="sxs-lookup"><span data-stu-id="5934a-147">In some cases, users may have been issued more than one license for a file.</span></span> <span data-ttu-id="5934a-148">Potrebbero ad esempio avere acquisito una licenza che consentiva cinque Play fino alla fine del mese e successivamente ha acquisito una seconda licenza per diritti illimitati.</span><span class="sxs-lookup"><span data-stu-id="5934a-148">For example, they might have acquired a license that allowed five plays until the end of the month, and later acquired a second license for unlimited rights.</span></span> <span data-ttu-id="5934a-149">In tal caso, il \_ \_ flag di dati dello stato delle licenze DRM \_ \_ è impostato in **dwVague** ( `dwVague & DRM_LICENSE_STATE_DATA_VAGUE != 0` ) e il componente DRM utilizzerà un algoritmo per determinare il set di diritti più probabile applicato.</span><span class="sxs-lookup"><span data-stu-id="5934a-149">In such a case, the DRM\_LICENSE\_STATE\_DATA\_VAGUE flag is set in **dwVague** (`dwVague & DRM_LICENSE_STATE_DATA_VAGUE != 0`) and the DRM component will use an algorithm to determine the most likely set of rights that have been applied.</span></span> <span data-ttu-id="5934a-150">Quando una licenza scade, il componente DRM esaminerà le licenze rimanenti e così via fino a quando tutte le licenze non saranno scadute.</span><span class="sxs-lookup"><span data-stu-id="5934a-150">When one license expires, the DRM component will examine the remaining licenses, and so on until all licenses have expired.</span></span>

## <a name="requirements"></a><span data-ttu-id="5934a-151">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5934a-151">Requirements</span></span>



| <span data-ttu-id="5934a-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="5934a-152">Requirement</span></span> | <span data-ttu-id="5934a-153">Valore</span><span class="sxs-lookup"><span data-stu-id="5934a-153">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5934a-154">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5934a-154">Header</span></span><br/> | <dl> <span data-ttu-id="5934a-155"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="5934a-155"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5934a-156">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5934a-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5934a-157">**Strutture**</span><span class="sxs-lookup"><span data-stu-id="5934a-157">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





