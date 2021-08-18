---
title: Specializzazione delle interfacce (Direct3D 11)
description: ID3DX11EffectVariable include diversi metodi per eseguire il cast dell'interfaccia nel tipo specifico di interfaccia necessario.
ms.assetid: 20892af0-7d4a-4a89-b8d7-4ef225400697
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6e4cff9c74f7a4b4034578b7ddeec2c388f0f953534393ac27778c31ed3856c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119126075"
---
# <a name="specializing-interfaces-direct3d-11"></a>Specializzazione delle interfacce (Direct3D 11)

[**ID3DX11EffectVariable**](id3dx11effectvariable.md) include diversi metodi per eseguire il cast dell'interfaccia nel tipo specifico di interfaccia necessario. I metodi hanno il formato *AsType* e includono un metodo per ogni tipo di variabile di effetto (ad esempio AsBlend, AsConstantBuffer e così via).

Si supponga, ad esempio, di avere un effetto con due variabili globali: time e world transform.


```
float    g_fTime;
float4x4 g_mWorld;
```



Ecco un esempio che ottiene queste variabili:


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



Anche le interfacce che ereditano da [**ID3DX11EffectVariable**](id3dx11effectvariable.md) hanno questi metodi, ma sono state progettate per restituire oggetti non validi. Solo le chiamate **da ID3DX11EffectVariable restituiscono** oggetti validi. Le applicazioni possono testare l'oggetto restituito per verificare se è valido chiamando [**ID3DX11EffectVariable::IsValid**](id3dx11effectvariable-isvalid.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Effetti (Direct3D 11)](d3d11-graphics-programming-guide-effects.md)
</dt> </dl>

 

 




