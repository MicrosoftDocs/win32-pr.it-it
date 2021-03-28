---
title: packoffset
description: Parola chiave facoltativa di compressione costante dello shader, che usa la sintassi seguente
ms.assetid: f0a3031b-d385-430d-83ee-7a8142334ad7
keywords:
- HLSL packoffset
topic_type:
- apiref
api_name:
- packoffset
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6feeaa586abe30fa8a36c28d0298dc408cdfb099
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104333908"
---
# <a name="packoffset"></a>packoffset

Parola chiave facoltativa di compressione costante dello shader, che usa la sintassi seguente:



|                                                 |
|-------------------------------------------------|
| : packoffset (c \[ SubComponent \] \[ . Component \] ) |



 

## <a name="parameters"></a>Parametri



| Elemento                                                                                                                                                                                 | Descrizione                                                                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="packoffset"></span><span id="PACKOFFSET"></span>**packoffset**<br/>                                                                                                  | Parola chiave required.<br/>                                                                                                                         |
| <span id="c"></span><span id="C"></span>**c**<br/>                                                                                                                             | La compressione si applica solo ai registri costanti (c). <br/>                                                                                          |
| <span id="_Subcomponent__.component_"></span><span id="_subcomponent__.component_"></span><span id="_SUBCOMPONENT__.COMPONENT_"></span>**\[Sottocomponente \] \[ . componente\]**<br/> | Componenti e sottocomponenti facoltativi. Un sottocomponente è un numero di registro, ovvero un numero intero. Il formato di un componente è \[ . xyzw \] .<br/> |



 

## <a name="remarks"></a>Commenti

Usare questa parola chiave per comprimere manualmente una costante dello shader quando si [dichiara un tipo di variabile](dx-graphics-hlsl-variable-syntax.md).

Quando si imballa una costante, non è possibile combinare tipi costanti.

Il compilatore si comporta in modo leggermente diverso per le costanti globali e le costanti uniformi:

-   Costante globale. Una variabile globale viene aggiunta come costante globale a un *$Global* cbuffer dal compilatore. Gli elementi compressi automaticamente (quelli dichiarati senza packoffset) verranno visualizzati dopo l'ultima variabile compressa manualmente. È possibile combinare i tipi durante la compressione delle costanti globali.
-   Costante uniforme. Un parametro uniforme nell'elenco di parametri di una funzione verrà aggiunto a un buffer costante *$param* dal compilatore quando lo shader viene compilato all'esterno del Framework degli effetti. Quando viene compilato all'interno del Framework degli effetti, una costante uniforme deve essere risolta in una variabile uniforme definita nell'ambito globale. Una costante uniforme non può essere offset manualmente; l'utilizzo consigliato è solo per la specializzazione di shader in cui viene eseguito l'aliasing a Globals, non come mezzo per passare i dati dell'applicazione allo shader.

Di seguito sono riportati alcuni esempi aggiuntivi: le [costanti di compressione con il modello di Shader 4](dx-graphics-hlsl-packing-rules.md).

## <a name="examples"></a>Esempio

Di seguito sono riportati alcuni esempi di compressione manuale delle costanti shader.

Comprimere i sottocomponenti di vettori e scalari le cui dimensioni sono sufficientemente grandi da impedire l'attraversamento dei limiti del registro. Ad esempio, sono tutti validi:


```
cbuffer MyBuffer
{
    float4 Element1 : packoffset(c0);
    float1 Element2 : packoffset(c1);
    float1 Element3 : packoffset(c1.y);
}
```



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Sintassi delle variabili](dx-graphics-hlsl-variable-syntax.md)
</dt> <dt>

[Variabili (DirectX HLSL)](dx-graphics-hlsl-variables.md)
</dt> </dl>

 

 





