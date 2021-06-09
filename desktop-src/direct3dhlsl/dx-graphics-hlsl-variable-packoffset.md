---
title: packoffset
description: Parola chiave facoltativa per la creazione di un pacchetto di costanti shader, che usa la sintassi seguente
ms.assetid: f0a3031b-d385-430d-83ee-7a8142334ad7
keywords:
- packoffset HLSL
topic_type:
- apiref
api_name:
- packoffset
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5c92a6375f0724a1910fc0f09b47e1593614f9f1
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/09/2021
ms.locfileid: "111826080"
---
# <a name="packoffset"></a>packoffset

Parola chiave facoltativa per la creazione di un pacchetto di costanti shader, che usa la sintassi seguente:

: packoffset( c \[ Subcomponent \] \[ .component \] )



 

## <a name="parameters"></a>Parametri



| Elemento                                                                                                                                                                                 | Descrizione                                                                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="packoffset"></span><span id="PACKOFFSET"></span>**packoffset**<br/>                                                                                                  | Parola chiave obbligatoria.<br/>                                                                                                                         |
| <span id="c"></span><span id="C"></span>**C**<br/>                                                                                                                             | La creazione di un pacchetto si applica solo ai registri costanti (c). <br/>                                                                                          |
| <span id="_Subcomponent__.component_"></span><span id="_subcomponent__.component_"></span><span id="_SUBCOMPONENT__.COMPONENT_"></span>**\[Componente \] \[ secondario .component\]**<br/> | Sottocomponenti e componenti facoltativi. Un sottocomponente è un numero di registro, ovvero un numero intero. Un componente è nel formato \[ .xyzw \] .<br/> |



 

## <a name="remarks"></a>Commenti

Usare questa parola chiave per creare manualmente un pacchetto di una costante shader [quando si dichiara un tipo di variabile](dx-graphics-hlsl-variable-syntax.md).

Quando si esegue il pacchetto di una costante, non è possibile combinare tipi costanti.

Il compilatore si comporta in modo leggermente diverso per le costanti globali e le costanti uniformi:

-   Costante globale. Una variabile globale viene aggiunta come costante globale *a* un $Global cbuffer dal compilatore. Gli elementi di tipo packed automaticamente (quelli dichiarati senza packoffset) verranno visualizzati dopo l'ultima variabile di tipo packed manualmente. È possibile combinare tipi durante la creazione di un pacchetto di costanti globali.
-   Costante uniforme. Un parametro uniforme nell'elenco di parametri di una funzione verrà aggiunto $Param un buffer costante di *$Param* dal compilatore quando lo shader viene compilato all'esterno del framework degli effetti. Quando viene compilata all'interno del framework degli effetti, una costante uniforme deve risolversi in una variabile uniforme definita nell'ambito globale. Non è possibile eseguire manualmente l'offset di una costante uniforme. L'uso consigliato è solo per la specializzazione degli shader in cui vengono di nuovo alias alle variabili globali, non come mezzo per passare i dati dell'applicazione nello shader.

Ecco alcuni esempi aggiuntivi: [creazione di un pacchetto di costanti usando il modello shader 4.](dx-graphics-hlsl-packing-rules.md)

## <a name="examples"></a>Esempio

Di seguito sono riportati alcuni esempi di creazione manuale di un pacchetto di costanti shader.

Creare un pacchetto di sottocomponenti di vettori e scalari la cui dimensione è sufficientemente grande da impedire l'attraversamento dei limiti del registro. Ad esempio, sono tutti validi:


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

 

 





