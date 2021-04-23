---
description: Le proprietà dell'immagine secondaria DVD controllano il colore, il contrasto e l'output della visualizzazione dell'immagine secondaria.
ms.assetid: ddbfb65c-7630-4e9f-8013-c5d65c62c628
title: Set di proprietà Dvd Subpicture (Dvdmedia.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a45b83595e8657ee0c60f39cd67f2d0e4c71511
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909089"
---
# <a name="dvd-subpicture-property-set"></a><span data-ttu-id="cd9ff-103">DVD Subpicture Property Set</span><span class="sxs-lookup"><span data-stu-id="cd9ff-103">DVD Subpicture Property Set</span></span>

<span data-ttu-id="cd9ff-104">Le proprietà dell'immagine secondaria DVD controllano il colore, il contrasto e l'output della visualizzazione dell'immagine secondaria.</span><span class="sxs-lookup"><span data-stu-id="cd9ff-104">DVD Subpicture properties control the color, contrast, and output of the subpicture display.</span></span>

<span data-ttu-id="cd9ff-105">Le informazioni seguenti presentano le costanti e i tipi di dati necessari da usare per questo set di proprietà nelle chiamate ai [**metodi IKsPropertySet.**](ikspropertyset.md)</span><span class="sxs-lookup"><span data-stu-id="cd9ff-105">The following information presents the necessary constants and data types to use for this property set in calls to [**IKsPropertySet**](ikspropertyset.md) methods.</span></span> <span data-ttu-id="cd9ff-106">Fornisce i valori per i **parametri GUID** (*guidPropSet*), ID proprietà (*dwPropID*) e tipo di dati della proprietà (*pPropData*).</span><span class="sxs-lookup"><span data-stu-id="cd9ff-106">It provides values for the **GUID** (*guidPropSet*), property ID (*dwPropID*), and property data type (*pPropData*) parameters.</span></span>



| <span data-ttu-id="cd9ff-107">Label</span><span class="sxs-lookup"><span data-stu-id="cd9ff-107">Label</span></span> | <span data-ttu-id="cd9ff-108">Valore</span><span class="sxs-lookup"><span data-stu-id="cd9ff-108">Value</span></span> |
|-------------------|----------------------------|
| <span data-ttu-id="cd9ff-109">GUID set di proprietà</span><span class="sxs-lookup"><span data-stu-id="cd9ff-109">Property Set GUID</span></span> | <span data-ttu-id="cd9ff-110">AM \_ KSPROPSETID \_ DvdSubPic</span><span class="sxs-lookup"><span data-stu-id="cd9ff-110">AM\_KSPROPSETID\_DvdSubPic</span></span> |



 



| <span data-ttu-id="cd9ff-111">ID proprietà</span><span class="sxs-lookup"><span data-stu-id="cd9ff-111">Property ID</span></span>                           | <span data-ttu-id="cd9ff-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cd9ff-112">Description</span></span>                                                                                                                                                                                                                                                                                                                                                              |
|---------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd9ff-113">AM \_ PROPERTY \_ DVDSUBPIC \_ COMPOSIT \_ ON</span><span class="sxs-lookup"><span data-stu-id="cd9ff-113">AM\_PROPERTY\_DVDSUBPIC\_COMPOSIT\_ON</span></span> | <span data-ttu-id="cd9ff-114">Proprietà di sola impostazione che abilita o disabilita la visualizzazione delle immagini secondarie.</span><span class="sxs-lookup"><span data-stu-id="cd9ff-114">Set-only property that enables or disables subpicture display.</span></span> <span data-ttu-id="cd9ff-115">DirectShow definisce il tipo di dati booleano **AM \_ PROPERTY COMPOSIT \_ \_ ON** per questa proprietà, nonché PAM PROPERTY COMPOSIT ON come puntatore \_ a questo tipo di \_ \_ dati.</span><span class="sxs-lookup"><span data-stu-id="cd9ff-115">DirectShow defines the **AM\_PROPERTY\_COMPOSIT\_ON** Boolean data type for this property, as well as PAM\_PROPERTY\_COMPOSIT\_ON as a pointer to this data type.</span></span> <span data-ttu-id="cd9ff-116">**TRUE** indica la visualizzazione dell'immagine secondaria, **FALSE** indica la disabilitazione.</span><span class="sxs-lookup"><span data-stu-id="cd9ff-116">**TRUE** indicates display the subpicture, **FALSE** indicates disable it.</span></span> <span data-ttu-id="cd9ff-117">Per altre informazioni, vedere la parte WDM di Windows DDK.</span><span class="sxs-lookup"><span data-stu-id="cd9ff-117">See the WDM portion of the Windows DDK for more information.</span></span> |
| <span data-ttu-id="cd9ff-118">PROPRIETÀ AM \_ \_ DVDSUBPIC \_ HLI</span><span class="sxs-lookup"><span data-stu-id="cd9ff-118">AM\_PROPERTY\_DVDSUBPIC\_HLI</span></span>          | <span data-ttu-id="cd9ff-119">Proprietà di sola impostazione che specifica un rettangolo di immagine secondaria o schermo il cui colore o contrasto verrà modificato.</span><span class="sxs-lookup"><span data-stu-id="cd9ff-119">Set-only property that specifies a rectangle of subpicture or screen whose color or contrast will be changed.</span></span> <span data-ttu-id="cd9ff-120">Il tipo di dati [**è AM \_ PROPERTY \_ SPHLI.**](/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_property_sphli)</span><span class="sxs-lookup"><span data-stu-id="cd9ff-120">Data type is [**AM\_PROPERTY\_SPHLI**](/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_property_sphli).</span></span> <span data-ttu-id="cd9ff-121">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="cd9ff-121">See Remarks.</span></span>                                                                                                                                                                                |
| <span data-ttu-id="cd9ff-122">PROPRIETÀ AM \_ \_ DVDSUBPIC \_ PALETTE</span><span class="sxs-lookup"><span data-stu-id="cd9ff-122">AM\_PROPERTY\_DVDSUBPIC\_PALETTE</span></span>      | <span data-ttu-id="cd9ff-123">Imposta la tavolozza per un'immagine secondaria.</span><span class="sxs-lookup"><span data-stu-id="cd9ff-123">Sets the palette for a subpicture.</span></span> <span data-ttu-id="cd9ff-124">Il tipo di dati [**è AM \_ PROPERTY \_ SPPAL.**](/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_property_sppal)</span><span class="sxs-lookup"><span data-stu-id="cd9ff-124">Data type is [**AM\_PROPERTY\_SPPAL**](/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_property_sppal).</span></span>                                                                                                                                                                                                                                                                        |



 

## <a name="remarks"></a><span data-ttu-id="cd9ff-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="cd9ff-125">Remarks</span></span>

<span data-ttu-id="cd9ff-126">La **proprietà AM PROPERTY \_ \_ DVDSUBPIC \_ HLI** è di sola impostazione.</span><span class="sxs-lookup"><span data-stu-id="cd9ff-126">The **AM\_PROPERTY\_DVDSUBPIC\_HLI** property is set-only.</span></span> <span data-ttu-id="cd9ff-127">Specifica un rettangolo di immagine secondaria o schermo il cui colore o contrasto verrà modificato.</span><span class="sxs-lookup"><span data-stu-id="cd9ff-127">It specifies a rectangle of subpicture or screen whose color or contrast will be changed.</span></span> <span data-ttu-id="cd9ff-128">Ciò differisce dalla specifica DVD-Video, in cui lo strumento di navigazione DVD Microsoft analizza tutte le informazioni su pulsanti e tastiera e passa un solo rettangolo di evidenziazione al decodificatore di immagini secondarie in un determinato momento.</span><span class="sxs-lookup"><span data-stu-id="cd9ff-128">This differs from the DVD-Video specification, in that the Microsoft DVD navigator parses all button and keyboard information and passes only one highlight rectangle to the subpicture decoder at any given time.</span></span> <span data-ttu-id="cd9ff-129">Di conseguenza, le informazioni di evidenziazione vengono inviate al decodificatore più spesso di quanto non sia presente nel flusso DVD.</span><span class="sxs-lookup"><span data-stu-id="cd9ff-129">As a result, highlight information is sent to the decoder more often than it is present in the DVD stream.</span></span>

<span data-ttu-id="cd9ff-130">Le informazioni di evidenziazione arrivano in modo asincrono al flusso di dati.</span><span class="sxs-lookup"><span data-stu-id="cd9ff-130">The highlight information arrives asynchronously to the data stream.</span></span> <span data-ttu-id="cd9ff-131">Il decodificatore usa gli indicatori di ora di inizio e fine evidenziati per correlare le informazioni di evidenziazione alle informazioni sull'immagine secondaria pertinente, se presenti.</span><span class="sxs-lookup"><span data-stu-id="cd9ff-131">The decoder uses the highlight Start and End time stamps to correlate the highlight information to the relevant subpicture information, if any.</span></span> <span data-ttu-id="cd9ff-132">Se il decodificatore non ha ricevuto informazioni sul flusso di immagini secondarie per i timestamp richiesti, il decodificatore presuppone che le informazioni di evidenziazione siano autonome e non si applicano a un'immagine secondaria.</span><span class="sxs-lookup"><span data-stu-id="cd9ff-132">If the decoder has not received any subpicture stream information for the requested time stamps, the decoder assumes that the highlight information is stand-alone and does not apply to a subpicture.</span></span> <span data-ttu-id="cd9ff-133">In questo caso, il decodificatore presuppone che le informazioni sul colore e sul contrasto siano tutte dello stesso colore.</span><span class="sxs-lookup"><span data-stu-id="cd9ff-133">In this case, the decoder assumes the color and contrast information is all the same color.</span></span>

<span data-ttu-id="cd9ff-134">I dati non sono interamente in formato disco DVD.</span><span class="sxs-lookup"><span data-stu-id="cd9ff-134">The data is not entirely in DVD disc format.</span></span> <span data-ttu-id="cd9ff-135">Microsoft fornisce una struttura aggiuntiva di [**tipo AM \_ PROPERTY \_ SPHLI**](/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_property_sphli) che viene passata come parametro a questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="cd9ff-135">Microsoft provides an additional structure of type [**AM\_PROPERTY\_SPHLI**](/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_property_sphli) that is passed as the parameter to this property.</span></span> <span data-ttu-id="cd9ff-136">Questa struttura descrive il pulsante attualmente selezionato dalle informazioni di evidenziazione dvd.</span><span class="sxs-lookup"><span data-stu-id="cd9ff-136">This structure describes the currently selected button from the DVD highlight information.</span></span>

<span data-ttu-id="cd9ff-137">Lo strumento di spostamento DVD elabora tutte le informazioni sulla sequenza di tasti e invia nuove informazioni di evidenziazione ogni volta che cambia lo stato di un pulsante.</span><span class="sxs-lookup"><span data-stu-id="cd9ff-137">The DVD navigator processes all keystroke information and sends new highlight information each time a button state changes.</span></span> <span data-ttu-id="cd9ff-138">Le informazioni descrivono una sola modalità di un pulsante alla volta.</span><span class="sxs-lookup"><span data-stu-id="cd9ff-138">The information describes only one mode of one button at a time.</span></span> <span data-ttu-id="cd9ff-139">Include un rettangolo di visualizzazione in coordinate pixel dello schermo o una visualizzazione dell'immagine secondaria, se presente.</span><span class="sxs-lookup"><span data-stu-id="cd9ff-139">It includes a display rectangle in pixel coordinates of the screen, or a display of the subpicture, if present.</span></span> <span data-ttu-id="cd9ff-140">La struttura contiene anche informazioni sul colore e sul contrasto, ma solo per lo stato corrente del pulsante attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="cd9ff-140">The structure also contains color and contrast information, but only for the present state of the currently selected button.</span></span> <span data-ttu-id="cd9ff-141">Il formato è definito nella specifica DVD.</span><span class="sxs-lookup"><span data-stu-id="cd9ff-141">The format is defined in the DVD specification.</span></span>

<span data-ttu-id="cd9ff-142">Le informazioni di evidenziazione contengono timestamp di inizio e fine.</span><span class="sxs-lookup"><span data-stu-id="cd9ff-142">Highlight information contains Start and End time stamps.</span></span> <span data-ttu-id="cd9ff-143">Queste sono nelle stesse unità degli altri timestamp, con due eccezioni: un timestamp di inizio di 0xFFFFFFFF indica che la proprietà highlight è valida al momento della ricezione e un timestamp di fine di 0xFFFFFFFF indica che la proprietà highlight è valida fino all'evidenziazione successiva ricevuta.</span><span class="sxs-lookup"><span data-stu-id="cd9ff-143">These are in the same units as other time stamps, with two exceptions: A Start time stamp of 0xFFFFFFFF means the highlight property is effective upon receipt, and an End time stamp of 0xFFFFFFFF means the highlight property is valid until next highlight received.</span></span>

<span data-ttu-id="cd9ff-144">Il campo HLISS è definito nella specifica DVD.</span><span class="sxs-lookup"><span data-stu-id="cd9ff-144">The HLISS field is as defined in the DVD specification.</span></span> <span data-ttu-id="cd9ff-145">Il valore zero indica che tutte le evidenziazioni non sono valide e che il decodificatore deve disabilitare tutte le evidenziazioni.</span><span class="sxs-lookup"><span data-stu-id="cd9ff-145">A value of zero indicates that all highlights are invalid and the decoder should disable all highlights.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd9ff-146">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cd9ff-146">Requirements</span></span>



| <span data-ttu-id="cd9ff-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd9ff-147">Requirement</span></span> | <span data-ttu-id="cd9ff-148">Valore</span><span class="sxs-lookup"><span data-stu-id="cd9ff-148">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cd9ff-149">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cd9ff-149">Header</span></span><br/> | <dl> <span data-ttu-id="cd9ff-150"><dt>Dvdmedia.h</dt></span><span class="sxs-lookup"><span data-stu-id="cd9ff-150"><dt>Dvdmedia.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd9ff-151">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cd9ff-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd9ff-152">Set di proprietà</span><span class="sxs-lookup"><span data-stu-id="cd9ff-152">Property Sets</span></span>](property-sets.md)
</dt> </dl>

 

 




