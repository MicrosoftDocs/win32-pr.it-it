---
description: Il set di proprietà di protezione copia DVD fornisce l'autenticazione delle informazioni di protezione copia da decrittografia hardware o software. Usare questa proprietà impostata per impedire la copia non autorizzata da DVD-video preregistrato.
ms.assetid: da3abefd-8f25-449d-8787-84d2cef928da
title: Set di proprietà DVD Copy Protection (Dvdmedia.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a14146ce0be19a4ed49c23517987a2c91a85da87
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331637"
---
# <a name="dvd-copy-protection-property-set"></a><span data-ttu-id="a802d-104">Set di proprietà di protezione copia DVD</span><span class="sxs-lookup"><span data-stu-id="a802d-104">DVD Copy Protection Property Set</span></span>

<span data-ttu-id="a802d-105">Il set di proprietà di protezione copia DVD fornisce l'autenticazione delle informazioni di protezione copia da decrittografia hardware o software.</span><span class="sxs-lookup"><span data-stu-id="a802d-105">The DVD Copy Protection property set provides authentication of copy protection information from hardware or software decrypters.</span></span> <span data-ttu-id="a802d-106">Usare questa proprietà impostata per impedire la copia non autorizzata da DVD-video preregistrato.</span><span class="sxs-lookup"><span data-stu-id="a802d-106">Use this property set to prevent unauthorized copying from prerecorded DVD-Video.</span></span>

<span data-ttu-id="a802d-107">Microsoft fornisce software che facilita il processo di autenticazione richiesto dallo schema di crittografia, consentendo in tal modo a un'unità DVD-ROM di autenticare e trasferire le chiavi con un DVD Decrypter.</span><span class="sxs-lookup"><span data-stu-id="a802d-107">Microsoft provides software that facilitates the authentication process required by the encryption scheme, thus enabling a DVD-ROM drive to authenticate and transfer keys with a DVD decrypter.</span></span> <span data-ttu-id="a802d-108">Microsoft non prevede alcun piano per la distribuzione di un DVD Decrypter e, al contrario, fornisce codice del sistema operativo che fungerà da agente per consentire l'autenticazione di decrittografia hardware o software.</span><span class="sxs-lookup"><span data-stu-id="a802d-108">Microsoft has no current plans to ship a DVD decrypter and, instead, is providing operating system code that will act as the agent to enable authentication of either hardware or software decrypters.</span></span>

<span data-ttu-id="a802d-109">Il navigatore DVD avvia e controlla il processo di scambio delle chiavi.</span><span class="sxs-lookup"><span data-stu-id="a802d-109">The DVD navigator initiates and controls the key exchange process.</span></span> <span data-ttu-id="a802d-110">Il minidriver DVD richiede solo l'implementazione delle proprietà seguenti.</span><span class="sxs-lookup"><span data-stu-id="a802d-110">The DVD minidriver needs only to implement the following properties.</span></span> <span data-ttu-id="a802d-111">Altri componenti gestiscono il resto.</span><span class="sxs-lookup"><span data-stu-id="a802d-111">Other components handle the rest.</span></span>

<span data-ttu-id="a802d-112">Ogni flusso di input DVD riceverà le proprietà di protezione della copia.</span><span class="sxs-lookup"><span data-stu-id="a802d-112">Each DVD input stream will receive copy protection properties.</span></span> <span data-ttu-id="a802d-113">Questo vale anche se lo stesso hardware controlla tutti i flussi DVD.</span><span class="sxs-lookup"><span data-stu-id="a802d-113">This is true even if the same hardware controls all DVD streams.</span></span>

<span data-ttu-id="a802d-114">Le informazioni seguenti presentano le costanti e i tipi di dati necessari da usare per questa proprietà impostata nelle chiamate ai metodi [**IKsPropertySet**](ikspropertyset.md) .</span><span class="sxs-lookup"><span data-stu-id="a802d-114">The following information presents the necessary constants and data types to use for this property set in calls to [**IKsPropertySet**](ikspropertyset.md) methods.</span></span> <span data-ttu-id="a802d-115">Fornisce valori per i parametri **GUID** (*GUIDPROPSET*), ID proprietà (*dwPropID*) e tipo di dati Property (*pPropData*).</span><span class="sxs-lookup"><span data-stu-id="a802d-115">It provides values for the **GUID** (*guidPropSet*), property ID (*dwPropID*), and property data type (*pPropData*) parameters.</span></span>



|                   |                           |
|-------------------|---------------------------|
| <span data-ttu-id="a802d-116">GUID set di proprietà</span><span class="sxs-lookup"><span data-stu-id="a802d-116">Property Set GUID</span></span> | <span data-ttu-id="a802d-117">\_CopyProt KSPROPSETID \_</span><span class="sxs-lookup"><span data-stu-id="a802d-117">AM\_KSPROPSETID\_CopyProt</span></span> |



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a802d-118">ID proprietà</span><span class="sxs-lookup"><span data-stu-id="a802d-118">Property ID</span></span></th>
<th><span data-ttu-id="a802d-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a802d-119">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a802d-120"><a href="am-property-copy-analog-component-property.md"><strong>AM_PROPERTY_COPY_ANALOG_COMPONENT</strong></a></span><span class="sxs-lookup"><span data-stu-id="a802d-120"><a href="am-property-copy-analog-component-property.md"><strong>AM_PROPERTY_COPY_ANALOG_COMPONENT</strong></a></span></span></td>
<td><span data-ttu-id="a802d-121">Esegue una query per verificare se l'output del video è una definizione standard, ovvero un video componente analogico.</span><span class="sxs-lookup"><span data-stu-id="a802d-121">Queries whether the video output is standard-definition, analog component video.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a802d-122">AM_PROPERTY_COPY_MACROVISION</span><span class="sxs-lookup"><span data-stu-id="a802d-122">AM_PROPERTY_COPY_MACROVISION</span></span></td>
<td><span data-ttu-id="a802d-123">Si tratta di una proprietà di sola impostazione.</span><span class="sxs-lookup"><span data-stu-id="a802d-123">This is a set-only property.</span></span> <span data-ttu-id="a802d-124">Questa proprietà imposta il livello di protezione per la copia analogico per il codificatore NTSC nell'output finale del PIN di destinazione.</span><span class="sxs-lookup"><span data-stu-id="a802d-124">This property sets the analog copy protection level for the NTSC encoder on the output end of the receiving pin.</span></span> <span data-ttu-id="a802d-125">USA <a href="/previous-versions/ms778996(v=vs.85)"><strong>AM_COPY_MACROVISION</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="a802d-125">Uses <a href="/previous-versions/ms778996(v=vs.85)"><strong>AM_COPY_MACROVISION</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a802d-126">AM_PROPERTY_DVDCOPY_CHLG_KEY</span><span class="sxs-lookup"><span data-stu-id="a802d-126">AM_PROPERTY_DVDCOPY_CHLG_KEY</span></span></td>
<td><span data-ttu-id="a802d-127">In questa proprietà sono supportate entrambe le operazioni get e set.</span><span class="sxs-lookup"><span data-stu-id="a802d-127">Both get and set operations are supported on this property.</span></span> <span data-ttu-id="a802d-128">Un'operazione Get richiede al decodificatore di fornire la chiave di richiesta del bus.</span><span class="sxs-lookup"><span data-stu-id="a802d-128">A get operation requests the decoder to provide its bus challenge key.</span></span> <span data-ttu-id="a802d-129">Un'operazione di impostazione fornisce al decodificatore la chiave della richiesta bus dall'unità DVD.</span><span class="sxs-lookup"><span data-stu-id="a802d-129">A set operation provides the decoder with the bus challenge key from the DVD drive.</span></span> <span data-ttu-id="a802d-130">I dati passati in questa proprietà saranno una struttura di tipo <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_chlgkey"><strong>AM_DVDCOPY_CHLGKEY</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="a802d-130">The data passed in this property will be a structure of type <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_chlgkey"><strong>AM_DVDCOPY_CHLGKEY</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a802d-131">AM_PROPERTY_DVDCOPY_DEC_KEY2</span><span class="sxs-lookup"><span data-stu-id="a802d-131">AM_PROPERTY_DVDCOPY_DEC_KEY2</span></span></td>
<td><span data-ttu-id="a802d-132">Si tratta di una proprietà di solo Get.</span><span class="sxs-lookup"><span data-stu-id="a802d-132">This is a get-only property.</span></span> <span data-ttu-id="a802d-133">Questa proprietà richiede che la chiave bus del decodificatore 2 venga trasferita all'unità DVD.</span><span class="sxs-lookup"><span data-stu-id="a802d-133">This property requests that the decoder's bus key 2 be transferred to the DVD drive.</span></span> <span data-ttu-id="a802d-134">I dati passati saranno una struttura di tipo <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_buskey"><strong>AM_DVDCOPY_BUSKEY</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="a802d-134">The data passed will be a structure of type <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_buskey"><strong>AM_DVDCOPY_BUSKEY</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a802d-135">AM_PROPERTY_DVDCOPY_DISC_KEY</span><span class="sxs-lookup"><span data-stu-id="a802d-135">AM_PROPERTY_DVDCOPY_DISC_KEY</span></span></td>
<td><span data-ttu-id="a802d-136">Proprietà di sola impostazione.</span><span class="sxs-lookup"><span data-stu-id="a802d-136">Set-only property.</span></span> <span data-ttu-id="a802d-137">Questa operazione fornisce la chiave del disco.</span><span class="sxs-lookup"><span data-stu-id="a802d-137">This provides disc key.</span></span> <span data-ttu-id="a802d-138">La chiave è una struttura di tipo <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_disckey"><strong>AM_DVDCOPY_DISCKEY</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="a802d-138">The key is a structure of type <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_disckey"><strong>AM_DVDCOPY_DISCKEY</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a802d-139">AM_PROPERTY_DVDCOPY_DVD_KEY1</span><span class="sxs-lookup"><span data-stu-id="a802d-139">AM_PROPERTY_DVDCOPY_DVD_KEY1</span></span></td>
<td><span data-ttu-id="a802d-140">Si tratta di una proprietà di sola impostazione.</span><span class="sxs-lookup"><span data-stu-id="a802d-140">This is a set-only property.</span></span> <span data-ttu-id="a802d-141">Questa proprietà fornisce la chiave del bus di unità DVD 1 al decodificatore.</span><span class="sxs-lookup"><span data-stu-id="a802d-141">This property provides the DVD drive bus key 1 to the decoder.</span></span> <span data-ttu-id="a802d-142">I dati passati saranno una struttura di tipo <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_buskey"><strong>AM_DVDCOPY_BUSKEY</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="a802d-142">The data passed will be a structure of type <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_buskey"><strong>AM_DVDCOPY_BUSKEY</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a802d-143">AM_PROPERTY_DVDCOPY_REGION</span><span class="sxs-lookup"><span data-stu-id="a802d-143">AM_PROPERTY_DVDCOPY_REGION</span></span></td>
<td><span data-ttu-id="a802d-144">Il codice dell'area richiede la definizione dell'area in cui è consentita la riproduzione del decodificatore come definito dal DVD Consortium.</span><span class="sxs-lookup"><span data-stu-id="a802d-144">Region code requests the region definition that the decoder is allowed to play in as defined by the DVD consortium.</span></span> <span data-ttu-id="a802d-145">Questa area è definita come struttura di <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-dvd_region"><strong>DVD_REGION</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="a802d-145">This region is defined as a <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-dvd_region"><strong>DVD_REGION</strong></a> structure.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a802d-146">AM_PROPERTY_DVDCOPY_SET_COPY_STATE</span><span class="sxs-lookup"><span data-stu-id="a802d-146">AM_PROPERTY_DVDCOPY_SET_COPY_STATE</span></span></td>
<td><span data-ttu-id="a802d-147">In questa proprietà sono supportati sia get che set.</span><span class="sxs-lookup"><span data-stu-id="a802d-147">Both get and set are supported on this property.</span></span> <span data-ttu-id="a802d-148">Get viene chiamato per primo per determinare se l'autenticazione è obbligatoria.</span><span class="sxs-lookup"><span data-stu-id="a802d-148">Get is called first to determine if authentication is required.</span></span> <span data-ttu-id="a802d-149">Le proprietà del set sono indicazioni sulla fase di negoziazione della protezione da copia del filtro.</span><span class="sxs-lookup"><span data-stu-id="a802d-149">The set properties are indications as to which phase of copy protection negotiation the filter is entering.</span></span> <span data-ttu-id="a802d-150">I dati passati saranno una struttura di tipo <a href="/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_dvdcopy_set_copy_state"><strong>AM_DVDCOPY_SET_COPY_STATE</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="a802d-150">The data passed will be a structure of type <a href="/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_dvdcopy_set_copy_state"><strong>AM_DVDCOPY_SET_COPY_STATE</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a802d-151">AM_PROPERTY_DVDCOPY_SUPPORTS_NEW_KEYCOUNT</span><span class="sxs-lookup"><span data-stu-id="a802d-151">AM_PROPERTY_DVDCOPY_SUPPORTS_NEW_KEYCOUNT</span></span></td>
<td><span data-ttu-id="a802d-152">Se questa proprietà è <strong>true</strong>, il NAVIGAtore DVD non invia <strong>AM_UseNewCSSKey</strong> esempi prima di negoziare la chiave del disco.</span><span class="sxs-lookup"><span data-stu-id="a802d-152">If this property is <strong>TRUE</strong>, the DVD Navigator does not send <strong>AM_UseNewCSSKey</strong> samples before negotiating the disc key.</span></span> <span data-ttu-id="a802d-153">Vedere <a href="/windows/win32/api/strmif/ns-strmif-am_sample2_properties"><strong>AM_SAMPLE2_PROPERTIES</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="a802d-153">See <a href="/windows/win32/api/strmif/ns-strmif-am_sample2_properties"><strong>AM_SAMPLE2_PROPERTIES</strong></a>.</span></span><br/> <span data-ttu-id="a802d-154">Di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="a802d-154">Read-only.</span></span> <span data-ttu-id="a802d-155">I dati della proprietà sono un valore <strong>bool</strong> .</span><span class="sxs-lookup"><span data-stu-id="a802d-155">The property data is a <strong>BOOL</strong> value.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="a802d-156">Si applica a Windows 7.</span><span class="sxs-lookup"><span data-stu-id="a802d-156">Applies to Windows 7.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a802d-157">AM_PROPERTY_DVDCOPY_TITLE_KEY</span><span class="sxs-lookup"><span data-stu-id="a802d-157">AM_PROPERTY_DVDCOPY_TITLE_KEY</span></span></td>
<td><span data-ttu-id="a802d-158">Si tratta di una proprietà di sola impostazione.</span><span class="sxs-lookup"><span data-stu-id="a802d-158">This is a set-only property.</span></span> <span data-ttu-id="a802d-159">Questa operazione fornisce la chiave del titolo del contenuto corrente.</span><span class="sxs-lookup"><span data-stu-id="a802d-159">This provides title key from current content.</span></span> <span data-ttu-id="a802d-160">La chiave è una struttura di tipo <a href="/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_dvdcopy_titlekey"><strong>AM_DVDCOPY_TITLEKEY</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="a802d-160">The key is a structure of type <a href="/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_dvdcopy_titlekey"><strong>AM_DVDCOPY_TITLEKEY</strong></a>.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="a802d-161">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a802d-161">Requirements</span></span>



| <span data-ttu-id="a802d-162">Requisito</span><span class="sxs-lookup"><span data-stu-id="a802d-162">Requirement</span></span> | <span data-ttu-id="a802d-163">Valore</span><span class="sxs-lookup"><span data-stu-id="a802d-163">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a802d-164">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a802d-164">Header</span></span><br/> | <dl> <span data-ttu-id="a802d-165"><dt>Dvdmedia. h</dt></span><span class="sxs-lookup"><span data-stu-id="a802d-165"><dt>Dvdmedia.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a802d-166">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a802d-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a802d-167">Set di proprietà</span><span class="sxs-lookup"><span data-stu-id="a802d-167">Property Sets</span></span>](property-sets.md)
</dt> </dl>

 

 




