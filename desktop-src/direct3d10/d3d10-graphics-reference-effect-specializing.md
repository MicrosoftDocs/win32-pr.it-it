---
description: L'interfaccia ID3D10EffectVariable dispone di una serie di metodi per eseguire il cast dell'interfaccia in un particolare tipo di interfaccia necessaria.
ms.assetid: c0842a1d-b78c-44b2-89c7-452d54efe403
title: Interfacce specializzate (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0ce8bc29ae16ada650da7283beb1dd858948cae
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305004"
---
# <a name="specializing-interfaces-direct3d-10"></a><span data-ttu-id="576ed-103">Interfacce specializzate (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="576ed-103">Specializing Interfaces (Direct3D 10)</span></span>

<span data-ttu-id="576ed-104">L' [**interfaccia ID3D10EffectVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvariable) dispone di una serie di metodi per eseguire il cast dell'interfaccia in un particolare tipo di interfaccia necessaria.</span><span class="sxs-lookup"><span data-stu-id="576ed-104">[**ID3D10EffectVariable Interface**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvariable) has a number of methods for casting the interface into the particular type of interface you need.</span></span> <span data-ttu-id="576ed-105">I metodi hanno il formato di *tipo* e includono un metodo per ogni tipo di variabile di effetto (ad esempio AsBlend, AsConstantBuffer e così via).</span><span class="sxs-lookup"><span data-stu-id="576ed-105">The methods are of the form As *Type* and include a method for each type of effect variable (such as AsBlend, AsConstantBuffer etc..)</span></span>

<span data-ttu-id="576ed-106">Si supponga, ad esempio, di avere un effetto con due variabili globali: ora e trasformazione mondiale.</span><span class="sxs-lookup"><span data-stu-id="576ed-106">For example, suppose you have an effect with two global variables: time and a world transform.</span></span>


```
float    g_fTime;
float4x4 g_mWorld;
```



<span data-ttu-id="576ed-107">Di seguito è riportato un esempio (dall' [esempio SimpleSample10](https://msdn.microsoft.com/library/Ee416428(v=VS.85).aspx)) che ottiene le variabili seguenti:</span><span class="sxs-lookup"><span data-stu-id="576ed-107">Here is an example (from [SimpleSample10 Sample](https://msdn.microsoft.com/library/Ee416428(v=VS.85).aspx)) that gets these variables:</span></span>


```
ID3D10EffectVariable* g_pVariable;
ID3D10EffectMatrixVariable* g_pmWorld;
ID3D10EffectScalarVariable* g_pfTime;

g_pVariable = g_pEffect10->GetVariableByName("g_mWorld");
g_pmWorld = g_pVariable->AsMatrix();
g_pfTime = g_pEffect10->GetVariableByName("g_fTime");
g_pfTime = g_pVariable->AsScalar();
```



<span data-ttu-id="576ed-108">Specializzando le interfacce, è possibile ridurre il codice a una singola chiamata.</span><span class="sxs-lookup"><span data-stu-id="576ed-108">By specializing the interfaces, you could reduce the code to a single call.</span></span>


```
g_pmWorld = (g_pEffect10->GetVariableByName("g_mWorld"))->AsMatrix();
g_pfTime = (g_pEffect10->GetVariableByName("g_fTime"))->AsScalar();
```



<span data-ttu-id="576ed-109">Anche le interfacce che ereditano dall' [**interfaccia ID3D10EffectVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvariable) dispongono di questi metodi, ma sono state progettate per restituire oggetti non validi; solo le chiamate dall' **interfaccia ID3D10EffectVariable** restituiscono oggetti validi.</span><span class="sxs-lookup"><span data-stu-id="576ed-109">Interfaces that inherit from [**ID3D10EffectVariable Interface**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvariable) also have these methods, but they have been designed to return invalid objects; only calls from **ID3D10EffectVariable Interface** return valid objects.</span></span> <span data-ttu-id="576ed-110">Le applicazioni possono testare l'oggetto restituito per verificare se è valido chiamando [**ID3D10EffectVariable:: IsValid**](/windows/desktop/api/D3D10Effect/nf-d3d10effect-id3d10effectvariable-isvalid).</span><span class="sxs-lookup"><span data-stu-id="576ed-110">Applications can test the returned object to see if it is valid by calling [**ID3D10EffectVariable::IsValid**](/windows/desktop/api/D3D10Effect/nf-d3d10effect-id3d10effectvariable-isvalid).</span></span>

## <a name="related-topics"></a><span data-ttu-id="576ed-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="576ed-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="576ed-112">Effetti</span><span class="sxs-lookup"><span data-stu-id="576ed-112">Effects</span></span>](d3d10-graphics-programming-guide-effects.md)
</dt> </dl>

 

 



