---
title: Proprietà del controllo
description: Proprietà del controllo
ms.assetid: 29c2cca3-9460-45d1-9591-026e8c18f26f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4749a7a7e408f6cd58951a72207ed801e4104d65
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856901"
---
# <a name="control-properties"></a><span data-ttu-id="82f30-103">Proprietà del controllo</span><span class="sxs-lookup"><span data-stu-id="82f30-103">Control Properties</span></span>

<span data-ttu-id="82f30-104">Oltre alle proprietà definite e implementate dal controllo stesso, la tecnologia dei controlli ActiveX comporta anche le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="82f30-104">In addition to properties defined and implemented by the control itself, ActiveX controls technology also involves:</span></span>

<dl> <dt>

<span data-ttu-id="82f30-105"><span id="Ambient_properties"></span><span id="ambient_properties"></span><span id="AMBIENT_PROPERTIES"></span>Proprietà di ambiente</span><span class="sxs-lookup"><span data-stu-id="82f30-105"><span id="Ambient_properties"></span><span id="ambient_properties"></span><span id="AMBIENT_PROPERTIES"></span>Ambient properties</span></span>
</dt> <dd>

<span data-ttu-id="82f30-106">Queste sono esposte dal contenitore tramite un sito client di controllo per fornire valori ambientali che si applicano a tutti i controlli incorporati nel contenitore.</span><span class="sxs-lookup"><span data-stu-id="82f30-106">These are exposed by the container through a control client site to provide environmental values that apply to all controls embedded in the container.</span></span> <span data-ttu-id="82f30-107">Un contenitore, ad esempio, può fornire un colore di sfondo predefinito o un tipo di carattere predefinito che può essere utilizzato dal controllo.</span><span class="sxs-lookup"><span data-stu-id="82f30-107">For example, a container can provide a default background color or a default font that the control can use.</span></span> <span data-ttu-id="82f30-108">Le proprietà di ambiente sono esposte tramite **IDispatch** implementate sull'oggetto sito di un contenitore.</span><span class="sxs-lookup"><span data-stu-id="82f30-108">Ambient properties are exposed through **IDispatch** implemented on a container's site object.</span></span> <span data-ttu-id="82f30-109">Il contenitore chiama il metodo [**IOleControl:: OnAmbientPropertyChange**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-onambientpropertychange) del controllo quando una delle proprietà di ambiente cambia valore.</span><span class="sxs-lookup"><span data-stu-id="82f30-109">The container calls the control's [**IOleControl::OnAmbientPropertyChange**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-onambientpropertychange) method when any of its ambient properties change value.</span></span> <span data-ttu-id="82f30-110">In risposta, potrebbe essere necessario che un controllo aggiorni lo stato interno o di visualizzazione in risposta.</span><span class="sxs-lookup"><span data-stu-id="82f30-110">In response, a control may need to update its own internal or visual state in response.</span></span> <span data-ttu-id="82f30-111">Il contenitore indica quale proprietà di ambiente è stata modificata con il parametro DISPID oppure può passare il DISPID \_ Unknown per indicare che più proprietà di ambiente sono state modificate.</span><span class="sxs-lookup"><span data-stu-id="82f30-111">The container indicates which ambient property changed with the DISPID parameter or may pass DISPID\_UNKNOWN to indicate that multiple ambient properties changed.</span></span>

</dd> <dt>

<span data-ttu-id="82f30-112"><span id="Extended_properties"></span><span id="extended_properties"></span><span id="EXTENDED_PROPERTIES"></span>Proprietà estese</span><span class="sxs-lookup"><span data-stu-id="82f30-112"><span id="Extended_properties"></span><span id="extended_properties"></span><span id="EXTENDED_PROPERTIES"></span>Extended properties</span></span>
</dt> <dd>

