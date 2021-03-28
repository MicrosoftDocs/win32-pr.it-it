---
title: Interfacce e classi negli effetti
description: Esistono diversi modi per usare le classi e le interfacce in Effects 11.
ms.assetid: 526d477b-fc1f-4bd0-a620-ce9b78147f68
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b067b8e03b2d43ea44ccab6164424cbc84c7237
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399229"
---
# <a name="interfaces-and-classes-in-effects"></a><span data-ttu-id="696b3-103">Interfacce e classi negli effetti</span><span class="sxs-lookup"><span data-stu-id="696b3-103">Interfaces and Classes in Effects</span></span>

<span data-ttu-id="696b3-104">Esistono diversi modi per usare le classi e le interfacce in Effects 11.</span><span class="sxs-lookup"><span data-stu-id="696b3-104">There are many ways to use classes and interfaces in Effects 11.</span></span> <span data-ttu-id="696b3-105">Per la sintassi dell'interfaccia e della classe, vedere [interfacce e classi](/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl-dynamic-linking-class).</span><span class="sxs-lookup"><span data-stu-id="696b3-105">For interface and class syntax, see [Interfaces and Classes](/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl-dynamic-linking-class).</span></span>

<span data-ttu-id="696b3-106">Le sezioni seguenti illustrano in dettaglio come specificare le istanze di classe per uno shader che usa le interfacce.</span><span class="sxs-lookup"><span data-stu-id="696b3-106">The following sections detail how to specify class instances to a shader which uses interfaces.</span></span> <span data-ttu-id="696b3-107">Negli esempi si useranno le seguenti interfacce e classi:</span><span class="sxs-lookup"><span data-stu-id="696b3-107">We will use the following interface and classes in the examples:</span></span>


```
interface IColor
{
  float4 GetColor();
};

class CRed : IColor
{
  float4 GetColor() { return float4(1,0,0,1); }
};
class CGreen : IColor
{
  float4 GetColor() { return float4(0,1,0,1); }
};

CRed pRed;
CGreen pGreen;
IColor pIColor;
IColor pIColor2 = pRed;
```



<span data-ttu-id="696b3-108">Si noti che le istanze dell'interfaccia possono essere inizializzate in istanze di classe.</span><span class="sxs-lookup"><span data-stu-id="696b3-108">Note that interface instances can be initialized to class instances.</span></span> <span data-ttu-id="696b3-109">Sono supportate anche matrici di classi e istanze di interfaccia che possono essere inizializzate come nell'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="696b3-109">Arrays of class and interface instances are also supported and they can be initialized as in the following example:</span></span>


```
CRed pRedArray[2];
IColor pIColor3 = pRedArray[1];
IColor pIColorArray[2] = {pRed, pGreen};
IColor pIColorArray2[2] = pRedArray;
```



## <a name="uniform-interface-parameters"></a><span data-ttu-id="696b3-110">Parametri dell'interfaccia uniforme</span><span class="sxs-lookup"><span data-stu-id="696b3-110">Uniform Interface Parameters</span></span>

<span data-ttu-id="696b3-111">Analogamente ad altri tipi di dati uniformi, è necessario specificare parametri di interfaccia uniformi nella chiamata CompileShader.</span><span class="sxs-lookup"><span data-stu-id="696b3-111">Just like other uniform data types, uniform interface parameters must be specified in the CompileShader call.</span></span> <span data-ttu-id="696b3-112">I parametri di interfaccia possono essere assegnati a istanze di interfaccia globali o a istanze di classe globali.</span><span class="sxs-lookup"><span data-stu-id="696b3-112">Interface parameters can be assigned to global interface instances or global class instances.</span></span> <span data-ttu-id="696b3-113">Quando viene assegnato a un'istanza dell'interfaccia globale, lo shader avrà una dipendenza dall'istanza dell'interfaccia, il che significa che deve essere impostato su un'istanza della classe.</span><span class="sxs-lookup"><span data-stu-id="696b3-113">When assigned to a global interface instance, the shader will have a dependency on the interface instance, which means that it must be set to a class instance.</span></span> <span data-ttu-id="696b3-114">Quando vengono assegnate a istanze di classe globali, il compilatore specializza lo shader (come con altri tipi di dati uniformi) per usare tale classe.</span><span class="sxs-lookup"><span data-stu-id="696b3-114">When assigned to global class instances, the compiler specializes the shader (as with other uniform data types) to use that class.</span></span> <span data-ttu-id="696b3-115">Questa operazione è importante per due scenari:</span><span class="sxs-lookup"><span data-stu-id="696b3-115">This is important for two scenarios:</span></span>

