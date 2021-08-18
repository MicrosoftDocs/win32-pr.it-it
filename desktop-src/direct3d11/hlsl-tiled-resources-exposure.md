---
title: Esposizione delle risorse affiancate HLSL
description: È necessaria la nuova sintassi HLSL (Microsoft High Level Shader Language) per supportare le risorse affiancate in Shader Model 5.
ms.assetid: B6CE51E6-1BA9-4D15-9654-86FE9BAAF585
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c66ded502bebefc1061028115a12026f67c26cad89ddc57f98a5ae6fee923591
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119633331"
---
# <a name="hlsl-tiled-resources-exposure"></a>Esposizione delle risorse affiancate HLSL

La nuova sintassi HLSL (Microsoft High Level Shader Language) è necessaria per supportare le risorse affiancate in [Shader Model 5.](/windows/desktop/direct3dhlsl/d3d11-graphics-reference-sm5)

La nuova sintassi HLSL è consentita solo nei dispositivi con supporto delle risorse affiancate. Ogni metodo HLSL pertinente per le risorse affiancate nella tabella seguente accetta uno (feedback) o due parametri facoltativi aggiuntivi (chiusura e feedback in questo ordine). Ad esempio, un **metodo Sample** è:

**Sample(sampler, \[ location, \[ offset, \[ clamp, feedback \] \] \] )**

Un esempio di metodo **Sample** è [**Texture2D.Sample(S,float,int,float,uint)**](/windows/desktop/direct3dhlsl/t2darray-sample-s-float-int-float-uint-).

I parametri offset, clamp e feedback sono facoltativi. È necessario specificare tutti i parametri facoltativi fino a quello necessario, che è coerente con le regole C++ per gli argomenti di funzione predefiniti. Ad esempio, se lo stato del feedback è necessario, entrambi i parametri offset e clamp devono essere forniti in modo esplicito a **Sample,** anche se potrebbero non essere logicamente necessari.

Il parametro clamp è un valore float scalare. Il valore letterale clamp=0.0f indica che l'operazione di chiusura non viene eseguita.

Il parametro feedback è una **variabile uint** che è possibile fornire alla funzione intrinseca [**CheckAccessFullyMapped**](/windows/desktop/direct3dhlsl/checkaccessfullymapped) per l'accesso alla memoria. Non è necessario modificare o interpretare il valore del parametro feedback. ma il compilatore non fornisce analisi e diagnostica avanzate per rilevare se il valore è stato modificato.

Di seguito è illustrata la [**sintassi di CheckAccessFullyMapped:**](/windows/desktop/direct3dhlsl/checkaccessfullymapped)

**bool CheckAccessFullyMapped(in uint FeedbackVar);**

[**CheckAccessFullyMapped**](/windows/desktop/direct3dhlsl/checkaccessfullymapped) interpreta il valore *di FeedbackVar* e restituisce true se è stato eseguito il mapping di tutti i dati a cui si accede nella risorsa. in caso contrario, **CheckAccessFullyMapped** restituisce false.

Se è presente il parametro clamp o feedback, il compilatore genera una variante dell'istruzione di base. Ad esempio, l'esempio di una risorsa affiancata genera `sample_cl_s` l'istruzione . Se non si specifica alcun commento, il compilatore genera l'istruzione di base, in modo che non vi siano modifiche rispetto al comportamento corrente. Il valore di 0,0f indica che non viene eseguita alcuna morsa. Di conseguenza, il compilatore del driver può personalizzare ulteriormente l'istruzione in base all'hardware di destinazione. Se il feedback è un registro NULL in un'istruzione, il feedback non viene usato; Di conseguenza, il compilatore del driver può personalizzare ulteriormente l'istruzione in base all'architettura di destinazione.

Se il compilatore HLSL deduce che clamp è 0,0f e il feedback non viene usato, il compilatore genera l'istruzione di base corrispondente (ad esempio, `sample` anziché `sample_cl_s` ).

Se un accesso alle risorse affiancate è costituito da diverse istruzioni di codice byte costituenti, ad esempio per le risorse strutturate, il compilatore aggrega singoli valori di feedback tramite l'operazione OR per produrre il valore di feedback finale. Di conseguenza, viene visualizzato un singolo valore di feedback per un accesso così complesso.

Questa è la tabella di riepilogo dei metodi HLSL che vengono modificati per supportare feedback e/o chiusura. Tutti questi elementi funzionano su risorse affiancate e non affiancate di tutte le dimensioni. Le risorse non affiancate sembrano sempre essere completamente mappate.



| [Oggetti HLSL](/windows/desktop/direct3dhlsl/d3d11-graphics-reference-sm5-objects)                                                                                                                                                                                                                                | Metodi intrinseci con l'opzione feedback ( \* ) - ha anche l'opzione clamp                                                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \[Trama \] RW2D<br/> \[RW \] Texture2DArray<br/> TextureCUBE<br/> TextureCUBEArray<br/>                                                                                                                                                                                    | Raccogliere<br/> GatherRed<br/> GatherGreen<br/> GatherBlue<br/> GatherAlpha<br/> GatherCmp<br/> GatherCmpRed<br/> GatherCmpGreen<br/> GatherCmpBlue<br/> GatherCmpAlpha<br/> |
| \[Trama \] RW1D<br/> \[RW \] Texture1DArray<br/> \[Trama \] RW2D<br/> \[RW \] Texture2DArray<br/> \[Trama \] RW3D<br/> TextureCUBE<br/> TextureCUBEArray<br/>                                                                                              | Esempio\*<br/> SampleBias\*<br/> SampleCmp\*<br/> SampleCmpLevelZero<br/> SampleGrad\*<br/> SampleLevel<br/>                                                                                      |
| \[Trama \] RW1D<br/> \[RW \] Texture1DArray<br/> \[Trama \] RW2D<br/> Texture2DMS<br/> \[RW \] Texture2DArray<br/> Texture2DArrayMS<br/> \[Trama \] RW3D<br/> \[RW \] Buffer<br/> \[RW \] ByteAddressBuffer<br/> \[RW \] StructuredBuffer<br/> | Caricamento                                                                                                                                                                                                                                 |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Accesso della pipeline alle risorse affiancate](pipeline-access-to-tiled-resources.md)
</dt> </dl>

 