<span data-ttu-id="82f30-113">Questi vengono effettivamente implementati da un contenitore per eseguire il wrapping dei controlli in esso contenuti per fornire proprietà gestite dal contenitore visualizzate come se fossero proprietà del controllo nativo.</span><span class="sxs-lookup"><span data-stu-id="82f30-113">These are actually implemented by a container to wrap the controls it contains to provide container-managed properties that appear as if they were native control properties.</span></span> <span data-ttu-id="82f30-114">Il contenitore può aggregare il controllo, aggiungendo le proprietà estese per completare o eseguire l'override delle proprietà del controllo.</span><span class="sxs-lookup"><span data-stu-id="82f30-114">The container can aggregate the control, adding the extended properties to supplement or override the control's properties.</span></span> <span data-ttu-id="82f30-115">L'oggetto aggregato è denominato controllo esteso.</span><span class="sxs-lookup"><span data-stu-id="82f30-115">The aggregated object is called an extended control.</span></span> <span data-ttu-id="82f30-116">Al contenitore, il controllo esteso viene visualizzato come il controllo stesso e le proprietà estese sembrano esposte dal controllo.</span><span class="sxs-lookup"><span data-stu-id="82f30-116">To the container, the extended control appears as the control itself and extended properties appear to be exposed by the control.</span></span> <span data-ttu-id="82f30-117">Il contenitore supporta un controllo esteso tramite il metodo del sito client [**IOleControlSite:: GetExtendedControl**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-getextendedcontrol).</span><span class="sxs-lookup"><span data-stu-id="82f30-117">The container supports an extended control through its client site method [**IOleControlSite::GetExtendedControl**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-getextendedcontrol).</span></span> <span data-ttu-id="82f30-118">Il metodo **GetExtendedControl** consente ai controlli di spostarsi tra il sito e l'oggetto controllo esteso fornito dal contenitore, se il contenitore supporta questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="82f30-118">The **GetExtendedControl** method allows controls to navigate through the site to the extended control object provided for them by the container, if the container supports this feature.</span></span> <span data-ttu-id="82f30-119">Un contenitore può anche scegliere di visualizzare le pagine delle proprietà per i controlli estesi, oltre alle pagine che un controllo normalmente specifica tramite [**ISpecifyPropertyPages**](/windows/desktop/api/OCIdl/nn-ocidl-ispecifypropertypages).</span><span class="sxs-lookup"><span data-stu-id="82f30-119">A container can also choose to show property pages for its extended controls in addition to those pages that a control would normally specify through [**ISpecifyPropertyPages**](/windows/desktop/api/OCIdl/nn-ocidl-ispecifypropertypages).</span></span> <span data-ttu-id="82f30-120">Per questo motivo, un controllo deve richiedere a un contenitore di visualizzare un frame di proprietà prima che il controllo tenti di eseguire questa operazione.</span><span class="sxs-lookup"><span data-stu-id="82f30-120">Because of this, a control has to ask a container to show a property frame before the control attempts to do so itself.</span></span> <span data-ttu-id="82f30-121">Per eseguire questa operazione, il controllo chiama [**IOleControlSite:: ShowPropertyFrame**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-showpropertyframe) .</span><span class="sxs-lookup"><span data-stu-id="82f30-121">The control calls [**IOleControlSite::ShowPropertyFrame**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-showpropertyframe) to do this.</span></span> <span data-ttu-id="82f30-122">Se il contenitore implementa questa funzione, viene visualizzato il frame della proprietà. Se il metodo restituisce un errore, il controllo può visualizzare il frame della proprietà.</span><span class="sxs-lookup"><span data-stu-id="82f30-122">If the container implements this function then it shows the property frame itself; if the method returns an error then the control can show the property frame.</span></span>

</dd> </dl>

<span data-ttu-id="82f30-123">Per altre informazioni, vedere i seguenti argomenti:</span><span class="sxs-lookup"><span data-stu-id="82f30-123">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="82f30-124">Proprietà standard</span><span class="sxs-lookup"><span data-stu-id="82f30-124">Standard Properties</span></span>](standard-properties.md)
-   [<span data-ttu-id="82f30-125">Oggetto tipo di carattere standard</span><span class="sxs-lookup"><span data-stu-id="82f30-125">Standard Font Object</span></span>](standard-font-object.md)
-   [<span data-ttu-id="82f30-126">Oggetto immagine standard</span><span class="sxs-lookup"><span data-stu-id="82f30-126">Standard Picture Object</span></span>](standard-picture-object.md)

## <a name="related-topics"></a><span data-ttu-id="82f30-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="82f30-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="82f30-128">Metodi di controllo</span><span class="sxs-lookup"><span data-stu-id="82f30-128">Control Methods</span></span>](control-methods.md)
</dt> </dl>

 

 




