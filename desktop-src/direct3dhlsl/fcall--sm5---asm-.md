---
title: fcall (sm5 - asm)
description: Chiamata di funzione dell'interfaccia.
ms.assetid: C21784A0-D2F4-4DDE-9AC4-4F21351BCA6E
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7781fc0a2fc7bbd715084d3c0e9682a433ddf16e4492724df8fdb2e31c84689
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119854511"
---
# <a name="fcall-sm5---asm"></a>fcall (sm5 - asm)

Chiamata di funzione dell'interfaccia.



| fcall fp \# \[ arrayIndex \] \[ callSite\] |
|--------------------------------------|



 



| Elemento                                                                                                           | Descrizione                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="fp_"></span><span id="FP_"></span>*Fp\#*<br/>                                                  | \[in \] Puntatore a funzione.<br/>                                                                                                                                                                                                                                                                    |
| <span id="arrayIndex"></span><span id="arrayindex"></span><span id="ARRAYINDEX"></span>*Arrayindex*<br/> | \[in \] Facoltativo. Specifica un offset nella matrice di puntatori a funzione. Questo parametro deve essere un intero senza segno letterale se fp \# non è stato dichiarato come indicizzabile. In caso contrario, arrayIndex può essere nel formato letterale base + offset da un registro shader. Ad esempio, fcall fp1 \[ r1.w + 0 \] \[ 0 \] .<br/> |
| <span id="_callSite"></span><span id="_callsite"></span><span id="_CALLSITE"></span>*callSite*<br/>     | \[in \] Facoltativo. Offset di un intero senza segno letterale nella tabella della funzione selezionata, selezionando un corpo della funzione fb \# da eseguire. <br/>                                                                                                                                                                |



 

## <a name="remarks"></a>Commenti

*fp \#* \[  \] \[ arrayIndex \] viene risolto in una tabella di funzioni specifica, selezionata dall'API all'esterno dello shader dalle opzioni della tabella della funzione elencate nella dichiarazione di *fp \#*.

La somma di \# in *fp \# e* *arrayIndex* seleziona la tabella delle funzioni. Ad esempio, se un'interfaccia viene dichiarata come fp4 4 4 3 (dimensione della matrice 4), le fcall s seguenti sono \[ \] \[ \] equivalenti: fcall fp4  \[ 2 \] \[ 3 e \] fp5 \[ 1 3, perché \] \[ \] 4+2 = 5+1.

### <a name="restrictions"></a>Restrizioni

-   Se *arrayIndex usa* l'indicizzazione dinamica, il comportamento non è definito se *arrayIndex* diverge sulle chiamate shader adiacenti, che potrebbero essere in esecuzione in lockstep. Il compilatore HLSL tenterà di non consentire questo caso.

    Le chiamate adiacenti possono essere inattive a causa del controllo di flusso, perché non interrompe l'esecuzione di lockstep.

-   Se *\# fp*  +  *arrayIndex* specifica un indice fuori limite, il comportamento non è definito.
-   Per i casi non definiti descritti qui, significa che il comportamento del dispositivo D3D corrente diventa indefinito, inclusa la possibilità di dispositivo perso. Tuttavia, nessuna memoria esterna al dispositivo D3D corrente verrà accessibile o eseguita come codice.

Questa istruzione si applica alle fasi dello shader seguenti:



| Vertice | Scafo | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

### <a name="minimum-shader-model"></a>Modello shader minimo

Questa istruzione è supportata nei modelli shader seguenti:



| Modello di shader                                              | Supportato |
|-----------------------------------------------------------|-----------|
| [Modello shader 5](d3d11-graphics-reference-sm5.md)        | sì       |
| [Modello shader 4.1](dx-graphics-hlsl-sm4.md)              | no        |
| [Modello shader 4](dx-graphics-hlsl-sm4.md)                | no        |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Modello shader 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Modello shader 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Assembly del modello shader 5 (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





