---
description: Il set di proprietà Protezione copia DVD fornisce l'autenticazione delle informazioni di protezione della copia dai decrittografatori hardware o software. Usare questa proprietà impostata per impedire la copia non autorizzata da DVD-Video preregistrato.
ms.assetid: da3abefd-8f25-449d-8787-84d2cef928da
title: Set di proprietà DVD Copy Protection (Dvdmedia.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 382243a6071fa73361df13ae933d259979686a06
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909479"
---
# <a name="dvd-copy-protection-property-set"></a><span data-ttu-id="0b9e5-104">Set di proprietà protezione copia DVD</span><span class="sxs-lookup"><span data-stu-id="0b9e5-104">DVD Copy Protection Property Set</span></span>

<span data-ttu-id="0b9e5-105">Il set di proprietà Protezione copia DVD fornisce l'autenticazione delle informazioni di protezione della copia dai decrittografatori hardware o software.</span><span class="sxs-lookup"><span data-stu-id="0b9e5-105">The DVD Copy Protection property set provides authentication of copy protection information from hardware or software decrypters.</span></span> <span data-ttu-id="0b9e5-106">Usare questa proprietà impostata per impedire la copia non autorizzata da DVD-Video preregistrato.</span><span class="sxs-lookup"><span data-stu-id="0b9e5-106">Use this property set to prevent unauthorized copying from prerecorded DVD-Video.</span></span>

<span data-ttu-id="0b9e5-107">Microsoft fornisce software che facilita il processo di autenticazione richiesto dallo schema di crittografia, consentendo così a un'unità DVD-ROM di autenticare e trasferire le chiavi con un decrittografatore DVD.</span><span class="sxs-lookup"><span data-stu-id="0b9e5-107">Microsoft provides software that facilitates the authentication process required by the encryption scheme, thus enabling a DVD-ROM drive to authenticate and transfer keys with a DVD decrypter.</span></span> <span data-ttu-id="0b9e5-108">Microsoft non prevede di fornire un decrittografatore DVD e, al contrario, fornisce il codice del sistema operativo che fungerà da agente per abilitare l'autenticazione dei decrittografatori hardware o software.</span><span class="sxs-lookup"><span data-stu-id="0b9e5-108">Microsoft has no current plans to ship a DVD decrypter and, instead, is providing operating system code that will act as the agent to enable authentication of either hardware or software decrypters.</span></span>

<span data-ttu-id="0b9e5-109">Lo strumento di spostamento DVD avvia e controlla il processo di scambio delle chiavi.</span><span class="sxs-lookup"><span data-stu-id="0b9e5-109">The DVD navigator initiates and controls the key exchange process.</span></span> <span data-ttu-id="0b9e5-110">Il minidriver DVD deve implementare solo le proprietà seguenti.</span><span class="sxs-lookup"><span data-stu-id="0b9e5-110">The DVD minidriver needs only to implement the following properties.</span></span> <span data-ttu-id="0b9e5-111">Gli altri componenti gestiscono il resto.</span><span class="sxs-lookup"><span data-stu-id="0b9e5-111">Other components handle the rest.</span></span>

<span data-ttu-id="0b9e5-112">Ogni flusso di input DVD riceverà le proprietà di protezione della copia.</span><span class="sxs-lookup"><span data-stu-id="0b9e5-112">Each DVD input stream will receive copy protection properties.</span></span> <span data-ttu-id="0b9e5-113">Questo vale anche se lo stesso hardware controlla tutti i flussi DVD.</span><span class="sxs-lookup"><span data-stu-id="0b9e5-113">This is true even if the same hardware controls all DVD streams.</span></span>

<span data-ttu-id="0b9e5-114">Le informazioni seguenti illustrano le costanti e i tipi di dati necessari da usare per questo set di proprietà nelle chiamate ai [**metodi IKsPropertySet.**](ikspropertyset.md)</span><span class="sxs-lookup"><span data-stu-id="0b9e5-114">The following information presents the necessary constants and data types to use for this property set in calls to [**IKsPropertySet**](ikspropertyset.md) methods.</span></span> <span data-ttu-id="0b9e5-115">Fornisce i valori per i **parametri GUID** (*guidPropSet*), ID proprietà (*dwPropID*) e tipo di dati della proprietà (*pPropData*).</span><span class="sxs-lookup"><span data-stu-id="0b9e5-115">It provides values for the **GUID** (*guidPropSet*), property ID (*dwPropID*), and property data type (*pPropData*) parameters.</span></span>



| <span data-ttu-id="0b9e5-116">Label</span><span class="sxs-lookup"><span data-stu-id="0b9e5-116">Label</span></span> | <span data-ttu-id="0b9e5-117">Valore</span><span class="sxs-lookup"><span data-stu-id="0b9e5-117">Value</span></span> |
|-------------------|---------------------------|
| <span data-ttu-id="0b9e5-118">GUID set di proprietà</span><span class="sxs-lookup"><span data-stu-id="0b9e5-118">Property Set GUID</span></span> | <span data-ttu-id="0b9e5-119">AM \_ KSPROPSETID \_ CopyProt</span><span class="sxs-lookup"><span data-stu-id="0b9e5-119">AM\_KSPROPSETID\_CopyProt</span></span> |



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0b9e5-120">ID proprietà</span><span class="sxs-lookup"><span data-stu-id="0b9e5-120">Property ID</span></span></th>
<th><span data-ttu-id="0b9e5-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0b9e5-121">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0b9e5-122"><a href="am-property-copy-analog-component-property.md"><strong>AM_PROPERTY_COPY_ANALOG_COMPONENT</strong></a></span><span class="sxs-lookup"><span data-stu-id="0b9e5-122"><a href="am-property-copy-analog-component-property.md"><strong>AM_PROPERTY_COPY_ANALOG_COMPONENT</strong></a></span></span></td>
<td><span data-ttu-id="0b9e5-123">Esegue una query per determinare se l'output video è di definizione standard, video con componente analogico.</span><span class="sxs-lookup"><span data-stu-id="0b9e5-123">Queries whether the video output is standard-definition, analog component video.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0b9e5-124">AM_PROPERTY_COPY_MACROVISION</span><span class="sxs-lookup"><span data-stu-id="0b9e5-124">AM_PROPERTY_COPY_MACROVISION</span></span></td>
<td><span data-ttu-id="0b9e5-125">Si tratta di una proprietà di sola impostazione.</span><span class="sxs-lookup"><span data-stu-id="0b9e5-125">This is a set-only property.</span></span> <span data-ttu-id="0b9e5-126">Questa proprietà imposta il livello di protezione della copia analoga per il codificatore NTSC all'estremità di output del pin ricevente.</span><span class="sxs-lookup"><span data-stu-id="0b9e5-126">This property sets the analog copy protection level for the NTSC encoder on the output end of the receiving pin.</span></span> <span data-ttu-id="0b9e5-127">Usa <a href="/previous-versions/ms778996(v=vs.85)"><strong>AM_COPY_MACROVISION</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="0b9e5-127">Uses <a href="/previous-versions/ms778996(v=vs.85)"><strong>AM_COPY_MACROVISION</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0b9e5-128">AM_PROPERTY_DVDCOPY_CHLG_KEY</span><span class="sxs-lookup"><span data-stu-id="0b9e5-128">AM_PROPERTY_DVDCOPY_CHLG_KEY</span></span></td>
<td><span data-ttu-id="0b9e5-129">Entrambe le operazioni get e set sono supportate in questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="0b9e5-129">Both get and set operations are supported on this property.</span></span> <span data-ttu-id="0b9e5-130">Un'operazione get richiede al decodificatore di fornire la chiave di richiesta del bus.</span><span class="sxs-lookup"><span data-stu-id="0b9e5-130">A get operation requests the decoder to provide its bus challenge key.</span></span> <span data-ttu-id="0b9e5-131">Un'operazione set fornisce al decodificatore la chiave di richiesta del bus dall'unità DVD.</span><span class="sxs-lookup"><span data-stu-id="0b9e5-131">A set operation provides the decoder with the bus challenge key from the DVD drive.</span></span> <span data-ttu-id="0b9e5-132">I dati passati in questa proprietà saranno una struttura di tipo <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_chlgkey"><strong>AM_DVDCOPY_CHLGKEY</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="0b9e5-132">The data passed in this property will be a structure of type <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_chlgkey"><strong>AM_DVDCOPY_CHLGKEY</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0b9e5-133">AM_PROPERTY_DVDCOPY_DEC_KEY2</span><span class="sxs-lookup"><span data-stu-id="0b9e5-133">AM_PROPERTY_DVDCOPY_DEC_KEY2</span></span></td>
<td><span data-ttu-id="0b9e5-134">Si tratta di una proprietà di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="0b9e5-134">This is a get-only property.</span></span> <span data-ttu-id="0b9e5-135">Questa proprietà richiede che la chiave bus 2 del decodificatore sia trasferita all'unità DVD.</span><span class="sxs-lookup"><span data-stu-id="0b9e5-135">This property requests that the decoder's bus key 2 be transferred to the DVD drive.</span></span> <span data-ttu-id="0b9e5-136">I dati passati saranno una struttura di tipo <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_buskey"><strong>AM_DVDCOPY_BUSKEY</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="0b9e5-136">The data passed will be a structure of type <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_buskey"><strong>AM_DVDCOPY_BUSKEY</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0b9e5-137">AM_PROPERTY_DVDCOPY_DISC_KEY</span><span class="sxs-lookup"><span data-stu-id="0b9e5-137">AM_PROPERTY_DVDCOPY_DISC_KEY</span></span></td>
<td><span data-ttu-id="0b9e5-138">Proprietà di sola impostazione.</span><span class="sxs-lookup"><span data-stu-id="0b9e5-138">Set-only property.</span></span> <span data-ttu-id="0b9e5-139">In questo modo viene fornita la chiave del disco.</span><span class="sxs-lookup"><span data-stu-id="0b9e5-139">This provides disc key.</span></span> <span data-ttu-id="0b9e5-140">La chiave è una struttura di tipo <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_disckey"><strong>AM_DVDCOPY_DISCKEY</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="0b9e5-140">The key is a structure of type <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_disckey"><strong>AM_DVDCOPY_DISCKEY</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0b9e5-141">AM_PROPERTY_DVDCOPY_DVD_KEY1</span><span class="sxs-lookup"><span data-stu-id="0b9e5-141">AM_PROPERTY_DVDCOPY_DVD_KEY1</span></span></td>
<td><span data-ttu-id="0b9e5-142">Si tratta di una proprietà di sola impostazione.</span><span class="sxs-lookup"><span data-stu-id="0b9e5-142">This is a set-only property.</span></span> <span data-ttu-id="0b9e5-143">Questa proprietà fornisce al decodificatore la chiave bus dell'unità DVD 1.</span><span class="sxs-lookup"><span data-stu-id="0b9e5-143">This property provides the DVD drive bus key 1 to the decoder.</span></span> <span data-ttu-id="0b9e5-144">I dati passati saranno una struttura di tipo <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_buskey"><strong>AM_DVDCOPY_BUSKEY</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="0b9e5-144">The data passed will be a structure of type <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_buskey"><strong>AM_DVDCOPY_BUSKEY</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0b9e5-145">AM_PROPERTY_DVDCOPY_REGION</span><span class="sxs-lookup"><span data-stu-id="0b9e5-145">AM_PROPERTY_DVDCOPY_REGION</span></span></td>
<td><span data-ttu-id="0b9e5-146">Il codice dell'area richiede la definizione dell'area in cui il decodificatore può riprodurre come definito dal consorzio DVD.</span><span class="sxs-lookup"><span data-stu-id="0b9e5-146">Region code requests the region definition that the decoder is allowed to play in as defined by the DVD consortium.</span></span> <span data-ttu-id="0b9e5-147">Questa area è definita come <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-dvd_region"><strong>DVD_REGION</strong></a> struttura.</span><span class="sxs-lookup"><span data-stu-id="0b9e5-147">This region is defined as a <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-dvd_region"><strong>DVD_REGION</strong></a> structure.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0b9e5-148">AM_PROPERTY_DVDCOPY_SET_COPY_STATE</span><span class="sxs-lookup"><span data-stu-id="0b9e5-148">AM_PROPERTY_DVDCOPY_SET_COPY_STATE</span></span></td>
<td><span data-ttu-id="0b9e5-149">Sia get che set sono supportati in questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="0b9e5-149">Both get and set are supported on this property.</span></span> <span data-ttu-id="0b9e5-150">Get viene chiamato per primo per determinare se è necessaria l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="0b9e5-150">Get is called first to determine if authentication is required.</span></span> <span data-ttu-id="0b9e5-151">Le proprietà del set indicano la fase di negoziazione della protezione della copia in cui viene immesso il filtro.</span><span class="sxs-lookup"><span data-stu-id="0b9e5-151">The set properties are indications as to which phase of copy protection negotiation the filter is entering.</span></span> <span data-ttu-id="0b9e5-152">I dati passati saranno una struttura di tipo <a href="/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_dvdcopy_set_copy_state"><strong>AM_DVDCOPY_SET_COPY_STATE</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="0b9e5-152">The data passed will be a structure of type <a href="/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_dvdcopy_set_copy_state"><strong>AM_DVDCOPY_SET_COPY_STATE</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0b9e5-153">AM_PROPERTY_DVDCOPY_SUPPORTS_NEW_KEYCOUNT</span><span class="sxs-lookup"><span data-stu-id="0b9e5-153">AM_PROPERTY_DVDCOPY_SUPPORTS_NEW_KEYCOUNT</span></span></td>
<td><span data-ttu-id="0b9e5-154">Se questa proprietà è <strong>TRUE,</strong>lo strumento di navigazione DVD non invia AM_UseNewCSSKey <strong>esempi</strong> prima di negoziare la chiave del disco.</span><span class="sxs-lookup"><span data-stu-id="0b9e5-154">If this property is <strong>TRUE</strong>, the DVD Navigator does not send <strong>AM_UseNewCSSKey</strong> samples before negotiating the disc key.</span></span> <span data-ttu-id="0b9e5-155">Vedere <a href="/windows/win32/api/strmif/ns-strmif-am_sample2_properties"><strong>AM_SAMPLE2_PROPERTIES</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="0b9e5-155">See <a href="/windows/win32/api/strmif/ns-strmif-am_sample2_properties"><strong>AM_SAMPLE2_PROPERTIES</strong></a>.</span></span><br/> <span data-ttu-id="0b9e5-156">Di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="0b9e5-156">Read-only.</span></span> <span data-ttu-id="0b9e5-157">I dati della proprietà sono un <strong>valore BOOL.</strong></span><span class="sxs-lookup"><span data-stu-id="0b9e5-157">The property data is a <strong>BOOL</strong> value.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="0b9e5-158">Si applica a Windows 7.</span><span class="sxs-lookup"><span data-stu-id="0b9e5-158">Applies to Windows 7.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0b9e5-159">AM_PROPERTY_DVDCOPY_TITLE_KEY</span><span class="sxs-lookup"><span data-stu-id="0b9e5-159">AM_PROPERTY_DVDCOPY_TITLE_KEY</span></span></td>
<td><span data-ttu-id="0b9e5-160">Si tratta di una proprietà di sola impostazione.</span><span class="sxs-lookup"><span data-stu-id="0b9e5-160">This is a set-only property.</span></span> <span data-ttu-id="0b9e5-161">In questo modo viene fornita la chiave del titolo dal contenuto corrente.</span><span class="sxs-lookup"><span data-stu-id="0b9e5-161">This provides title key from current content.</span></span> <span data-ttu-id="0b9e5-162">La chiave è una struttura di tipo <a href="/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_dvdcopy_titlekey"><strong>AM_DVDCOPY_TITLEKEY</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="0b9e5-162">The key is a structure of type <a href="/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_dvdcopy_titlekey"><strong>AM_DVDCOPY_TITLEKEY</strong></a>.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="0b9e5-163">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0b9e5-163">Requirements</span></span>



| <span data-ttu-id="0b9e5-164">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b9e5-164">Requirement</span></span> | <span data-ttu-id="0b9e5-165">Valore</span><span class="sxs-lookup"><span data-stu-id="0b9e5-165">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0b9e5-166">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0b9e5-166">Header</span></span><br/> | <dl> <span data-ttu-id="0b9e5-167"><dt>Dvdmedia.h</dt></span><span class="sxs-lookup"><span data-stu-id="0b9e5-167"><dt>Dvdmedia.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b9e5-168">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0b9e5-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b9e5-169">Set di proprietà</span><span class="sxs-lookup"><span data-stu-id="0b9e5-169">Property Sets</span></span>](property-sets.md)
</dt> </dl>

 

 




