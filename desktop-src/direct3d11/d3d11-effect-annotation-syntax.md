---
title: Sintassi delle annotazioni (Direct3D 11)
description: Un'annotazione è un'informazione definita dall'utente, dichiarata con la sintassi descritta in questa sezione.
ms.assetid: a81198d2-c4d7-47b5-b3b8-2de11a9ee9a3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1109695f6239708e8f241b796b888b8d494acd7ab806b98c08352dbe3aeaee3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118538565"
---
# <a name="annotation-syntax-direct3d-11"></a>Sintassi delle annotazioni (Direct3D 11)

Un'annotazione è un'informazione definita dall'utente, dichiarata con la sintassi descritta in questa sezione.



| <*DataType* *Name*  =  *Value*; *...* ;> |
|----------------------------------------------|



 

## <a name="parameters"></a>Parametri



| Elemento                                                                                                   | Descrizione                                                                                                                                                                      |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DataType"></span><span id="datatype"></span><span id="DATATYPE"></span>*Datatype*<br/> | \[in \] Tipo di dati, che include qualsiasi tipo [HLSL scalare](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-scalar) e il [tipo stringa](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-scalar).<br/> |
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

[Formato effetto](d3d11-effect-format.md)
</dt> <dt>

[Sintassi delle variabili degli effetti](d3d11-effect-variable-syntax.md)
</dt> </dl>

 

