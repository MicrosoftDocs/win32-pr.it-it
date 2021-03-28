---
title: Sintassi delle annotazioni (Direct3D 11)
description: Un'annotazione è una parte di informazioni definita dall'utente, dichiarata con la sintassi descritta in questa sezione.
ms.assetid: a81198d2-c4d7-47b5-b3b8-2de11a9ee9a3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9583dafd3e1fb314ae6ac9e53d609bebc74a030
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963111"
---
# <a name="annotation-syntax-direct3d-11"></a>Sintassi delle annotazioni (Direct3D 11)

Un'annotazione è una parte di informazioni definita dall'utente, dichiarata con la sintassi descritta in questa sezione.



| <   =  *Valore* nome DataType; *...* ; > |
|----------------------------------------------|



 

## <a name="parameters"></a>Parametri



| Elemento                                                                                                   | Descrizione                                                                                                                                                                      |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DataType"></span><span id="datatype"></span><span id="DATATYPE"></span>*Tipo*<br/> | \[nel \] tipo di dati, che include qualsiasi tipo di [HLSL scalare](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-scalar) , nonché il [tipo di stringa](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-scalar).<br/> |
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

[Formato effetto](d3d11-effect-format.md)
</dt> <dt>

[Sintassi della variabile Effect](d3d11-effect-variable-syntax.md)
</dt> </dl>

 