1.  <span data-ttu-id="696b3-116">Gli shader con una \_ destinazione 4 x possono usare i parametri di interfaccia se questi parametri sono uniformi e assegnati alle istanze di classe globali (pertanto non viene usato alcun collegamento dinamico).</span><span class="sxs-lookup"><span data-stu-id="696b3-116">Shaders with a 4\_x target can use interface parameters if these parameters are uniform and assigned to global class instances (so no dynamic linkage is used).</span></span>
2.  <span data-ttu-id="696b3-117">Gli utenti possono decidere di avere molti shader compilati e specializzati senza collegamento dinamico o con pochi shader compilati con collegamento dinamico.</span><span class="sxs-lookup"><span data-stu-id="696b3-117">Users can decide to have many compiled, specialized shaders with no dynamic linkage or few compiled shaders with dynamic linkage.</span></span>


```
float4 PSUniform( uniform IColor color ) : SV_Target
{
  return color;
}

technique11
{
  pass
  {
    SetPixelShader( CompileShader( ps_4_0, PSUniform(pRed) ) );
  }
  pass
  {
    SetPixelShader( CompileShader( ps_5_0, PSUniform(pIColor2) ) );
  }
}
```



<span data-ttu-id="696b3-118">Se pIColor2 rimane invariato tramite l'API, le due passate precedenti sono funzionalmente equivalenti, ma il primo usa uno \_ \_ shader statico PS 4 0 mentre il secondo usa uno \_ shader PS 5 \_ 0 con collegamento dinamico.</span><span class="sxs-lookup"><span data-stu-id="696b3-118">If pIColor2 remains unchanged through the API, then the previous two passes are functionally equivalent, but the first uses a ps\_4\_0 static shader while the second uses a ps\_5\_0 shader with dynamic linkage.</span></span> <span data-ttu-id="696b3-119">Se pIColor2 viene modificato tramite l'API Effects (vedere l'impostazione delle istanze della classe di seguito), il comportamento del pixel shader nel secondo passaggio potrebbe cambiare.</span><span class="sxs-lookup"><span data-stu-id="696b3-119">If pIColor2 is changed through the effects API (see Setting Class Instances below), then the behavior of the pixel shader in the second pass may change.</span></span>

## <a name="non-uniform-interface-parameters"></a><span data-ttu-id="696b3-120">Parametri di interfaccia non uniformi</span><span class="sxs-lookup"><span data-stu-id="696b3-120">Non-Uniform Interface Parameters</span></span>

<span data-ttu-id="696b3-121">I parametri di interfaccia non uniformi creano dipendenze dell'interfaccia per gli shader.</span><span class="sxs-lookup"><span data-stu-id="696b3-121">Non-uniform interface parameters create interface dependencies for the shaders.</span></span> <span data-ttu-id="696b3-122">Quando si applica uno shader con parametri di interfaccia, questi parametri devono essere assegnati in con la chiamata BindInterfaces.</span><span class="sxs-lookup"><span data-stu-id="696b3-122">When applying a shader with interface parameters, these parameters must be assigned in with the BindInterfaces call.</span></span> <span data-ttu-id="696b3-123">Le istanze di interfaccia globali e le istanze della classe globale possono essere specificate nella chiamata BindInterfaces.</span><span class="sxs-lookup"><span data-stu-id="696b3-123">Global interface instances and global class instances can be specified in the BindInterfaces call.</span></span>


```
float4 PSAbstract( IColor color ) : SV_Target
{
  return color;
}

PixelShader pPSAbstract = CompileShader( ps_5_0, PSAbstract(pRed) );

technique11
{
  pass
  {
    SetPixelShader( BindInterfaces( pPSAbstract, pRed ) );
  }
  pass
  {
    SetPixelShader( BindInterfaces( pPSAbstract, pIColor2 ) );
  }
}
```



<span data-ttu-id="696b3-124">Se pIColor2 rimane invariato tramite l'API, le due passate precedenti sono funzionalmente equivalenti e usano il collegamento dinamico.</span><span class="sxs-lookup"><span data-stu-id="696b3-124">If pIColor2 remains unchanged through the API, then the previous two passes are functionally equivalent and both use dynamic linkage.</span></span> <span data-ttu-id="696b3-125">Se pIColor2 viene modificato tramite l'API Effects (vedere l'impostazione delle istanze della classe di seguito), il comportamento del pixel shader nel secondo passaggio potrebbe cambiare.</span><span class="sxs-lookup"><span data-stu-id="696b3-125">If pIColor2 is changed through the effects API (see Setting Class Instances below), then the behavior of the pixel shader in the second pass may change.</span></span>

## <a name="setting-class-instances"></a><span data-ttu-id="696b3-126">Impostazione delle istanze della classe</span><span class="sxs-lookup"><span data-stu-id="696b3-126">Setting Class Instances</span></span>

<span data-ttu-id="696b3-127">Quando si imposta uno shader con collegamento dello shader dinamico sul dispositivo Direct3D 11, è necessario specificare anche le istanze della classe.</span><span class="sxs-lookup"><span data-stu-id="696b3-127">When setting a shader with dynamic shader linkage to the Direct3D 11 device, class instances must also be specified.</span></span> <span data-ttu-id="696b3-128">È un errore impostare tale shader con un'istanza della classe **null** .</span><span class="sxs-lookup"><span data-stu-id="696b3-128">It is an error to set such a shader with a **NULL** class instance.</span></span> <span data-ttu-id="696b3-129">Pertanto, tutte le istanze di interfaccia a cui fa riferimento uno shader devono disporre di un'istanza della classe associata.</span><span class="sxs-lookup"><span data-stu-id="696b3-129">Therefore, all interface instances which a shader references must have an associated class instance.</span></span>

<span data-ttu-id="696b3-130">Nell'esempio seguente viene illustrato come ottenere una variabile di istanza di classe da un effetto e come impostarla su una variabile di interfaccia:</span><span class="sxs-lookup"><span data-stu-id="696b3-130">The following example shows how to get a class instance variable from an effect and set it to an interface variable:</span></span>


```
ID3DX11EffectPass* pPass = pEffect->GetTechniqueByIndex(0)->GetPassByIndex(1);

ID3DX11EffectInterfaceVariable* pIface = pEffect->GetVariableByName( "pIColor2" )->AsInterface();
ID3DX11EffectClassInstanceVariable* pCI = pEffect->GetVariableByName( "pGreen" )->AsClassInstance();
pIface->SetClassInstance( pCI );
pPass->Apply( 0, pDeviceContext );

// Apply the same pass with a different class instance
pCI = pEffect->GetVariableByName( "pRedArray" )->GetElement(1)->AsClassInstance();
pIface->SetClassInstance( pCI );
pPass->Apply( 0, pDeviceContext );
```



## <a name="related-topics"></a><span data-ttu-id="696b3-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="696b3-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="696b3-132">Effetti (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="696b3-132">Effects (Direct3D 11)</span></span>](d3d11-graphics-programming-guide-effects.md)
</dt> </dl>

 

 