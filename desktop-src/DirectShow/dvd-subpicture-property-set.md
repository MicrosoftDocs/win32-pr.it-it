---
description: Le proprietà del sottoimmagine DVD controllano il colore, il contrasto e l'output della visualizzazione dell'immagine.
ms.assetid: ddbfb65c-7630-4e9f-8013-c5d65c62c628
title: Set di proprietà della sottoimmagine DVD (dvdmedia. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac2706bd0a7f078fb7352e70e8f8eb62f5dea948
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329263"
---
# <a name="dvd-subpicture-property-set"></a><span data-ttu-id="83812-103">Set di proprietà della sottoimmagine DVD</span><span class="sxs-lookup"><span data-stu-id="83812-103">DVD Subpicture Property Set</span></span>

<span data-ttu-id="83812-104">Le proprietà del sottoimmagine DVD controllano il colore, il contrasto e l'output della visualizzazione dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="83812-104">DVD Subpicture properties control the color, contrast, and output of the subpicture display.</span></span>

<span data-ttu-id="83812-105">Le informazioni seguenti presentano le costanti e i tipi di dati necessari da usare per questa proprietà impostata nelle chiamate ai metodi [**IKsPropertySet**](ikspropertyset.md) .</span><span class="sxs-lookup"><span data-stu-id="83812-105">The following information presents the necessary constants and data types to use for this property set in calls to [**IKsPropertySet**](ikspropertyset.md) methods.</span></span> <span data-ttu-id="83812-106">Fornisce valori per i parametri **GUID** (*GUIDPROPSET*), ID proprietà (*dwPropID*) e tipo di dati Property (*pPropData*).</span><span class="sxs-lookup"><span data-stu-id="83812-106">It provides values for the **GUID** (*guidPropSet*), property ID (*dwPropID*), and property data type (*pPropData*) parameters.</span></span>



|                   |                            |
|-------------------|----------------------------|
| <span data-ttu-id="83812-107">GUID set di proprietà</span><span class="sxs-lookup"><span data-stu-id="83812-107">Property Set GUID</span></span> | <span data-ttu-id="83812-108">\_DvdSubPic KSPROPSETID \_</span><span class="sxs-lookup"><span data-stu-id="83812-108">AM\_KSPROPSETID\_DvdSubPic</span></span> |



 



| <span data-ttu-id="83812-109">ID proprietà</span><span class="sxs-lookup"><span data-stu-id="83812-109">Property ID</span></span>                           | <span data-ttu-id="83812-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="83812-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                              |
|---------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="83812-111">\_Proprietà am \_ DVDSUBPIC \_ composizione \_ su</span><span class="sxs-lookup"><span data-stu-id="83812-111">AM\_PROPERTY\_DVDSUBPIC\_COMPOSIT\_ON</span></span> | <span data-ttu-id="83812-112">Proprietà di sola impostazione che Abilita o Disabilita la visualizzazione dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="83812-112">Set-only property that enables or disables subpicture display.</span></span> <span data-ttu-id="83812-113">DirectShow definisce la **\_ Proprietà am \_ composita \_ sul** tipo di dati booleano per questa proprietà, nonché la \_ Proprietà PAM \_ composita \_ in come puntatore a questo tipo di dati.</span><span class="sxs-lookup"><span data-stu-id="83812-113">DirectShow defines the **AM\_PROPERTY\_COMPOSIT\_ON** Boolean data type for this property, as well as PAM\_PROPERTY\_COMPOSIT\_ON as a pointer to this data type.</span></span> <span data-ttu-id="83812-114">**True** indica che viene visualizzata la sottoimmagine, **false** indica che è disabilitata.</span><span class="sxs-lookup"><span data-stu-id="83812-114">**TRUE** indicates display the subpicture, **FALSE** indicates disable it.</span></span> <span data-ttu-id="83812-115">Per ulteriori informazioni, vedere la parte WDM del DDK di Windows.</span><span class="sxs-lookup"><span data-stu-id="83812-115">See the WDM portion of the Windows DDK for more information.</span></span> |
| <span data-ttu-id="83812-116">\_Proprietà am \_ DVDSUBPIC \_ HLI</span><span class="sxs-lookup"><span data-stu-id="83812-116">AM\_PROPERTY\_DVDSUBPIC\_HLI</span></span>          | <span data-ttu-id="83812-117">Proprietà set-only che specifica un rettangolo di subimmagine o schermata il cui colore o contrasto verrà modificato.</span><span class="sxs-lookup"><span data-stu-id="83812-117">Set-only property that specifies a rectangle of subpicture or screen whose color or contrast will be changed.</span></span> <span data-ttu-id="83812-118">Il tipo di dati è [**\_ \_ SPHLI Property**](/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_property_sphli).</span><span class="sxs-lookup"><span data-stu-id="83812-118">Data type is [**AM\_PROPERTY\_SPHLI**](/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_property_sphli).</span></span> <span data-ttu-id="83812-119">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="83812-119">See Remarks.</span></span>                                                                                                                                                                                |
| <span data-ttu-id="83812-120">\_ \_ tavolozza DVDSUBPIC della proprietà am \_</span><span class="sxs-lookup"><span data-stu-id="83812-120">AM\_PROPERTY\_DVDSUBPIC\_PALETTE</span></span>      | <span data-ttu-id="83812-121">Imposta la tavolozza per un'immagine.</span><span class="sxs-lookup"><span data-stu-id="83812-121">Sets the palette for a subpicture.</span></span> <span data-ttu-id="83812-122">Il tipo di dati è [**\_ \_ SPPAL Property**](/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_property_sppal).</span><span class="sxs-lookup"><span data-stu-id="83812-122">Data type is [**AM\_PROPERTY\_SPPAL**](/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_property_sppal).</span></span>                                                                                                                                                                                                                                                                        |



 

## <a name="remarks"></a><span data-ttu-id="83812-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="83812-123">Remarks</span></span>

<span data-ttu-id="83812-124">La **proprietà \_ am \_ DVDSUBPIC \_ HLI** è impostata su Only.</span><span class="sxs-lookup"><span data-stu-id="83812-124">The **AM\_PROPERTY\_DVDSUBPIC\_HLI** property is set-only.</span></span> <span data-ttu-id="83812-125">Specifica un rettangolo di subimmagine o schermata il cui colore o contrasto verrà modificato.</span><span class="sxs-lookup"><span data-stu-id="83812-125">It specifies a rectangle of subpicture or screen whose color or contrast will be changed.</span></span> <span data-ttu-id="83812-126">Questo comportamento è diverso da quello della specifica DVD-Video, in quanto il navigatore DVD di Microsoft analizza tutte le informazioni sul pulsante e sulla tastiera e passa un solo rettangolo di evidenziazione al decodificatore dell'immagine in un determinato momento.</span><span class="sxs-lookup"><span data-stu-id="83812-126">This differs from the DVD-Video specification, in that the Microsoft DVD navigator parses all button and keyboard information and passes only one highlight rectangle to the subpicture decoder at any given time.</span></span> <span data-ttu-id="83812-127">Di conseguenza, le informazioni sull'evidenziazione vengono inviate al decodificatore più spesso di quanto sia presente nel flusso di DVD.</span><span class="sxs-lookup"><span data-stu-id="83812-127">As a result, highlight information is sent to the decoder more often than it is present in the DVD stream.</span></span>

<span data-ttu-id="83812-128">Le informazioni di evidenziazione arrivano in modo asincrono al flusso di dati.</span><span class="sxs-lookup"><span data-stu-id="83812-128">The highlight information arrives asynchronously to the data stream.</span></span> <span data-ttu-id="83812-129">Il decodificatore usa i timestamp di inizio e fine dell'evidenziazione per correlare le informazioni di evidenziazione alle informazioni relative all'immagine, se presenti.</span><span class="sxs-lookup"><span data-stu-id="83812-129">The decoder uses the highlight Start and End time stamps to correlate the highlight information to the relevant subpicture information, if any.</span></span> <span data-ttu-id="83812-130">Se il decodificatore non ha ricevuto informazioni sul flusso di sottoimmagine per i timestamp richiesti, il decodificatore presuppone che le informazioni di evidenziazione siano autonome e non si applichino a un'immagine.</span><span class="sxs-lookup"><span data-stu-id="83812-130">If the decoder has not received any subpicture stream information for the requested time stamps, the decoder assumes that the highlight information is stand-alone and does not apply to a subpicture.</span></span> <span data-ttu-id="83812-131">In questo caso, il decodificatore presuppone che il colore e le informazioni sul contrasto siano tutti dello stesso colore.</span><span class="sxs-lookup"><span data-stu-id="83812-131">In this case, the decoder assumes the color and contrast information is all the same color.</span></span>

<span data-ttu-id="83812-132">I dati non sono interamente in formato DVD.</span><span class="sxs-lookup"><span data-stu-id="83812-132">The data is not entirely in DVD disc format.</span></span> <span data-ttu-id="83812-133">Microsoft fornisce una struttura aggiuntiva di tipo [**am \_ Property \_ SPHLI**](/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_property_sphli) che viene passata come parametro a questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="83812-133">Microsoft provides an additional structure of type [**AM\_PROPERTY\_SPHLI**](/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_property_sphli) that is passed as the parameter to this property.</span></span> <span data-ttu-id="83812-134">Questa struttura descrive il pulsante attualmente selezionato dalle informazioni di evidenziazione del DVD.</span><span class="sxs-lookup"><span data-stu-id="83812-134">This structure describes the currently selected button from the DVD highlight information.</span></span>

<span data-ttu-id="83812-135">Il navigatore DVD elabora tutte le informazioni sulla sequenza di tasti e invia nuove informazioni di evidenziazione ogni volta che viene modificato lo stato di un pulsante.</span><span class="sxs-lookup"><span data-stu-id="83812-135">The DVD navigator processes all keystroke information and sends new highlight information each time a button state changes.</span></span> <span data-ttu-id="83812-136">Le informazioni descrivono solo una modalità di un pulsante alla volta.</span><span class="sxs-lookup"><span data-stu-id="83812-136">The information describes only one mode of one button at a time.</span></span> <span data-ttu-id="83812-137">Include un rettangolo di visualizzazione nelle coordinate dei pixel dello schermo o una visualizzazione dell'immagine, se presente.</span><span class="sxs-lookup"><span data-stu-id="83812-137">It includes a display rectangle in pixel coordinates of the screen, or a display of the subpicture, if present.</span></span> <span data-ttu-id="83812-138">La struttura contiene anche informazioni sul colore e sul contrasto, ma solo per lo stato attuale del pulsante attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="83812-138">The structure also contains color and contrast information, but only for the present state of the currently selected button.</span></span> <span data-ttu-id="83812-139">Il formato è definito nella specifica DVD.</span><span class="sxs-lookup"><span data-stu-id="83812-139">The format is defined in the DVD specification.</span></span>

<span data-ttu-id="83812-140">Le informazioni relative all'evidenziazione contengono timestamp di inizio e di fine.</span><span class="sxs-lookup"><span data-stu-id="83812-140">Highlight information contains Start and End time stamps.</span></span> <span data-ttu-id="83812-141">Si trovano nelle stesse unità di altri timestamp, con due eccezioni: un timestamp di inizio di 0xFFFFFFFF indica che la proprietà Highlight è valida al momento della ricezione e un timestamp di fine 0xFFFFFFFF indica che la proprietà Highlight è valida fino a quando non viene ricevuta l'evidenziazione successiva.</span><span class="sxs-lookup"><span data-stu-id="83812-141">These are in the same units as other time stamps, with two exceptions: A Start time stamp of 0xFFFFFFFF means the highlight property is effective upon receipt, and an End time stamp of 0xFFFFFFFF means the highlight property is valid until next highlight received.</span></span>

<span data-ttu-id="83812-142">Il campo HLISS è definito nella specifica DVD.</span><span class="sxs-lookup"><span data-stu-id="83812-142">The HLISS field is as defined in the DVD specification.</span></span> <span data-ttu-id="83812-143">Un valore pari a zero indica che tutte le evidenziazioni non sono valide e che il decodificatore deve disabilitare tutte le evidenziazioni.</span><span class="sxs-lookup"><span data-stu-id="83812-143">A value of zero indicates that all highlights are invalid and the decoder should disable all highlights.</span></span>

## <a name="requirements"></a><span data-ttu-id="83812-144">Requisiti</span><span class="sxs-lookup"><span data-stu-id="83812-144">Requirements</span></span>



| <span data-ttu-id="83812-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="83812-145">Requirement</span></span> | <span data-ttu-id="83812-146">Valore</span><span class="sxs-lookup"><span data-stu-id="83812-146">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="83812-147">Intestazione</span><span class="sxs-lookup"><span data-stu-id="83812-147">Header</span></span><br/> | <dl> <span data-ttu-id="83812-148"><dt>Dvdmedia. h</dt></span><span class="sxs-lookup"><span data-stu-id="83812-148"><dt>Dvdmedia.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="83812-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="83812-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83812-150">Set di proprietà</span><span class="sxs-lookup"><span data-stu-id="83812-150">Property Sets</span></span>](property-sets.md)
</dt> </dl>

 

 




