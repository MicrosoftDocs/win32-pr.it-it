---
title: Interfacce specializzate (Direct3D 11)
description: ID3DX11EffectVariable dispone di diversi metodi per eseguire il cast dell'interfaccia in un particolare tipo di interfaccia necessaria.
ms.assetid: 20892af0-7d4a-4a89-b8d7-4ef225400697
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cb9f8adb5a5bb184473ff5679df99f0b71557fa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103712070"
---
# <a name="specializing-interfaces-direct3d-11"></a><span data-ttu-id="aa869-103">Interfacce specializzate (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="aa869-103">Specializing Interfaces (Direct3D 11)</span></span>

<span data-ttu-id="aa869-104">[**ID3DX11EffectVariable**](id3dx11effectvariable.md) dispone di diversi metodi per eseguire il cast dell'interfaccia in un particolare tipo di interfaccia necessaria.</span><span class="sxs-lookup"><span data-stu-id="aa869-104">[**ID3DX11EffectVariable**](id3dx11effectvariable.md) has a number of methods for casting the interface into the particular type of interface you need.</span></span> <span data-ttu-id="aa869-105">I metodi sono nel formato *AsType* e includono un metodo per ogni tipo di variabile di effetto, ad esempio AsBlend, AsConstantBuffer e così via.</span><span class="sxs-lookup"><span data-stu-id="aa869-105">The methods are of the form *AsType* and include a method for each type of effect variable (such as AsBlend, AsConstantBuffer etc..)</span></span>

<span data-ttu-id="aa869-106">Si supponga, ad esempio, di avere un effetto con due variabili globali: ora e trasformazione mondiale.</span><span class="sxs-lookup"><span data-stu-id="aa869-106">For example, suppose you have an effect with two global variables: time and a world transform.</span></span>


```
float    g_fTime;
float4x4 g_mWorld;
```



<span data-ttu-id="aa869-107">Di seguito è riportato un esempio che ottiene le variabili seguenti:</span><span class="sxs-lookup"><span data-stu-id="aa869-107">Here is an example that gets these variables:</span></span>


```
ID3DX11EffectVariable* g_pVariable;
ID3DX11EffectMatrixVariable* g_pmWorld;
ID3DX11EffectScalarVariable* g_pfTime;

g_pVariable = g_pEffect11->GetVariableByName("g_mWorld");
g_pmWorld = g_pVariable->AsMatrix();
g_pVariable = g_pEffect11->GetVariableByName("g_fTime");
g_pfTime = g_pVariable->AsScalar();
```



<span data-ttu-id="aa869-108">Specializzando le interfacce, è possibile ridurre il codice a una singola chiamata.</span><span class="sxs-lookup"><span data-stu-id="aa869-108">By specializing the interfaces, you could reduce the code to a single call.</span></span>


```
g_pmWorld = (g_pEffect11->GetVariableByName("g_mWorld"))->AsMatrix();
g_pfTime = (g_pEffect11->GetVariableByName("g_fTime"))->AsScalar();
```



<span data-ttu-id="aa869-109">Anche le interfacce che ereditano da [**ID3DX11EffectVariable**](id3dx11effectvariable.md) dispongono di questi metodi, ma sono state progettate per restituire oggetti non validi; solo le chiamate da **ID3DX11EffectVariable** restituiscono oggetti validi.</span><span class="sxs-lookup"><span data-stu-id="aa869-109">Interfaces that inherit from [**ID3DX11EffectVariable**](id3dx11effectvariable.md) also have these methods, but they have been designed to return invalid objects; only calls from **ID3DX11EffectVariable** return valid objects.</span></span> <span data-ttu-id="aa869-110">Le applicazioni possono testare l'oggetto restituito per verificare se è valido chiamando [**ID3DX11EffectVariable:: IsValid**](id3dx11effectvariable-isvalid.md).</span><span class="sxs-lookup"><span data-stu-id="aa869-110">Applications can test the returned object to see if it is valid by calling [**ID3DX11EffectVariable::IsValid**](id3dx11effectvariable-isvalid.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="aa869-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="aa869-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aa869-112">Effetti (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="aa869-112">Effects (Direct3D 11)</span></span>](d3d11-graphics-programming-guide-effects.md)
</dt> </dl>

 

 




