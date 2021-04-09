---
description: Un'annotazione è una parte di informazioni definita dall'utente, dichiarata con la sintassi seguente.
ms.assetid: 9178e61e-05a4-441c-a9f1-e05e23ab48a5
title: Sintassi delle annotazioni (Direct3D 10)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 303065e9c49c380a5accba6faadbc641ec0f528a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878410"
---
# <a name="annotation-syntax-direct3d-10"></a>Sintassi delle annotazioni (Direct3D 10)

Un'annotazione è una parte di informazioni definita dall'utente, dichiarata con la sintassi seguente.



| <   =  *Valore* nome DataType;...; > |
|--------------------------------------------|



 

## <a name="parameters"></a>Parametri



| Elemento                                                                                                   | Descrizione                                                                                                                                                                      |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DataType"></span><span id="datatype"></span><span id="DATATYPE"></span>*Tipo*<br/> | \[nel \] tipo di dati, che include qualsiasi tipo di [HLSL scalare](../direct3dhlsl/dx-graphics-hlsl-scalar.md) , nonché il [tipo di stringa](../direct3dhlsl/dx-graphics-hlsl-scalar.md).<br/> |
| <span id="Name"></span><span id="name"></span><span id="NAME"></span>*Nome*<br/>                 | \[in \] una stringa ASCII che rappresenta il nome dell'annotazione.<br/>                                                                                                          |
| <span id="Value"></span><span id="value"></span><span id="VALUE"></span>*Valore*<br/>             | \[\]valore iniziale dell'annotazione.<br/>                                                                                                                           |
| <span id="..."></span>*...*<br/>                                                                 | \[in \] altre annotazioni (coppie nome-valore).<br/>                                                                                                                     |



 

## <a name="remarks"></a>Commenti

È possibile aggiungere più di un'annotazione tra parentesi acute, ognuna delle quali è separata da un punto e virgola. Le API del Framework degli effetti riconoscono le annotazioni sulle variabili globali. tutte le altre annotazioni vengono ignorate.

## <a name="example"></a>Esempio

Di seguito sono riportati alcuni esempi.


```
       
int i <int blabla=27; string blacksheep="Hello There";>;

int j <int bambam=30; string blacksheep="Goodbye There";> = 5 ;

float y <float y=2.3;> = 2.3, z <float y=1.3;> = 1.3 ;

half w <half GlobalW = 3.62;>;

float4 main(float4 pos : SV_POSITION ) : SV_POSITION
{
    pos.y = pos.x > 0 ? pos.w * 1.3 : pos.z * .032;
    for (int x = i; x < j ; x++) 
    {
        pos.w = pos.w * pos.y + x + j - y * w;
    } 

return pos;
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sintassi della variabile Effect](d3d10-effect-variable-syntax.md)
</dt> </dl>

 

 
