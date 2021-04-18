---
title: Struttura DRM_LICENSE_STATE_DATA (Drmexternals. h)
description: La \_ \_ \_ struttura dei dati di stato della licenza DRM contiene informazioni sulle licenze relative a un diritto DRM specificato.
ms.assetid: 5ca577b5-d28b-4e36-8af7-6fae4300d464
keywords:
- Formato di Windows Media per la struttura DRM_LICENSE_STATE_DATA
- struttura Windows Media Format
topic_type:
- apiref
api_name:
- DRM_LICENSE_STATE_DATA
api_location:
- Drmexternals.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3bb63bce02a52aefcf1f3351fe34ab008996aa0b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302062"
---
# <a name="drm_license_state_data-structure-drmexternalsh"></a><span data-ttu-id="76f9b-105">Struttura DRM_LICENSE_STATE_DATA (Drmexternals. h)</span><span class="sxs-lookup"><span data-stu-id="76f9b-105">DRM_LICENSE_STATE_DATA structure (Drmexternals.h)</span></span>

<span data-ttu-id="76f9b-106">La **struttura \_ \_ \_ dei dati di stato della licenza DRM** contiene informazioni sulle [*licenze*](wmformat-glossary.md) relative a un diritto [*DRM*](wmformat-glossary.md) specificato.</span><span class="sxs-lookup"><span data-stu-id="76f9b-106">The **DRM\_LICENSE\_STATE\_DATA** structure contains [*license*](wmformat-glossary.md) information about a specified [*DRM*](wmformat-glossary.md) right.</span></span>

## <a name="syntax"></a><span data-ttu-id="76f9b-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="76f9b-107">Syntax</span></span>


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



## <a name="members"></a><span data-ttu-id="76f9b-108">Members</span><span class="sxs-lookup"><span data-stu-id="76f9b-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="76f9b-109">**dwStreamId**</span><span class="sxs-lookup"><span data-stu-id="76f9b-109">**dwStreamId**</span></span>
</dt> <dd>

<span data-ttu-id="76f9b-110">Numero di flusso a cui si applica la licenza.</span><span class="sxs-lookup"><span data-stu-id="76f9b-110">Stream number to which the license applies.</span></span> <span data-ttu-id="76f9b-111">Deve essere 0, che indica che la licenza viene applicata a tutti i flussi del file.</span><span class="sxs-lookup"><span data-stu-id="76f9b-111">Must be 0, which indicates that the license applies to all streams in the file.</span></span>

</dd> <dt>

<span data-ttu-id="76f9b-112">**dwCategory**</span><span class="sxs-lookup"><span data-stu-id="76f9b-112">**dwCategory**</span></span>
</dt> <dd>

<span data-ttu-id="76f9b-113">Categoria di stringa da visualizzare.</span><span class="sxs-lookup"><span data-stu-id="76f9b-113">Category of string to be displayed.</span></span> <span data-ttu-id="76f9b-114">Vedere [**la \_ \_ \_ categoria dello stato della licenza DRM**](drm-license-state-category.md) per i valori possibili e il relativo significato.</span><span class="sxs-lookup"><span data-stu-id="76f9b-114">See [**DRM\_LICENSE\_STATE\_CATEGORY**](drm-license-state-category.md) for possible values and their meaning.</span></span>

</dd> <dt>

<span data-ttu-id="76f9b-115">**dwNumCounts**</span><span class="sxs-lookup"><span data-stu-id="76f9b-115">**dwNumCounts**</span></span>
</dt> <dd>

<span data-ttu-id="76f9b-116">Numero di elementi forniti in **dwCount**.</span><span class="sxs-lookup"><span data-stu-id="76f9b-116">Number of items supplied in **dwCount**.</span></span> <span data-ttu-id="76f9b-117">Questo valore è in genere 0 o 1.</span><span class="sxs-lookup"><span data-stu-id="76f9b-117">This value is typically 0 or 1.</span></span>

</dd> <dt>

<span data-ttu-id="76f9b-118">**dwCount \[ 4\]**</span><span class="sxs-lookup"><span data-stu-id="76f9b-118">**dwCount\[4\]**</span></span>
</dt> <dd>

