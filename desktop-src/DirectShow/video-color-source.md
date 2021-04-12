---
description: Origine colore video
ms.assetid: e6addd55-06ca-4d4b-b2b0-fde281fab244
title: Origine colore video
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56e9c751d74a78b027d50f033acb3709d18fe8f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232281"
---
# <a name="video-color-source"></a><span data-ttu-id="10804-103">Origine colore video</span><span class="sxs-lookup"><span data-stu-id="10804-103">Video Color Source</span></span>

> [!Note]  
> <span data-ttu-id="10804-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="10804-104">\[Deprecated.</span></span> <span data-ttu-id="10804-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="10804-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="10804-106">L'origine colori video crea un'immagine video continua di un colore a tinta unita.</span><span class="sxs-lookup"><span data-stu-id="10804-106">The Video Color Source creates a continuous video image of a solid color.</span></span>

<span data-ttu-id="10804-107">ID classe (CLSID): **{0CFDD070-581A-11D2-9EE6-006008039E37}**</span><span class="sxs-lookup"><span data-stu-id="10804-107">Class ID (CLSID): **{0CFDD070-581A-11D2-9EE6-006008039E37}**</span></span>

<span data-ttu-id="10804-108">Nome variabile CLSID: **CLSID \_ ColorSource**</span><span class="sxs-lookup"><span data-stu-id="10804-108">CLSID Variable Name: **CLSID\_ColorSource**</span></span>

<span data-ttu-id="10804-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="10804-109">Properties</span></span>



| <span data-ttu-id="10804-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="10804-110">Property</span></span> | <span data-ttu-id="10804-111">Type</span><span class="sxs-lookup"><span data-stu-id="10804-111">Type</span></span>      | <span data-ttu-id="10804-112">Predefinito</span><span class="sxs-lookup"><span data-stu-id="10804-112">Default</span></span> | <span data-ttu-id="10804-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="10804-113">Description</span></span>                                   |
|----------|-----------|---------|-----------------------------------------------|
| <span data-ttu-id="10804-114">Colore</span><span class="sxs-lookup"><span data-stu-id="10804-114">"Color"</span></span>  | <span data-ttu-id="10804-115">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="10804-115">**DWORD**</span></span> | <span data-ttu-id="10804-116">0</span><span class="sxs-lookup"><span data-stu-id="10804-116">0</span></span>       | <span data-ttu-id="10804-117">Specifica il colore da generare.</span><span class="sxs-lookup"><span data-stu-id="10804-117">Specifies the color to generate.</span></span> <span data-ttu-id="10804-118">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="10804-118">See Remarks.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="10804-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="10804-119">Remarks</span></span>

<span data-ttu-id="10804-120">L'origine dei colori video viene utilizzata con gli oggetti di origine.</span><span class="sxs-lookup"><span data-stu-id="10804-120">The Video Color Source is used with source objects.</span></span> <span data-ttu-id="10804-121">Per prima cosa, creare un nuovo oggetto di origine.</span><span class="sxs-lookup"><span data-stu-id="10804-121">First, create a new source object.</span></span> <span data-ttu-id="10804-122">Impostare quindi il GUID dell'oggetto di origine su CLSID \_ ColorSource, chiamando il metodo [**IAMTimelineObj:: SetSubObjectGUID**](iamtimelineobj-setsubobjectguid.md) .</span><span class="sxs-lookup"><span data-stu-id="10804-122">Then set the source object's subobject GUID to CLSID\_ColorSource, by calling the [**IAMTimelineObj::SetSubObjectGUID**](iamtimelineobj-setsubobjectguid.md) method.</span></span>

<span data-ttu-id="10804-123">Per impostare il colore, creare un oggetto [setter della proprietà](property-setter.md) e applicare la proprietà "color" all'ora zero.</span><span class="sxs-lookup"><span data-stu-id="10804-123">To set the color, create a [Property Setter](property-setter.md) object and apply the "Color" property at time zero.</span></span> <span data-ttu-id="10804-124">Il valore di questa proprietà è un numero esadecimale con formato *0xAARRGGBB*, dove *AA* è il valore alfa, *RR* è il valore rosso, *GG* è il valore verde e *BB* è il valore blu.</span><span class="sxs-lookup"><span data-stu-id="10804-124">The value of this property is a hexadecimal number with the format *0xAARRGGBB*, where *AA* is the alpha value, *RR* is the red value, *GG* is the green value, and *BB* is the blue value.</span></span> <span data-ttu-id="10804-125">I valori alfa variano da 0x00 (trasparente) a 0xFF (opaco).</span><span class="sxs-lookup"><span data-stu-id="10804-125">Alpha values range from 0x00 (transparent) to 0xFF (opaque).</span></span> <span data-ttu-id="10804-126">La proprietà è statica e deve essere applicata all'ora zero.</span><span class="sxs-lookup"><span data-stu-id="10804-126">The property is static and must be applied at time zero.</span></span>

