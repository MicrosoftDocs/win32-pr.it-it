---
description: Impostazione delle proprietà per effetti e transizioni
ms.assetid: ce773140-7e50-4b72-8cb5-e34cba51644d
title: Impostazione delle proprietà per effetti e transizioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4ddd129eb9d4ab24ebef6f5c760a4211f26c9a6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303696"
---
# <a name="setting-properties-on-effects-and-transitions"></a><span data-ttu-id="4cdbb-103">Impostazione delle proprietà per effetti e transizioni</span><span class="sxs-lookup"><span data-stu-id="4cdbb-103">Setting Properties on Effects and Transitions</span></span>

<span data-ttu-id="4cdbb-104">\[Questa API non è supportata e può essere modificata o non disponibile in futuro.\]</span><span class="sxs-lookup"><span data-stu-id="4cdbb-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="4cdbb-105">Molti effetti e transizioni di [servizi di modifica DirectShow](directshow-editing-services.md) supportano le proprietà che ne controllano il comportamento.</span><span class="sxs-lookup"><span data-stu-id="4cdbb-105">Many [DirectShow Editing Services](directshow-editing-services.md) effects and transitions support properties that control their behavior.</span></span> <span data-ttu-id="4cdbb-106">Un'applicazione può impostare il valore di una proprietà usando l'interfaccia [**IPropertySetter**](ipropertysetter.md) .</span><span class="sxs-lookup"><span data-stu-id="4cdbb-106">An application can set the value of a property using the [**IPropertySetter**](ipropertysetter.md) interface.</span></span> <span data-ttu-id="4cdbb-107">L'oggetto Effect o Transition sottostante deve supportare **IDispatch** per l'impostazione delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="4cdbb-107">The underlying effect or transition object must support **IDispatch** for setting the properties.</span></span> <span data-ttu-id="4cdbb-108">Con gli effetti video e le transizioni, l'applicazione può impostare un intervallo di valori che cambiano nel tempo.</span><span class="sxs-lookup"><span data-stu-id="4cdbb-108">With video effects and transitions, the application can set a range of values that change over time.</span></span> <span data-ttu-id="4cdbb-109">(Ad esempio, è possibile impostare una transizione di cancellazione per spostarsi avanti e indietro nel frame). Con gli effetti audio, il valore della proprietà è statico e non può essere modificato nel tempo.</span><span class="sxs-lookup"><span data-stu-id="4cdbb-109">(For example, you can set a wipe transition to move back and forth across the frame.) With audio effects, the value of the property is static and cannot change over time.</span></span> <span data-ttu-id="4cdbb-110">L'unica eccezione è l'effetto della [busta del volume](volume-envelope-effect.md) , che supporta una proprietà dinamica per il livello del volume.</span><span class="sxs-lookup"><span data-stu-id="4cdbb-110">The only exception is the [Volume Envelope](volume-envelope-effect.md) effect, which supports a dynamic property for the volume level.</span></span>

<span data-ttu-id="4cdbb-111">Per impostare una proprietà, seguire questa procedura.</span><span class="sxs-lookup"><span data-stu-id="4cdbb-111">To set a property, perform the following steps.</span></span>

1.  <span data-ttu-id="4cdbb-112">Creare un'istanza del setter della proprietà (CLSID \_ PropertySetter).</span><span class="sxs-lookup"><span data-stu-id="4cdbb-112">Create an instance of the property setter (CLSID\_PropertySetter).</span></span>
2.  <span data-ttu-id="4cdbb-113">Riempire le strutture del [**\_ valore**](dexter-value.md) Dexter [**\_ param**](dexter-param.md) e Dexter con i dati della proprietà.</span><span class="sxs-lookup"><span data-stu-id="4cdbb-113">Fill [**DEXTER\_PARAM**](dexter-param.md) and [**DEXTER\_VALUE**](dexter-value.md) structures with the property data.</span></span> <span data-ttu-id="4cdbb-114">Queste strutture sono descritte di seguito.</span><span class="sxs-lookup"><span data-stu-id="4cdbb-114">These structures are discussed below.</span></span>
3.  <span data-ttu-id="4cdbb-115">Passare le strutture del [**\_ valore**](dexter-value.md) [**Dexter \_ param**](dexter-param.md) e Dexter al metodo [**IPropertySetter:: AddProp**](ipropertysetter-addprop.md) .</span><span class="sxs-lookup"><span data-stu-id="4cdbb-115">Pass the [**DEXTER\_PARAM**](dexter-param.md) and [**DEXTER\_VALUE**](dexter-value.md) structures to the [**IPropertySetter::AddProp**](ipropertysetter-addprop.md) method.</span></span>
4.  <span data-ttu-id="4cdbb-116">Ripetere i passaggi 2 e 3 per ogni proprietà che si desidera impostare.</span><span class="sxs-lookup"><span data-stu-id="4cdbb-116">Repeat steps 2 and 3 for each property you want to set.</span></span>
5.  <span data-ttu-id="4cdbb-117">Passare il puntatore all'interfaccia [**IPropertySetter**](ipropertysetter.md) al metodo [**IAMTimelineObj:: SetPropertySetter**](iamtimelineobj-setpropertysetter.md) .</span><span class="sxs-lookup"><span data-stu-id="4cdbb-117">Pass the [**IPropertySetter**](ipropertysetter.md) interface pointer to the [**IAMTimelineObj::SetPropertySetter**](iamtimelineobj-setpropertysetter.md) method.</span></span>

