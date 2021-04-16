---
description: I materiali descrivono il modo in cui i poligoni riflettono la luce o sembrano emettere luce in una scena 3D.
ms.assetid: vs|directx_sdk|~\materials.htm
title: Materiali (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64e75953fd5839e1b3e7b9cc89b7331147cdb585
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104558073"
---
# <a name="materials-direct3d-9"></a><span data-ttu-id="d608c-103">Materiali (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="d608c-103">Materials (Direct3D 9)</span></span>

<span data-ttu-id="d608c-104">I materiali descrivono il modo in cui i poligoni riflettono la luce o sembrano emettere luce in una scena 3D.</span><span class="sxs-lookup"><span data-stu-id="d608c-104">Materials describe how polygons reflect light or appear to emit light in a 3D scene.</span></span> <span data-ttu-id="d608c-105">Le proprietà del materiale illustrano in dettaglio la reflection diffusa del materiale, la reflection ambiente, le emissioni chiare e le caratteristiche di evidenziazione speculare.</span><span class="sxs-lookup"><span data-stu-id="d608c-105">Material properties detail a material's diffuse reflection, ambient reflection, light emission, and specular highlight characteristics.</span></span> <span data-ttu-id="d608c-106">Direct3D usa la struttura [**D3DMATERIAL9**](d3dmaterial9.md) per contenere tutte le informazioni sulle proprietà del materiale.</span><span class="sxs-lookup"><span data-stu-id="d608c-106">Direct3D uses the [**D3DMATERIAL9**](d3dmaterial9.md) structure to carry all material property information.</span></span> <span data-ttu-id="d608c-107">Fatta eccezione per la proprietà speculare, ogni proprietà viene descritta come un colore RGBA che rappresenta la quantità di parti rosse, verdi e blu di un determinato tipo di luce che riflette e un fattore di fusione alfa.</span><span class="sxs-lookup"><span data-stu-id="d608c-107">With the exception of the specular property, each property is described as an RGBA color that represents how much of the red, green, and blue parts of a given type of light it reflects, and an alpha blending factor.</span></span>

## <a name="diffuse-and-ambient-reflection"></a><span data-ttu-id="d608c-108">Reflection diffusa e di ambiente</span><span class="sxs-lookup"><span data-stu-id="d608c-108">Diffuse and Ambient Reflection</span></span>

<span data-ttu-id="d608c-109">I membri diffusi e di ambiente della struttura [**D3DMATERIAL9**](d3dmaterial9.md) descrivono in che modo un materiale riflette l'ambiente e diffonde la luce in una scena.</span><span class="sxs-lookup"><span data-stu-id="d608c-109">The Diffuse and Ambient members of the [**D3DMATERIAL9**](d3dmaterial9.md) structure describe how a material reflects the ambient and diffuse light in a scene.</span></span> <span data-ttu-id="d608c-110">Poiché la maggior parte delle scene contiene una luce molto più diffusa rispetto alla luce ambientale, la reflection diffusa riproduce la parte più ampia per determinare il colore.</span><span class="sxs-lookup"><span data-stu-id="d608c-110">Because most scenes contain much more diffuse light than ambient light, diffuse reflection plays the largest part in determining color.</span></span> <span data-ttu-id="d608c-111">Inoltre, poiché la luce diffusa è direzionale, l'angolo di incidenza della luce diffusa influiscono sull'intensità complessiva della reflection.</span><span class="sxs-lookup"><span data-stu-id="d608c-111">Additionally, because diffuse light is directional, the angle of incidence for diffuse light affects the overall intensity of the reflection.</span></span> <span data-ttu-id="d608c-112">La reflection diffusa è maggiore quando la luce colpisce un vertice parallelo alla normale del vertice.</span><span class="sxs-lookup"><span data-stu-id="d608c-112">Diffuse reflection is greatest when the light strikes a vertex parallel to the vertex normal.</span></span> <span data-ttu-id="d608c-113">Con l'aumentare dell'angolo, l'effetto della reflection diffusa diminuisce.</span><span class="sxs-lookup"><span data-stu-id="d608c-113">As the angle increases, the effect of diffuse reflection diminishes.</span></span> <span data-ttu-id="d608c-114">La quantità di luce riflessa è il coseno dell'angolo tra la luce in arrivo e il vertice normale, come illustrato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="d608c-114">The amount of light reflected is the cosine of the angle between the incoming light and the vertex normal, as shown in the following illustration.</span></span>

![illustrazione della quantità di luce riflessa](images/incident.png)

<span data-ttu-id="d608c-116">La reflection di ambiente, ad esempio la luce di ambiente, non è direzionale.</span><span class="sxs-lookup"><span data-stu-id="d608c-116">Ambient reflection, like ambient light, is nondirectional.</span></span> <span data-ttu-id="d608c-117">La reflection di ambiente ha un impatto minore sul colore apparente di un oggetto di cui è stato eseguito il rendering, ma influisce sul colore complessivo ed è più evidente quando poca o nessuna luce diffusa riflette il materiale.</span><span class="sxs-lookup"><span data-stu-id="d608c-117">Ambient reflection has a lesser impact on the apparent color of a rendered object, but it does affect the overall color and is most noticeable when little or no diffuse light reflects off the material.</span></span> <span data-ttu-id="d608c-118">La reflection di ambiente di un materiale è interessata dal set di luce di ambiente per una scena chiamando il metodo [**IDirect3DDevice9:: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) con il \_ flag di ambiente D3DRS.</span><span class="sxs-lookup"><span data-stu-id="d608c-118">A material's ambient reflection is affected by the ambient light set for a scene by calling the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method with the D3DRS\_AMBIENT flag.</span></span>

<span data-ttu-id="d608c-119">La reflection diffusa e di ambiente interagiscono per determinare il colore percepito di un oggetto e sono in genere valori identici.</span><span class="sxs-lookup"><span data-stu-id="d608c-119">Diffuse and ambient reflection work together to determine the perceived color of an object, and are usually identical values.</span></span> <span data-ttu-id="d608c-120">Ad esempio, per eseguire il rendering di un oggetto cristallino blu, si crea un materiale che riflette solo il componente blu di diffusione e luce ambientale.</span><span class="sxs-lookup"><span data-stu-id="d608c-120">For example, to render a blue crystalline object, you create a material that reflects only the blue component of diffuse and ambient light.</span></span> <span data-ttu-id="d608c-121">Quando viene inserita in una stanza con una luce bianca, il cristallo sembra essere blu.</span><span class="sxs-lookup"><span data-stu-id="d608c-121">When placed in a room with a white light, the crystal appears to be blue.</span></span> <span data-ttu-id="d608c-122">Tuttavia, in una stanza con solo luce rossa, lo stesso cristallo sembrerebbe nero, perché il materiale non riflette la luce rossa.</span><span class="sxs-lookup"><span data-stu-id="d608c-122">However, in a room that has only red light, the same crystal would appear to be black, because its material doesn't reflect red light.</span></span>

## <a name="emission"></a><span data-ttu-id="d608c-123">Emissione</span><span class="sxs-lookup"><span data-stu-id="d608c-123">Emission</span></span>

<span data-ttu-id="d608c-124">I materiali possono essere usati per fare in modo che un oggetto di cui è stato eseguito il rendering risulti con luminosità automatica.</span><span class="sxs-lookup"><span data-stu-id="d608c-124">Materials can be used to make a rendered object appear to be self-luminous.</span></span> <span data-ttu-id="d608c-125">Il membro emissivo della struttura [**D3DMATERIAL9**](d3dmaterial9.md) viene usato per descrivere il colore e la trasparenza della luce emessa.</span><span class="sxs-lookup"><span data-stu-id="d608c-125">The Emissive member of the [**D3DMATERIAL9**](d3dmaterial9.md) structure is used to describe the color and transparency of the emitted light.</span></span> <span data-ttu-id="d608c-126">L'emissione influiscono sul colore di un oggetto e può, ad esempio, rendere un materiale scuro più chiaro e assumere parte del colore emesso.</span><span class="sxs-lookup"><span data-stu-id="d608c-126">Emission affects an object's color and can, for example, make a dark material brighter and take on part of the emitted color.</span></span>

<span data-ttu-id="d608c-127">È possibile usare la proprietà emissivo di un materiale per aggiungere l'illusione che un oggetto emette la luce, senza incorrere nel sovraccarico computazionale dell'aggiunta di una luce alla scena.</span><span class="sxs-lookup"><span data-stu-id="d608c-127">You can use a material's emissive property to add the illusion that an object is emitting light, without incurring the computational overhead of adding a light to the scene.</span></span> <span data-ttu-id="d608c-128">Nel caso del cristallo blu, la proprietà emissivo è utile se si vuole che il cristallo appaia chiaro, ma non viene eseguito il cast della luce sugli altri oggetti nella scena.</span><span class="sxs-lookup"><span data-stu-id="d608c-128">In the case of the blue crystal, the emissive property is useful if you want to make the crystal appear to light up, but not cast light on other objects in the scene.</span></span> <span data-ttu-id="d608c-129">Tenere presente che i materiali con proprietà emissivo non emettono luce che possono essere riflessi da altri oggetti in una scena.</span><span class="sxs-lookup"><span data-stu-id="d608c-129">Remember, materials with emissive properties don't emit light that can be reflected by other objects in a scene.</span></span> <span data-ttu-id="d608c-130">Per ottenere questa luce riflessa, è necessario inserire una luce aggiuntiva all'interno della scena.</span><span class="sxs-lookup"><span data-stu-id="d608c-130">To achieve this reflected light, you need to place an additional light within the scene.</span></span>

## <a name="specular-reflection"></a><span data-ttu-id="d608c-131">Reflection speculare</span><span class="sxs-lookup"><span data-stu-id="d608c-131">Specular Reflection</span></span>

<span data-ttu-id="d608c-132">La reflection speculare crea evidenziazioni sugli oggetti, facendo in modo che vengano visualizzate lucide.</span><span class="sxs-lookup"><span data-stu-id="d608c-132">Specular reflection creates highlights on objects, making them appear shiny.</span></span> <span data-ttu-id="d608c-133">La struttura [**D3DMATERIAL9**](d3dmaterial9.md) contiene due membri che descrivono il colore di evidenziazione speculare, nonché il lucentezza globale del materiale.</span><span class="sxs-lookup"><span data-stu-id="d608c-133">The [**D3DMATERIAL9**](d3dmaterial9.md) structure contains two members that describe the specular highlight color as well as the material's overall shininess.</span></span> <span data-ttu-id="d608c-134">Il colore delle evidenziazioni speculari viene stabilito impostando il membro speculare sul colore RGBA desiderato. i colori più comuni sono bianco o grigio chiaro.</span><span class="sxs-lookup"><span data-stu-id="d608c-134">You establish the color of the specular highlights by setting the Specular member to the desired RGBA color - the most common colors are white or light gray.</span></span> <span data-ttu-id="d608c-135">I valori impostati in Power membri controllano la nitidezza degli effetti speculari.</span><span class="sxs-lookup"><span data-stu-id="d608c-135">The values you set in the Power member control how sharp the specular effects are.</span></span>

<span data-ttu-id="d608c-136">Le evidenziazioni speculari possono creare effetti drammatici.</span><span class="sxs-lookup"><span data-stu-id="d608c-136">Specular highlights can create dramatic effects.</span></span> <span data-ttu-id="d608c-137">Disegno di nuovo in Blue Crystal analogy: un valore di potenza maggiore crea evidenziazioni speculari più nitide, rendendo il cristallo apparentemente chiaro.</span><span class="sxs-lookup"><span data-stu-id="d608c-137">Drawing again on the blue crystal analogy: a larger Power value creates sharper specular highlights, making the crystal appear to be quite shiny.</span></span> <span data-ttu-id="d608c-138">I valori più piccoli aumentano l'area dell'effetto, creando una reflection noiosa che rende l'aspetto cristallizzato.</span><span class="sxs-lookup"><span data-stu-id="d608c-138">Smaller values increase the area of the effect, creating a dull reflection that make the crystal look frosty.</span></span> <span data-ttu-id="d608c-139">Per fare in modo che un oggetto sia effettivamente opaco, impostare il membro di alimentazione su zero e il colore da speculare a nero.</span><span class="sxs-lookup"><span data-stu-id="d608c-139">To make an object truly matte, set the Power member to zero and the color in Specular to black.</span></span> <span data-ttu-id="d608c-140">Sperimentare diversi livelli di reflection per produrre un aspetto realistico per le proprie esigenze.</span><span class="sxs-lookup"><span data-stu-id="d608c-140">Experiment with different levels of reflection to produce a realistic appearance for your needs.</span></span> <span data-ttu-id="d608c-141">Nella figura seguente vengono illustrati due modelli identici.</span><span class="sxs-lookup"><span data-stu-id="d608c-141">The following illustration shows two identical models.</span></span> <span data-ttu-id="d608c-142">Quello a sinistra usa una potenza di Reflection speculare di 10. il modello a destra non ha Reflection speculare.</span><span class="sxs-lookup"><span data-stu-id="d608c-142">The one on the left uses a specular reflection power of 10; the model on the right has no specular reflection.</span></span>

![illustrazione dei modelli di Reflection speculare](images/spechigh.png)

## <a name="setting-material-properties"></a><span data-ttu-id="d608c-144">Impostazione delle proprietà del materiale</span><span class="sxs-lookup"><span data-stu-id="d608c-144">Setting Material Properties</span></span>

<span data-ttu-id="d608c-145">I dispositivi di rendering Direct3D possono eseguire il rendering con un set di proprietà del materiale alla volta.</span><span class="sxs-lookup"><span data-stu-id="d608c-145">Direct3D rendering devices can render with one set of material properties at a time.</span></span>

<span data-ttu-id="d608c-146">In un'applicazione C++ è possibile impostare le proprietà del materiale utilizzate dal sistema preparando una struttura [**D3DMATERIAL9**](d3dmaterial9.md) , quindi chiamando il metodo [**IDirect3DDevice9:: sematerial**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setmaterial) .</span><span class="sxs-lookup"><span data-stu-id="d608c-146">In a C++ application, you set the material properties that the system uses by preparing a [**D3DMATERIAL9**](d3dmaterial9.md) structure, and then calling the [**IDirect3DDevice9::SetMaterial**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setmaterial) method.</span></span>

<span data-ttu-id="d608c-147">Per preparare la struttura [**D3DMATERIAL9**](d3dmaterial9.md) per l'uso, impostare le informazioni sulle proprietà nella struttura per creare l'effetto desiderato durante il rendering.</span><span class="sxs-lookup"><span data-stu-id="d608c-147">To prepare the [**D3DMATERIAL9**](d3dmaterial9.md) structure for use, set the property information in the structure to create the desired effect during rendering.</span></span> <span data-ttu-id="d608c-148">Nell'esempio di codice seguente viene impostata la struttura **D3DMATERIAL9** per un materiale viola con evidenziazioni speculari bianche nitide.</span><span class="sxs-lookup"><span data-stu-id="d608c-148">The following code example sets up the **D3DMATERIAL9** structure for a purple material with sharp white specular highlights.</span></span>


```
D3DMATERIAL9 mat;

// Set the RGBA for diffuse reflection.
mat.Diffuse.r = 0.5f;
mat.Diffuse.g = 0.0f;
mat.Diffuse.b = 0.5f;
mat.Diffuse.a = 1.0f;

// Set the RGBA for ambient reflection.
mat.Ambient.r = 0.5f;
mat.Ambient.g = 0.0f;
mat.Ambient.b = 0.5f;
mat.Ambient.a = 1.0f;

// Set the color and sharpness of specular highlights.
mat.Specular.r = 1.0f;
mat.Specular.g = 1.0f;
mat.Specular.b = 1.0f;
mat.Specular.a = 1.0f;
mat.Power = 50.0f;

// Set the RGBA for emissive color.
mat.Emissive.r = 0.0f;
mat.Emissive.g = 0.0f;
mat.Emissive.b = 0.0f;
mat.Emissive.a = 0.0f;
```



<span data-ttu-id="d608c-149">Dopo aver preparato la struttura [**D3DMATERIAL9**](d3dmaterial9.md) , è necessario applicare le proprietà chiamando il metodo [**IDirect3DDevice9:: sematerial**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setmaterial) del dispositivo di rendering.</span><span class="sxs-lookup"><span data-stu-id="d608c-149">After preparing the [**D3DMATERIAL9**](d3dmaterial9.md) structure, you apply the properties by calling the [**IDirect3DDevice9::SetMaterial**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setmaterial) method of the rendering device.</span></span> <span data-ttu-id="d608c-150">Questo metodo accetta l'indirizzo di una struttura **D3DMATERIAL9** predisposta come unico parametro.</span><span class="sxs-lookup"><span data-stu-id="d608c-150">This method accepts the address of a prepared **D3DMATERIAL9** structure as its only parameter.</span></span> <span data-ttu-id="d608c-151">È possibile chiamare **IDirect3DDevice9:: sematerial** con le nuove informazioni necessarie per aggiornare le proprietà del materiale per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d608c-151">You can call **IDirect3DDevice9::SetMaterial** with new information as needed to update the material properties for the device.</span></span> <span data-ttu-id="d608c-152">Nell'esempio di codice riportato di seguito viene illustrato come potrebbe apparire nel codice.</span><span class="sxs-lookup"><span data-stu-id="d608c-152">The following code example shows how this might look in code.</span></span>


```
// This code example uses the material properties defined for 
// the mat variable earlier in this topic. The pd3dDev is assumed
// to be a valid pointer to an IDirect3DDevice9 interface.
HRESULT hr;
hr = pd3dDev->SetMaterial(&mat);
if(FAILED(hr))
{
    // Code to handle the error goes here.
}
```



<span data-ttu-id="d608c-153">Quando si crea un dispositivo Direct3D, il materiale corrente viene impostato automaticamente sul valore predefinito indicato nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="d608c-153">When you create a Direct3D device, the current material is automatically set to the default shown in the following table.</span></span>



| <span data-ttu-id="d608c-154">Membro</span><span class="sxs-lookup"><span data-stu-id="d608c-154">Member</span></span>   | <span data-ttu-id="d608c-155">Valore</span><span class="sxs-lookup"><span data-stu-id="d608c-155">Value</span></span>                |
|----------|----------------------|
| <span data-ttu-id="d608c-156">Diffusa</span><span class="sxs-lookup"><span data-stu-id="d608c-156">Diffuse</span></span>  | <span data-ttu-id="d608c-157">(R:0, G:0, B:0, A:0)</span><span class="sxs-lookup"><span data-stu-id="d608c-157">(R:0, G:0, B:0, A:0)</span></span> |
| <span data-ttu-id="d608c-158">Speculare</span><span class="sxs-lookup"><span data-stu-id="d608c-158">Specular</span></span> | <span data-ttu-id="d608c-159">(R:0, G:0, B:0, A:0)</span><span class="sxs-lookup"><span data-stu-id="d608c-159">(R:0, G:0, B:0, A:0)</span></span> |
| <span data-ttu-id="d608c-160">Di ambiente</span><span class="sxs-lookup"><span data-stu-id="d608c-160">Ambient</span></span>  | <span data-ttu-id="d608c-161">(R:0, G:0, B:0, A:0)</span><span class="sxs-lookup"><span data-stu-id="d608c-161">(R:0, G:0, B:0, A:0)</span></span> |
| <span data-ttu-id="d608c-162">Emissiva</span><span class="sxs-lookup"><span data-stu-id="d608c-162">Emissive</span></span> | <span data-ttu-id="d608c-163">(R:0, G:0, B:0, A:0)</span><span class="sxs-lookup"><span data-stu-id="d608c-163">(R:0, G:0, B:0, A:0)</span></span> |
| <span data-ttu-id="d608c-164">Potenza</span><span class="sxs-lookup"><span data-stu-id="d608c-164">Power</span></span>    | <span data-ttu-id="d608c-165">(0,0)</span><span class="sxs-lookup"><span data-stu-id="d608c-165">(0.0)</span></span>                |



 

## <a name="retrieving-material-properties"></a><span data-ttu-id="d608c-166">Recupero delle proprietà del materiale</span><span class="sxs-lookup"><span data-stu-id="d608c-166">Retrieving Material Properties</span></span>

<span data-ttu-id="d608c-167">È possibile recuperare le proprietà del materiale utilizzate attualmente dal dispositivo di rendering chiamando il metodo [**IDirect3DDevice9:: getmaterial**](/windows/desktop/api) per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d608c-167">You retrieve the material properties that the rendering device is currently using by calling the [**IDirect3DDevice9::GetMaterial**](/windows/desktop/api) method for the device.</span></span> <span data-ttu-id="d608c-168">A differenza del metodo [**IDirect3DDevice9:: sematerial**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setmaterial) , **IDirect3DDevice9:: getmaterial** non richiede la preparazione.</span><span class="sxs-lookup"><span data-stu-id="d608c-168">Unlike the [**IDirect3DDevice9::SetMaterial**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setmaterial) method, **IDirect3DDevice9::GetMaterial** doesn't require preparation.</span></span> <span data-ttu-id="d608c-169">Il metodo **IDirect3DDevice9:: getmaterial** accetta l'indirizzo di una struttura [**D3DMATERIAL9**](d3dmaterial9.md) e riempie la struttura fornita con le informazioni che descrivono le proprietà Material correnti prima di restituire.</span><span class="sxs-lookup"><span data-stu-id="d608c-169">The **IDirect3DDevice9::GetMaterial** method accepts the address of a [**D3DMATERIAL9**](d3dmaterial9.md) structure, and fills the provided structure with information describing the current material properties before returning.</span></span>


```
// For this example, the pd3dDev variable is assumed to 
// be a valid pointer to an IDirect3DDevice9 interface.
HRESULT hr;
D3DMATERIAL9 mat;

hr = pd3dDev->GetMaterial(&mat);
if(FAILED(hr))
{
    // Code to handle the error goes here.
}
```



> [!Note]  
> <span data-ttu-id="d608c-170">Se l'applicazione non specifica le proprietà del materiale per il rendering, il sistema utilizza un materiale predefinito.</span><span class="sxs-lookup"><span data-stu-id="d608c-170">If your application does not specify material properties for rendering, the system uses a default material.</span></span> <span data-ttu-id="d608c-171">Il materiale predefinito riflette tutto il bianco chiaro, ad esempio, senza reflection di ambiente o speculare e nessun colore emissivo.</span><span class="sxs-lookup"><span data-stu-id="d608c-171">The default material reflects all diffuse light - white, for example - with no ambient or specular reflection, and no emissive color.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="d608c-172">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d608c-172">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d608c-173">Luci e materiali</span><span class="sxs-lookup"><span data-stu-id="d608c-173">Lights and Materials</span></span>](lights-and-materials.md)
</dt> </dl>

 

 
