---
title: dcl_interface_dynamicindexed (SM5-ASM)
description: Dichiarare i puntatori a tabella di funzione (interfacce). | dcl_interface_dynamicindexed (SM5-ASM)
ms.assetid: 5C77EBB6-7AEC-4471-AA6E-0F6D3E215156
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f78bb0152b44f7e29b9e76221db13da0c465a434
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995693"
---
# <a name="dcl_interface_dynamicindexed-sm5---asm"></a>\_interfaccia DCL \_ dynamicindexed (SM5-ASM)

Dichiarare i puntatori a tabella di funzione (interfacce).



| \_interfaccia DCL \_ dynamicindexed FP \# \[ arraySize \] \[ numCallSites \] = {ft \# , ft \# ,...} |
|--------------------------------------------------------------------------------------|



 



| Elemento                                                          | Descrizione                                    |
|---------------------------------------------------------------|------------------------------------------------|
| <span id="fp_"></span><span id="FP_"></span>*FP\#*<br/> | \[nei \] puntatori della tabella di funzioni.<br/> |



 

## <a name="remarks"></a>Commenti

Ogni interfaccia deve essere associata dall'API prima che lo shader sia utilizzabile. Il binding fornisce un riferimento a una delle tabelle di funzioni in modo che sia possibile compilare gli slot del metodo. Il compilatore non genererà i puntatori per gli oggetti senza riferimenti.

Un puntatore a tabella di funzione dispone di un set completo di slot del metodo per evitare il livello aggiuntivo di riferimento indiretto che una rappresentazione da puntatore a puntatore a vtable di C++ richiederebbe. Questa operazione richiede anche che i puntatori siano di 5 tuple. Nel modello di incorporamento virtuale HLSL è sempre noto quale variabile/input globale viene usato per una chiamata, in modo da poter configurare le tabelle per ogni oggetto radice.

Le dichiarazioni di puntatore a funzione indicano quali tabelle di funzioni sono valide da usare con loro. Ciò consente anche la derivazione delle informazioni sulla correlazione dei metodi.

Il primo \[ \] di una dichiarazione di interfaccia è la dimensione della matrice. Se si utilizza l'indicizzazione dinamica, la dichiarazione indicherà che, come illustrato. Una matrice di puntatori di interfaccia può essere indicizzata anche in modo statico, ma non è necessario che le matrici di puntatori di interfaccia significhino l'indicizzazione dinamica.

Il numero di puntatori a interfaccia inizia da 0 per la prima dichiarazione e successivamente prende in considerazione la dimensione della matrice, quindi il primo puntatore dopo una matrice di quattro voci FP0 \[ 4 \] \[ 1 \] è 4PQ \[ \] \[ \] .

Il secondo \[ \] di una dichiarazione di interfaccia è il numero di siti di chiamata, che deve corrispondere al numero di corpi in ogni tabella a cui viene fatto riferimento nella dichiarazione.

Non sono previsti limiti per il numero di scelte della tabella function (ft \# ) che possono essere elencate in una dichiarazione di interfaccia.

Una determinata tabella di funzioni (ft \# ) può comparire più di una volta in una o più dichiarazioni di interfaccia.

### <a name="restrictions"></a>Restrizioni

-   Il numero di siti degli oggetti in uno shader, ovvero la somma in tutte le *dichiarazioni \# FP* delle \[ \] dichiarazioni arraySize, non deve essere superiore a 253. Questo numero corrisponde al numero di **puntatori** che possono essere presenti. Il Runtime impone questo limite di 253 per limitare le dimensioni dell'interfaccia DDI per la comunicazione di questi dati del puntatore.
-   Il numero di siti di chiamata in uno shader, ovvero la somma in tutte le istruzioni fcall del numero di potenziali destinazioni dei rami, non deve superare 4096.

    Ad esempio, un [fcall](fcall--sm5---asm-.md) che utilizza un indice statico per la prima *dimensione \[ \] \[ \] FP* viene conteggiato come uno:

    `                       fcall fp0[0][0]         // +1`

    Un **fcall** che utilizza un indice dinamico viene conteggiato come numero di elementi nella matrice (prima \[ \] dell' **\_ interfaccia DCL**):

    `                    dcl_interface_dynamicindexed fp1[2][1] = {ft2, ft3, ft4}                      ...                     `

    `fcall fp1[r0.z + 0][1]  // +2`

    Questo limite consente ad alcune implementazioni di adattare facilmente le tabelle delle selezioni del corpo della funzione in un archivio costante di tipo buffer.

Questa istruzione si applica alle fasi dello shader seguenti:



| Vertice | Hull | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Modello Shader minimo

Questa istruzione è supportata nei modelli shader seguenti:



| Modello di shader                                              | Supportato |
|-----------------------------------------------------------|-----------|
| [Modello Shader 5](d3d11-graphics-reference-sm5.md)        | sì       |
| [Modello Shader 4,1](dx-graphics-hlsl-sm4.md)              | no        |
| [Modello Shader 4](dx-graphics-hlsl-sm4.md)                | no        |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

cs \_ 4 \_ 0 e cs \_ 4 \_ 1 supportano questa istruzione per UAV e SRV.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Assembly Shader Model 5 (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