<span data-ttu-id="4cdbb-118">La struttura del [**\_ param Dexter**](dexter-param.md) specifica quale proprietà viene impostata.</span><span class="sxs-lookup"><span data-stu-id="4cdbb-118">The [**DEXTER\_PARAM**](dexter-param.md) structure specifies which property is being set.</span></span> <span data-ttu-id="4cdbb-119">Contiene i membri seguenti.</span><span class="sxs-lookup"><span data-stu-id="4cdbb-119">It contains the following members.</span></span>

-   <span data-ttu-id="4cdbb-120">**Nome**: nome della proprietà</span><span class="sxs-lookup"><span data-stu-id="4cdbb-120">**Name**: Name of the property</span></span>
-   <span data-ttu-id="4cdbb-121">**DISPID**: riservato, deve essere zero</span><span class="sxs-lookup"><span data-stu-id="4cdbb-121">**dispID**: Reserved, must be zero</span></span>
-   <span data-ttu-id="4cdbb-122">**nValori**: numero di valori</span><span class="sxs-lookup"><span data-stu-id="4cdbb-122">**nValues**: Number of values</span></span>

<span data-ttu-id="4cdbb-123">La \_ struttura del valore Dexter specifica il valore di una proprietà in un determinato momento.</span><span class="sxs-lookup"><span data-stu-id="4cdbb-123">The DEXTER\_VALUE structure specifies the value of a property at a given time.</span></span> <span data-ttu-id="4cdbb-124">Contiene i membri seguenti.</span><span class="sxs-lookup"><span data-stu-id="4cdbb-124">It contains the following members.</span></span>

-   <span data-ttu-id="4cdbb-125">**v**: tipo Variant che specifica un nuovo valore per la proprietà.</span><span class="sxs-lookup"><span data-stu-id="4cdbb-125">**v**: VARIANT type that specifies a new value for the property.</span></span> <span data-ttu-id="4cdbb-126">Il membro **VT** di questa variante definisce il tipo di dati della proprietà.</span><span class="sxs-lookup"><span data-stu-id="4cdbb-126">The **vt** member of this VARIANT defines the data type of the property.</span></span> <span data-ttu-id="4cdbb-127">Per ulteriori informazioni sul tipo **Variant** , vedere la Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="4cdbb-127">For more information on the **VARIANT** type, see the Windows SDK.</span></span>
-   <span data-ttu-id="4cdbb-128">**RT**: ora di riferimento quando la proprietà presuppone questo valore, in relazione all'ora di inizio dell'effetto o della transizione.</span><span class="sxs-lookup"><span data-stu-id="4cdbb-128">**rt**: Reference time when the property assumes this value, relative to the starting time of the effect or transition.</span></span> <span data-ttu-id="4cdbb-129">L'ora di inizio dell'effetto o della transizione è relativa all'ora di inizio dell'oggetto padre.</span><span class="sxs-lookup"><span data-stu-id="4cdbb-129">The start time of the effect or transition is relative to the start time of its parent object.</span></span>
-   <span data-ttu-id="4cdbb-130">**dwInterp**: flag che specifica il modo in cui la proprietà cambia dal valore precedente al nuovo valore.</span><span class="sxs-lookup"><span data-stu-id="4cdbb-130">**dwInterp**: Flag that specifies how the property changes from the previous value to the new value.</span></span> <span data-ttu-id="4cdbb-131">Con il \_ flag jump DEXTERF, la proprietà passa immediatamente al nuovo valore all'ora specificata.</span><span class="sxs-lookup"><span data-stu-id="4cdbb-131">With the DEXTERF\_JUMP flag, the property jumps instantly to the new value at the specified time.</span></span> <span data-ttu-id="4cdbb-132">Con il flag DEXTERF interpolate \_ , la proprietà viene interpolata in modo lineare rispetto al valore precedente.</span><span class="sxs-lookup"><span data-stu-id="4cdbb-132">With the DEXTERF\_INTERPOLATE flag, the property is interpolated linearly from the previous value.</span></span>

