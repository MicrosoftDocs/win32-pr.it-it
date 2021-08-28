---
description: Un'annotazione è un'informazione definita dall'utente, dichiarata con la sintassi seguente.
ms.assetid: 9178e61e-05a4-441c-a9f1-e05e23ab48a5
title: Sintassi delle annotazioni (Direct3D 10)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea0c02e250438f25a22f8ba6d059a723299f1ee1fa175b51ce2ffe87b07c5f87
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120120001"
---
# <a name="annotation-syntax-direct3d-10"></a>Sintassi delle annotazioni (Direct3D 10)

Un'annotazione è un'informazione definita dall'utente, dichiarata con la sintassi seguente.



| <*DataType* *Name*  =  *Value*; ... ; > |
|--------------------------------------------|



 

## <a name="parameters"></a>Parametri



| Elemento                                                                                                   | Descrizione                                                                                                                                                                      |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DataType"></span><span id="datatype"></span><span id="DATATYPE"></span>*Datatype*<br/> | \[in \] Tipo di dati, che include qualsiasi tipo [HLSL scalare](../direct3dhlsl/dx-graphics-hlsl-scalar.md) e il [tipo stringa](../direct3dhlsl/dx-graphics-hlsl-scalar.md).<br/> |
| <span id="Name"></span><span id="name"></span><span id="NAME"></span>*Nome*<br/>                 | \[in \] Una stringa ASCII che rappresenta il nome dell'annotazione.<br/>                                                                                                          |
| <span id="Value"></span><span id="value"></span><span id="VALUE"></span>*Valore*<br/>             | \[in \] Valore iniziale dell'annotazione.<br/>                                                                                                                           |
| <span id="..."></span>*...*<br/>                                                                 | \[in \] Annotazioni aggiuntive (coppie nome-valore).<br/>                                                                                                                     |



 

## <a name="remarks"></a>Commenti

È possibile aggiungere più annotazioni all'interno delle parentesi uncinate, ognuna separata da un punto e virgola. Le API del framework degli effetti riconoscono le annotazioni sulle variabili globali. tutte le altre annotazioni vengono ignorate.

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

[Sintassi delle variabili degli effetti](d3d10-effect-variable-syntax.md)
</dt> </dl>

 

 
