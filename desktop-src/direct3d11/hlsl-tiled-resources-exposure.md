---
title: Esposizione delle risorse affiancate HLSL
description: Per supportare le risorse affiancate nel modello di shader 5 è necessaria la nuova sintassi Microsoft High Level Shader Language (HLSL).
ms.assetid: B6CE51E6-1BA9-4D15-9654-86FE9BAAF585
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2b266b98045b38645e1e8d24ed0014a5f448a38
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473603"
---
# <a name="hlsl-tiled-resources-exposure"></a>Esposizione delle risorse affiancate HLSL

Per supportare le risorse affiancate nel [modello di shader 5](/windows/desktop/direct3dhlsl/d3d11-graphics-reference-sm5)è necessaria la nuova sintassi Microsoft High Level Shader Language (HLSL).

La nuova sintassi HLSL è consentita solo nei dispositivi con supporto di risorse affiancato. Ogni metodo HLSL pertinente per le risorse affiancate nella tabella seguente accetta una (commenti e suggerimenti) o due (morsetto e commenti in questo ordine) altri parametri facoltativi. Ad esempio, un metodo di **esempio** è:

**Esempio (Sampler, location \[ , offset \[ , Clamp \[ , feedback \] \] \] )**

Un esempio di metodo di **esempio** è [**Texture2D. Sample (S, float, int, float, uint)**](/windows/desktop/direct3dhlsl/t2darray-sample-s-float-int-float-uint-).

I parametri offset, Clamp e feedback sono facoltativi. È necessario specificare tutti i parametri facoltativi fino a quello necessario, coerente con le regole C++ per gli argomenti della funzione predefiniti. Se, ad esempio, lo stato del feedback è necessario, è necessario specificare in modo esplicito i parametri offset e clamp per l' **esempio**, anche se potrebbero non essere logicamente necessari.

Il parametro Clamp è un valore float scalare. Il valore letterale di Clamp = 0,0 f indica che l'operazione clamp non viene eseguita.

Il parametro feedback è una variabile **uint** che è possibile fornire alla funzione [**CheckAccessFullyMapped**](/windows/desktop/direct3dhlsl/checkaccessfullymapped) intrinseca di query di accesso alla memoria. Non è necessario modificare o interpretare il valore del parametro feedback. Tuttavia, il compilatore non fornisce alcuna analisi e diagnostica avanzata per rilevare se il valore è stato modificato.

Di seguito è illustrata la sintassi di [**CheckAccessFullyMapped**](/windows/desktop/direct3dhlsl/checkaccessfullymapped):

**bool CheckAccessFullyMapped (in uint FeedbackVar);**

[**CheckAccessFullyMapped**](/windows/desktop/direct3dhlsl/checkaccessfullymapped) interpreta il valore di *FeedbackVar* e restituisce true se è stato eseguito il mapping di tutti i dati a cui è stato eseguito il mapping nella risorsa. in caso contrario, **CheckAccessFullyMapped** restituisce false.

Se è presente il parametro clamp o feedback, il compilatore genera una variante dell'istruzione di base. Ad esempio, l'esempio di una risorsa affiancata genera l' `sample_cl_s` istruzione. Se non viene specificato né il morsetto né il feedback, il compilatore genera l'istruzione di base, in modo che non vi siano modifiche rispetto al comportamento corrente. Il valore del morsetto 0,0 f indica che non viene eseguito alcun morsetto; di conseguenza, il compilatore di driver può adattare ulteriormente l'istruzione all'hardware di destinazione. Se il feedback è un registro NULL in un'istruzione, il feedback è inutilizzato. di conseguenza, il compilatore di driver può personalizzare ulteriormente l'istruzione nell'architettura di destinazione.

Se il compilatore HLSL deduce che Clamp è 0,0 f e il feedback è inutilizzato, il compilatore genera l'istruzione di base corrispondente, ad esempio `sample` invece di `sample_cl_s` .

Se l'accesso a una risorsa affiancata è costituito da diverse istruzioni per il codice di byte costitutive, ad esempio per le risorse strutturate, il compilatore aggrega i singoli valori di feedback tramite l'operazione o per produrre il valore di feedback finale. Viene pertanto visualizzato un singolo valore di feedback per tale accesso complesso.

Si tratta della tabella riepilogativa dei metodi HLSL che sono stati modificati per supportare feedback e/o clamp. Tutti funzionano su risorse affiancate e non affiancate di tutte le dimensioni. Le risorse non affiancate sembrano sempre completamente mappate.



| [Oggetti HLSL](/windows/desktop/direct3dhlsl/d3d11-graphics-reference-sm5-objects)                                                                                                                                                                                                                                | Metodi intrinseci con l'opzione feedback ( \* )-anche con l'opzione Clamp                                                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \[\]TEXTURE2D RW<br/> \[\]TEXTURE2DARRAY RW<br/> TextureCUBE<br/> TextureCUBEArray<br/>                                                                                                                                                                                    | Raccogliere<br/> GatherRed<br/> GatherGreen<br/> GatherBlue<br/> GatherAlpha<br/> GatherCmp<br/> GatherCmpRed<br/> GatherCmpGreen<br/> GatherCmpBlue<br/> GatherCmpAlpha<br/> |
| \[\]TEXTURE1D RW<br/> \[\]TEXTURE1DARRAY RW<br/> \[\]TEXTURE2D RW<br/> \[\]TEXTURE2DARRAY RW<br/> \[\]TEXTURE3D RW<br/> TextureCUBE<br/> TextureCUBEArray<br/>                                                                                              | Esempio\*<br/> SampleBias\*<br/> SampleCmp\*<br/> SampleCmpLevelZero<br/> SampleGrad\*<br/> SampleLevel<br/>                                                                                      |
| \[\]TEXTURE1D RW<br/> \[\]TEXTURE1DARRAY RW<br/> \[\]TEXTURE2D RW<br/> Texture2DMS<br/> \[\]TEXTURE2DARRAY RW<br/> Texture2DArrayMS<br/> \[\]TEXTURE3D RW<br/> \[\]Buffer RW<br/> \[\]BYTEADDRESSBUFFER RW<br/> \[\]STRUCTUREDBUFFER RW<br/> | Caricamento                                                                                                                                                                                                                                 |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Accesso alla pipeline alle risorse affiancate](pipeline-access-to-tiled-resources.md)
</dt> </dl>

 