<span data-ttu-id="4cdbb-133">Se si imposta il membro **VT** su VT \_ BSTR, il setter della proprietà esegue le conversioni necessarie.</span><span class="sxs-lookup"><span data-stu-id="4cdbb-133">If you set the **vt** member to VT\_BSTR, the property setter makes any necessary conversions.</span></span> <span data-ttu-id="4cdbb-134">Per i valori a virgola mobile, includere lo zero iniziali prima della posizione decimale.</span><span class="sxs-lookup"><span data-stu-id="4cdbb-134">For floating-point values, include the leading zero before the decimal place.</span></span> <span data-ttu-id="4cdbb-135">Ad esempio, 0,3, not. 3.</span><span class="sxs-lookup"><span data-stu-id="4cdbb-135">For example, 0.3, not .3.</span></span>

> [!Note]  
> <span data-ttu-id="4cdbb-136">Le applicazioni devono evitare di basarsi sulla conversione da **BSTR** s a valori numerici.</span><span class="sxs-lookup"><span data-stu-id="4cdbb-136">Applications should avoid relying on the conversion from **BSTR** s to numeric values.</span></span> <span data-ttu-id="4cdbb-137">Se la proprietà ha un valore numerico, è possibile usare il tipo **Variant** numerico appropriato.</span><span class="sxs-lookup"><span data-stu-id="4cdbb-137">If the property has a numeric value, use the appropriate numeric **VARIANT** type is possible.</span></span>

 

<span data-ttu-id="4cdbb-138">Il valore di una proprietà può variare nel tempo, quindi il metodo [**IPropertySetter:: AddProp**](ipropertysetter-addprop.md) accetta un'unica struttura di [**\_ parametri Dexter**](dexter-param.md) e un puntatore a una matrice di strutture di [**\_ valori Dexter**](dexter-value.md) .</span><span class="sxs-lookup"><span data-stu-id="4cdbb-138">The value of a property can change over time, so the [**IPropertySetter::AddProp**](ipropertysetter-addprop.md) method takes a single [**DEXTER\_PARAM**](dexter-param.md) structure and a pointer to an array of [**DEXTER\_VALUE**](dexter-value.md) structures.</span></span> <span data-ttu-id="4cdbb-139">La matrice definisce un set di valori basati sul tempo per la proprietà.</span><span class="sxs-lookup"><span data-stu-id="4cdbb-139">The array defines a set of time-based values for the property.</span></span> <span data-ttu-id="4cdbb-140">I membri della matrice devono essere in ordine di tempo crescente e il membro **nValori** della struttura del parametro Dexter \_ deve essere uguale alla lunghezza della matrice.</span><span class="sxs-lookup"><span data-stu-id="4cdbb-140">The members of the array must be in ascending time order, and the **nValues** member of the DEXTER\_PARAM structure must equal the length of the array.</span></span>

<span data-ttu-id="4cdbb-141">Nell'esempio di codice seguente vengono creati i dati delle proprietà per la transizione di [cancellazione SMPTE](smpte-wipe-transition.md) .</span><span class="sxs-lookup"><span data-stu-id="4cdbb-141">The following code example creates property data for the [SMPTE Wipe](smpte-wipe-transition.md) transition.</span></span> <span data-ttu-id="4cdbb-142">Imposta il codice di cancellazione su 120, che crea una cancellazione ovale.</span><span class="sxs-lookup"><span data-stu-id="4cdbb-142">It sets the wipe code to 120, which creates an oval wipe.</span></span> <span data-ttu-id="4cdbb-143">Imposta la durata di riferimento su zero, che indica l'inizio della transizione.</span><span class="sxs-lookup"><span data-stu-id="4cdbb-143">It sets the reference time to zero, indicating the start of the transition.</span></span>