<span data-ttu-id="10804-127">Se non si specifica il valore alfa, il valore predefinito è zero (trasparente).</span><span class="sxs-lookup"><span data-stu-id="10804-127">If you do not specify the alpha value, it defaults to zero (transparent).</span></span> <span data-ttu-id="10804-128">In un progetto video a colori a 32 bit, questa operazione causerà transizioni o effetti che usano Alpha per eseguire il rendering dell'origine del colore del video come completamente trasparente.</span><span class="sxs-lookup"><span data-stu-id="10804-128">In a 32-bit-color video project, this will cause transitions or effects that use alpha to render the Video Color Source as completely transparent.</span></span> <span data-ttu-id="10804-129">Per essere sicuri, specificare sempre l'alfa.</span><span class="sxs-lookup"><span data-stu-id="10804-129">To be safe, always specify the alpha.</span></span> <span data-ttu-id="10804-130">Ad esempio, il nero opaco è **0xFF000000**.</span><span class="sxs-lookup"><span data-stu-id="10804-130">For example, opaque black is **0xFF000000**.</span></span>

<span data-ttu-id="10804-131">Nell'esempio di codice riportato di seguito viene illustrato come utilizzare questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="10804-131">The following code example shows how to use this object.</span></span> <span data-ttu-id="10804-132">Per ulteriori informazioni sull'utilizzo di [**IPropertySetter**](ipropertysetter.md), vedere [impostazione delle proprietà relative a effetti e transizioni](setting-properties-on-effects-and-transitions.md):</span><span class="sxs-lookup"><span data-stu-id="10804-132">For more information about using [**IPropertySetter**](ipropertysetter.md), see [Setting Properties on Effects and Transitions](setting-properties-on-effects-and-transitions.md):</span></span>


```C++
DWORD           dwYellow = 0xFFFF00;
IAMTimelineObj  *pSource = NULL;

// Create the source.
HRESULT hr = pTimeline->CreateEmptyNode(&pSource, TIMELINE_MAJOR_TYPE_SOURCE);
if (SUCCEEDED(hr))
{
    hr = pSource->SetStartStop(0, 50000000);
}

if (SUCCEEDED(hr))
{
    hr = pSource->SetSubObjectGUID(CLSID_ColorSource);
}

// Create a property setter.
if (SUCCEEDED(hr))
{
    IPropertySetter *pProp = NULL;
    
    hr = CoCreateInstance(CLSID_PropertySetter, NULL, CLSCTX_INPROC_SERVER, 
        IID_PPV_ARGS(&pProp));

    if SUCCEEDED(hr))
    {
        // Set the color.    
        DEXTER_PARAM param;
        DEXTER_VALUE val;

        param.Name = SysAllocString(OLESTR("Color"));
        param.dispID = 0;
        param.nValues = 1;

        if (param.Name == NULL)
        {
            hr = E_OUTOFMEMORY;
        }
        else
        {
            val.v.vt = VT_I4;
            val.v.lVal = dwYellow;
            val.rt = 0;  // Time must be zero.
            val.dwInterp = DEXTERF_JUMP;

            hr = pProp->AddProp(param, &val);
            
            SysFreeString(param.Name);
        }

        if (SUCCEEDED(hr))
        {
            hr = pSource->SetPropertySetter(pProp); 
        }
        pProp->Release();
    }
}
```



<span data-ttu-id="10804-133">Nell'esempio seguente viene illustrata la rappresentazione XML dell'oggetto creato nell'esempio precedente.</span><span class="sxs-lookup"><span data-stu-id="10804-133">The following example shows the XML representation of the object created in the previous example.</span></span> <span data-ttu-id="10804-134">In questo caso l'elemento [**param**](param-element.md) non supporta gli elementi [**in**](at-element.md) o [**lineari**](linear-element.md) , perché l'oggetto non supporta le proprietà dinamiche:</span><span class="sxs-lookup"><span data-stu-id="10804-134">In this case the [**param**](param-element.md) element does not support [**at**](at-element.md) or [**linear**](linear-element.md) elements, because the object does not support dynamic properties:</span></span>


```C++
<clip start="0" stop="5" clsid="{0CFDD070-581A-11D2-9EE6-006008039E37}">
    <param name="Color" value="16776960"/>
</clip>
```



 

 