<span data-ttu-id="76f9b-119">Matrice di 0 o 1 o più **DWORD** che rappresenta il numero di volte in cui è possibile eseguire l'azione specificata in **dwCategory** .</span><span class="sxs-lookup"><span data-stu-id="76f9b-119">An array of 0 or 1 or more **DWORD** s that represent the number of times the action specified in **dwCategory** may be performed.</span></span> <span data-ttu-id="76f9b-120">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="76f9b-120">See remarks.</span></span>

</dd> <dt>

<span data-ttu-id="76f9b-121">**dwNumDates**</span><span class="sxs-lookup"><span data-stu-id="76f9b-121">**dwNumDates**</span></span>
</dt> <dd>

<span data-ttu-id="76f9b-122">Numero di elementi forniti in **DateTime**.</span><span class="sxs-lookup"><span data-stu-id="76f9b-122">Number of items supplied in **datetime**.</span></span> <span data-ttu-id="76f9b-123">In genere, non vengono usate più di due date, ad esempio, con una licenza valida da una data fino a un'altra data.</span><span class="sxs-lookup"><span data-stu-id="76f9b-123">Typically no more than two dates are used, for example, with a license that is valid from one date until another date.</span></span>

</dd> <dt>

<span data-ttu-id="76f9b-124">**DateTime \[ 4\]**</span><span class="sxs-lookup"><span data-stu-id="76f9b-124">**datetime\[4\]**</span></span>
</dt> <dd>

<span data-ttu-id="76f9b-125">Matrice di una o più strutture FILETIME che rappresentano una o più date nella licenza.</span><span class="sxs-lookup"><span data-stu-id="76f9b-125">An array of one or more FILETIME structures representing one or more dates in the license.</span></span> <span data-ttu-id="76f9b-126">Il significato di una determinata data dipende dal valore di **dwCategory**.</span><span class="sxs-lookup"><span data-stu-id="76f9b-126">The meaning of a particular date depends on the value of **dwCategory**.</span></span>

</dd> <dt>

<span data-ttu-id="76f9b-127">**dwVague**</span><span class="sxs-lookup"><span data-stu-id="76f9b-127">**dwVague**</span></span>
</dt> <dd>

<span data-ttu-id="76f9b-128">Zero o più dei flag seguenti combinati con un **or** bit per bit:</span><span class="sxs-lookup"><span data-stu-id="76f9b-128">Zero or more of the following flags combined with a bitwise **OR**:</span></span>



| <span data-ttu-id="76f9b-129">Flag</span><span class="sxs-lookup"><span data-stu-id="76f9b-129">Flag</span></span>                                    | <span data-ttu-id="76f9b-130">Descrizione</span><span class="sxs-lookup"><span data-stu-id="76f9b-130">Description</span></span>                                                                                                                                           |
|-----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="76f9b-131">\_dati di stato della licenza DRM \_ \_ \_ vaghi</span><span class="sxs-lookup"><span data-stu-id="76f9b-131">DRM\_LICENSE\_STATE\_DATA\_VAGUE</span></span>        | <span data-ttu-id="76f9b-132">Se impostato, potrebbero essere presenti più licenze valide per il contenuto.</span><span class="sxs-lookup"><span data-stu-id="76f9b-132">If set, there may be more licenses that apply to the content.</span></span>                                                                                         |
| <span data-ttu-id="76f9b-133">\_OPL dati di stato della licenza DRM \_ \_ \_ \_ presenti</span><span class="sxs-lookup"><span data-stu-id="76f9b-133">DRM\_LICENSE\_STATE\_DATA\_OPL\_PRESENT</span></span> | <span data-ttu-id="76f9b-134">Se impostata, la licenza include i livelli di protezione dell'output (OPLs) che devono essere recuperati e controllati rispetto alla destinazione dell'output dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="76f9b-134">If set, the license includes output protection levels (OPLs) that must be retrieved and checked against the destination of your application's output.</span></span> |
| <span data-ttu-id="76f9b-135">\_ \_ \_ \_ SAP presente dati di stato delle licenze DRM \_</span><span class="sxs-lookup"><span data-stu-id="76f9b-135">DRM\_LICENSE\_STATE\_DATA\_SAP\_PRESENT</span></span> | <span data-ttu-id="76f9b-136">Se impostato, il contenuto deve essere recapitato usando il percorso audio sicuro (SAP).</span><span class="sxs-lookup"><span data-stu-id="76f9b-136">If set, the content must be delivered using secure audio path (SAP).</span></span>                                                                                  |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="76f9b-137">Commenti</span><span class="sxs-lookup"><span data-stu-id="76f9b-137">Remarks</span></span>