```C++
IPropertySetter     *pProp;   // Property setter
IAMTimelineObj      *pTransObj;  // Transition object
// Create an SMPTE Wipe transition object. (Not shown)

hr = CoCreateInstance(CLSID_PropertySetter, NULL, CLSCTX_INPROC_SERVER,
    IID_IPropertySetter, (void**) &pProp);

// Error checking is omitted for clarity...

DEXTER_PARAM param;
DEXTER_VALUE *pValue = (DEXTER_VALUE*)CoTaskMemAlloc(sizeof(DEXTER_VALUE));

// Initialize the parameter. 
param.Name = SysAllocString(L"MaskNum");
param.dispID = 0;
param.nValues = 1;

// Initialize the value.
pValue->v.vt = VT_I4;
pValue->v.lVal = 120; // Oval
pValue->rt = 0;
pValue->dwInterp = DEXTERF_JUMP;

pProp->AddProp(param, pValue);

// Free allocated resources.
SysFreeString(param.Name);
VariantClear(&(pValue->v));
CoTaskMemFree(pValue);

// Set the property on the transition.
pTransObj->SetPropertySetter(pProp);
pProp->Release();
```



<span data-ttu-id="4cdbb-144">**Modifica dinamica delle proprietà**</span><span class="sxs-lookup"><span data-stu-id="4cdbb-144">**Dynamically Changing Properties**</span></span>

<span data-ttu-id="4cdbb-145">Dopo aver eseguito il rendering di un progetto di modifica video, è possibile modificare le proprietà di un oggetto o di un effetto di transizione durante l'esecuzione del grafo.</span><span class="sxs-lookup"><span data-stu-id="4cdbb-145">After you render a video editing project, it is possible to modify an effect or transition object's properties while the graph is running.</span></span> <span data-ttu-id="4cdbb-146">Questa operazione è tuttavia possibile solo se si impostano le proprietà di tale oggetto prima dell'applicazione denominata [**IRenderEngine:: ConnectFrontEnd**](irenderengine-connectfrontend.md).</span><span class="sxs-lookup"><span data-stu-id="4cdbb-146">However, this is possible only if you set properties on that object before the application called [**IRenderEngine::ConnectFrontEnd**](irenderengine-connectfrontend.md).</span></span> <span data-ttu-id="4cdbb-147">In tal caso, è possibile chiamare [**IAMTimelineObj:: GetPropertySetter**](iamtimelineobj-getpropertysetter.md) per effetto o transizione, cancellare o modificare le proprietà e le modifiche vengono eseguite in modo dinamico durante l'esecuzione del grafo.</span><span class="sxs-lookup"><span data-stu-id="4cdbb-147">If so, you can call [**IAMTimelineObj::GetPropertySetter**](iamtimelineobj-getpropertysetter.md) on the effect or transition, clear or modify the properties, and the changes will happen dynamically as the graph is running.</span></span> <span data-ttu-id="4cdbb-148">È possibile che si verifichino anomalie visive durante la modifica, quindi questa operazione è consigliata solo per l'anteprima.</span><span class="sxs-lookup"><span data-stu-id="4cdbb-148">There may be visual anomalies while the change occurs, so this is recommended only for preview.</span></span> <span data-ttu-id="4cdbb-149">Non modificare le proprietà durante la scrittura del progetto in un file.</span><span class="sxs-lookup"><span data-stu-id="4cdbb-149">Do not change the properties while you are writing the project to a file.</span></span>

<span data-ttu-id="4cdbb-150">Se non sono state impostate proprietà nell'oggetto Effect o Transition prima di chiamare **ConnectFrontEnd**, non è possibile aggiungervi proprietà durante l'esecuzione del grafo.</span><span class="sxs-lookup"><span data-stu-id="4cdbb-150">If you did not set any properties on the effect or transition object before you called **ConnectFrontEnd**, you cannot add properties to it while the graph is running.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4cdbb-151">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4cdbb-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4cdbb-152">Utilizzo degli effetti e delle transizioni</span><span class="sxs-lookup"><span data-stu-id="4cdbb-152">Working with Effects and Transitions</span></span>](working-with-effects-and-transitions.md)
</dt> </dl>

 

 



