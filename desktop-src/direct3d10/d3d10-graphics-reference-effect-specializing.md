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
# <a name="specializing-interfaces-direct3d-10"></a>Interfacce specializzate (Direct3D 10)

L' [**interfaccia ID3D10EffectVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvariable) dispone di una serie di metodi per eseguire il cast dell'interfaccia in un particolare tipo di interfaccia necessaria. I metodi hanno il formato di *tipo* e includono un metodo per ogni tipo di variabile di effetto (ad esempio AsBlend, AsConstantBuffer e così via).

Si supponga, ad esempio, di avere un effetto con due variabili globali: ora e trasformazione mondiale.


```
float    g_fTime;
float4x4 g_mWorld;
```



Di seguito è riportato un esempio (dall' [esempio SimpleSample10](https://msdn.microsoft.com/library/Ee416428(v=VS.85).aspx)) che ottiene le variabili seguenti:


```
ID3D10EffectVariable* g_pVariable;
ID3D10EffectMatrixVariable* g_pmWorld;
ID3D10EffectScalarVariable* g_pfTime;

g_pVariable = g_pEffect10->GetVariableByName("g_mWorld");
g_pmWorld = g_pVariable->AsMatrix();
g_pfTime = g_pEffect10->GetVariableByName("g_fTime");
g_pfTime = g_pVariable->AsScalar();
```



Specializzando le interfacce, è possibile ridurre il codice a una singola chiamata.


```
g_pmWorld = (g_pEffect10->GetVariableByName("g_mWorld"))->AsMatrix();
g_pfTime = (g_pEffect10->GetVariableByName("g_fTime"))->AsScalar();
```



Anche le interfacce che ereditano dall' [**interfaccia ID3D10EffectVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvariable) dispongono di questi metodi, ma sono state progettate per restituire oggetti non validi; solo le chiamate dall' **interfaccia ID3D10EffectVariable** restituiscono oggetti validi. Le applicazioni possono testare l'oggetto restituito per verificare se è valido chiamando [**ID3D10EffectVariable:: IsValid**](/windows/desktop/api/D3D10Effect/nf-d3d10effect-id3d10effectvariable-isvalid).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Effetti](d3d10-graphics-programming-guide-effects.md)
</dt> </dl>

 

 