<span data-ttu-id="76f9b-138">Questa struttura viene restituita (incapsulata in una struttura di [**\_ \_ \_ dati dello stato di licenza WM**](/previous-versions/windows/desktop/legacy/dd757942(v=vs.85)) ) da una chiamata a [**IWMDRMReader:: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty) quando si specifica una delle proprietà di stato della licenza DRM.</span><span class="sxs-lookup"><span data-stu-id="76f9b-138">This structure is returned (encapsulated in a [**WM\_LICENSE\_STATE\_DATA**](/previous-versions/windows/desktop/legacy/dd757942(v=vs.85)) structure) from a call to [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty) when you specify one of the DRM license state properties.</span></span> <span data-ttu-id="76f9b-139">Le proprietà sono riportate di seguito:</span><span class="sxs-lookup"><span data-stu-id="76f9b-139">These properties are:</span></span>

-   [<span data-ttu-id="76f9b-140">**\_Riproduzione LICENSESTATE \_ DRM**</span><span class="sxs-lookup"><span data-stu-id="76f9b-140">**DRM\_LicenseState\_Playback**</span></span>](drm-licensestate-playback.md)
-   [<span data-ttu-id="76f9b-141">**\_CopyToCD LICENSESTATE \_ DRM**</span><span class="sxs-lookup"><span data-stu-id="76f9b-141">**DRM\_LicenseState\_CopyToCD**</span></span>](drm-licensestate-copytocd.md)
-   [<span data-ttu-id="76f9b-142">**\_CopyToSDMIDevice LICENSESTATE \_ DRM**</span><span class="sxs-lookup"><span data-stu-id="76f9b-142">**DRM\_LicenseState\_CopyToSDMIDevice**</span></span>](drm-licensestate-copytosdmidevice.md)
-   [<span data-ttu-id="76f9b-143">**\_CopyToNonSDMIDevice LICENSESTATE \_ DRM**</span><span class="sxs-lookup"><span data-stu-id="76f9b-143">**DRM\_LicenseState\_CopyToNonSDMIDevice**</span></span>](drm-licensestate-copytononsdmidevice.md)
-   [<span data-ttu-id="76f9b-144">**\_CollaborativePlay LICENSESTATE \_ DRM**</span><span class="sxs-lookup"><span data-stu-id="76f9b-144">**DRM\_LicenseState\_CollaborativePlay**</span></span>](drm-licensestate-collaborativeplay.md)
-   [<span data-ttu-id="76f9b-145">**\_Copia di LICENSESTATE DRM \_**</span><span class="sxs-lookup"><span data-stu-id="76f9b-145">**DRM\_LicenseState\_Copy**</span></span>](drm-licensestate-copy.md)
-   [<span data-ttu-id="76f9b-146">**\_PlaylistBurn LICENSESTATE \_ DRM**</span><span class="sxs-lookup"><span data-stu-id="76f9b-146">**DRM\_LicenseState\_PlaylistBurn**</span></span>](drm-licensestate-playlistburn.md)

<span data-ttu-id="76f9b-147">Se **dwCategory** è **il \_ \_ \_ conteggio dello stato di licenza WM DRM \_ \_ da \_ fino a,** la matrice **DateTime** conterrà in genere due date, una data "from" e una data "until".</span><span class="sxs-lookup"><span data-stu-id="76f9b-147">If **dwCategory** is **WM\_DRM\_LICENSE\_STATE\_COUNT\_FROM\_UNTIL,** then the **datetime** array will typically contain two dates, a "from" date and an "until" date.</span></span> <span data-ttu-id="76f9b-148">È anche possibile specificare due coppie di date per creare licenze più complesse.</span><span class="sxs-lookup"><span data-stu-id="76f9b-148">Two date pairs may also be specified to create more complex licenses.</span></span>

