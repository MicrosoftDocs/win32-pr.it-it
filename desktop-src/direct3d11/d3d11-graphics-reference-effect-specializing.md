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
# <a name="specializing-interfaces-direct3d-11"></a>Interfacce specializzate (Direct3D 11)

[**ID3DX11EffectVariable**](id3dx11effectvariable.md) dispone di diversi metodi per eseguire il cast dell'interfaccia in un particolare tipo di interfaccia necessaria. I metodi sono nel formato *AsType* e includono un metodo per ogni tipo di variabile di effetto, ad esempio AsBlend, AsConstantBuffer e così via.

Si supponga, ad esempio, di avere un effetto con due variabili globali: ora e trasformazione mondiale.


```
float    g_fTime;
float4x4 g_mWorld;
```



Di seguito è riportato un esempio che ottiene le variabili seguenti:


```
ID3DX11EffectVariable* g_pVariable;
ID3DX11EffectMatrixVariable* g_pmWorld;
ID3DX11EffectScalarVariable* g_pfTime;

g_pVariable = g_pEffect11->GetVariableByName("g_mWorld");
g_pmWorld = g_pVariable->AsMatrix();
g_pVariable = g_pEffect11->GetVariableByName("g_fTime");
g_pfTime = g_pVariable->AsScalar();
```



Specializzando le interfacce, è possibile ridurre il codice a una singola chiamata.


```
g_pmWorld = (g_pEffect11->GetVariableByName("g_mWorld"))->AsMatrix();
g_pfTime = (g_pEffect11->GetVariableByName("g_fTime"))->AsScalar();
```



Anche le interfacce che ereditano da [**ID3DX11EffectVariable**](id3dx11effectvariable.md) dispongono di questi metodi, ma sono state progettate per restituire oggetti non validi; solo le chiamate da **ID3DX11EffectVariable** restituiscono oggetti validi. Le applicazioni possono testare l'oggetto restituito per verificare se è valido chiamando [**ID3DX11EffectVariable:: IsValid**](id3dx11effectvariable-isvalid.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Effetti (Direct3D 11)](d3d11-graphics-programming-guide-effects.md)
</dt> </dl>

 

 