<span data-ttu-id="76f9b-149">Gli elementi della matrice **dwCount** corrispondono agli intervalli di date o date specificati nella matrice **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="76f9b-149">The elements of the **dwCount** array correspond to the dates or date ranges specified in the **datetime** array.</span></span> <span data-ttu-id="76f9b-150">Se **dwCategory** è **il \_ \_ \_ conteggio dello stato di licenza WM DRM \_ \_ da \_ until** e **DateTime** contiene una coppia di date, **dwCount** conterrà un elemento.</span><span class="sxs-lookup"><span data-stu-id="76f9b-150">If **dwCategory** is **WM\_DRM\_LICENSE\_STATE\_COUNT\_FROM\_UNTIL** and **datetime** contains one pair of dates, then **dwCount** will contain one element.</span></span> <span data-ttu-id="76f9b-151">Se **DateTime** contiene due coppie di date (quattro elementi), **dwCount** deve contenere due elementi, uno per ogni coppia di date.</span><span class="sxs-lookup"><span data-stu-id="76f9b-151">If **datetime** contains two date pairs (four elements), then **dwCount** should contain two elements, one for each date pair.</span></span>

<span data-ttu-id="76f9b-152">In alcuni casi, è possibile che agli utenti sia stata rilasciata più di una licenza per un file.</span><span class="sxs-lookup"><span data-stu-id="76f9b-152">In some cases, users may have been issued more than one license for a file.</span></span> <span data-ttu-id="76f9b-153">Potrebbero ad esempio avere acquisito una licenza che consentiva cinque Play fino alla fine del mese e successivamente ha acquisito una seconda licenza per diritti illimitati.</span><span class="sxs-lookup"><span data-stu-id="76f9b-153">For example, they might have acquired a license that allowed five plays until the end of the month, and later acquired a second license for unlimited rights.</span></span> <span data-ttu-id="76f9b-154">In tal caso, il \_ \_ flag di dati dello stato delle licenze DRM \_ \_ è impostato in **dwVague** ( `dwVague & DRM_LICENSE_STATE_DATA_VAGUE != 0` ) e il componente DRM utilizzerà un algoritmo per determinare il set di diritti più probabile applicato.</span><span class="sxs-lookup"><span data-stu-id="76f9b-154">In such a case, the DRM\_LICENSE\_STATE\_DATA\_VAGUE flag is set in **dwVague** (`dwVague & DRM_LICENSE_STATE_DATA_VAGUE != 0`) and the DRM component will use an algorithm to determine the most likely set of rights that have been applied.</span></span> <span data-ttu-id="76f9b-155">Quando una licenza scade, il componente DRM esamina le licenze rimanenti e così via fino a quando tutte le licenze non saranno scadute.</span><span class="sxs-lookup"><span data-stu-id="76f9b-155">When one license expires, the DRM component will examine the remaining license(s), and so on until all licenses have expired.</span></span>

## <a name="requirements"></a><span data-ttu-id="76f9b-156">Requisiti</span><span class="sxs-lookup"><span data-stu-id="76f9b-156">Requirements</span></span>



| <span data-ttu-id="76f9b-157">Requisito</span><span class="sxs-lookup"><span data-stu-id="76f9b-157">Requirement</span></span> | <span data-ttu-id="76f9b-158">Valore</span><span class="sxs-lookup"><span data-stu-id="76f9b-158">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="76f9b-159">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="76f9b-159">Minimum supported client</span></span><br/> | <span data-ttu-id="76f9b-160">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="76f9b-160">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="76f9b-161">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="76f9b-161">Minimum supported server</span></span><br/> | <span data-ttu-id="76f9b-162">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="76f9b-162">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="76f9b-163">Versione</span><span class="sxs-lookup"><span data-stu-id="76f9b-163">Version</span></span><br/>                  | <span data-ttu-id="76f9b-164">Windows Media Format 7 SDK o versioni successive dell'SDK</span><span class="sxs-lookup"><span data-stu-id="76f9b-164">Windows Media Format 7 SDK, or later versions of the SDK</span></span><br/>                       |
| <span data-ttu-id="76f9b-165">Intestazione</span><span class="sxs-lookup"><span data-stu-id="76f9b-165">Header</span></span><br/>                   | <dl> <span data-ttu-id="76f9b-166"><dt>Drmexternals. h</dt></span><span class="sxs-lookup"><span data-stu-id="76f9b-166"><dt>Drmexternals.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="76f9b-167">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="76f9b-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76f9b-168">**Strutture**</span><span class="sxs-lookup"><span data-stu-id="76f9b-168">**Structures**</span></span>](structures.md)
</dt> </dl>

 

