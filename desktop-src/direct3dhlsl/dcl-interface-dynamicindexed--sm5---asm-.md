---
title: dcl_interface_dynamicindexed (sm5 - asm)
description: Dichiarare puntatori a tabella di funzione (interfacce). | dcl_interface_dynamicindexed (sm5 - asm)
ms.assetid: 5C77EBB6-7AEC-4471-AA6E-0F6D3E215156
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4bc52dc841b2e6de3c5af9725faac2c6dc5900b95117a28f77d8bc5087248df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118286053"
---
# <a name="dcl_interface_dynamicindexed-sm5---asm"></a>Interfaccia dcl \_ \_ dynamicindexed (sm5 - asm)

Dichiarare puntatori a tabella di funzione (interfacce).



| dcl \_ interface \_ dynamicindexed fp \# \[ arraySize \] \[ numCallSites \] = {ft , ft , \# \# ...} |
|--------------------------------------------------------------------------------------|



 



| Elemento                                                          | Descrizione                                    |
|---------------------------------------------------------------|------------------------------------------------|
| <span id="fp_"></span><span id="FP_"></span>*Fp\#*<br/> | \[in \] Puntatori alla tabella della funzione.<br/> |



 

## <a name="remarks"></a>Commenti

Ogni interfaccia deve essere associata dall'API prima che lo shader sia utilizzabile. L'associazione fornisce un riferimento a una delle tabelle di funzioni in modo che gli slot del metodo possano essere compilati. Il compilatore non genererà puntatori per gli oggetti senza riferimenti.

Un puntatore a tabella di funzione ha un set completo di slot di metodo per evitare il livello aggiuntivo di riferimento indiretto richiesto da una rappresentazione da puntatore a vtable del puntatore C++. Ciò richiederebbe anche che i puntatori siano a 5 tuple. Nel modello di inlining virtuale HLSL è sempre noto quale variabile/input globale viene usato per una chiamata, in modo da poter configurare tabelle per ogni oggetto radice.

Le dichiarazioni dei puntatori a funzione indicano quali tabelle di funzioni possono essere usate con esse. Ciò consente anche la derivazione delle informazioni di correlazione dei metodi.

La prima \[ \] di una dichiarazione di interfaccia è la dimensione della matrice. Se viene usata l'indicizzazione dinamica, la dichiarazione lo indicherà come illustrato. Una matrice di puntatori a interfaccia può essere indicizzata anche in modo statico. Non è necessario che le matrici di puntatori a interfaccia significherebbe l'indicizzazione dinamica.

La numerazione dei puntatori a interfaccia inizia da 0 per la prima dichiarazione e successivamente prende in considerazione le dimensioni della matrice, quindi il primo puntatore dopo una matrice di quattro voci fp0 \[ 4 1 sarebbe \] \[ \] fp4 \[ \] \[ \] .

Il secondo di una dichiarazione di interfaccia è il numero di siti di chiamata, che devono corrispondere al numero di corpi in ogni tabella a cui \[ \] si fa riferimento nella dichiarazione.

Non sono presenti limiti al numero di opzioni della tabella di funzioni (ft ) che \# possono essere elencate in una dichiarazione di interfaccia.

Una determinata tabella di funzioni (ft \# ) può essere visualizzata più di una volta in una o più dichiarazioni di interfaccia.

### <a name="restrictions"></a>Restrizioni

-   Il numero di siti di oggetti in uno shader, ovvero la somma in tutte le dichiarazioni *fp \#* delle dichiarazioni arraySize, non deve essere \[ maggiore di \] 253. Questo numero corrisponde al numero **di puntatori** this che possono essere presenti. Il runtime applica questo limite di 253 per mantenere un limite alle dimensioni dell'interfaccia DDI per la comunicazione di questi dati del puntatore.
-   Il numero di siti di chiamata in uno shader, ovvero la somma tra tutte le istruzioni fcall del numero di potenziali destinazioni di ramo, non deve essere maggiore di 4096.

    Ad esempio, una [chiamata fcall](fcall--sm5---asm-.md) che usa un indice statico per la prima *dimensione fp \[ \] \[ \]* viene conteggiato come uno:

    `                       fcall fp0[0][0]         // +1`

    Una **chiamata fcall** che usa un indice dinamico viene conteggiato come numero di elementi nella matrice (primo \[ \] dell'interfaccia **dcl \_**):

    `                    dcl_interface_dynamicindexed fp1[2][1] = {ft2, ft3, ft4}                      ...                     `

    `fcall fp1[r0.z + 0][1]  // +2`

    Questo limite consente ad alcune implementazioni di adattare facilmente le tabelle delle selezioni del corpo della funzione nell'archiviazione costante simile al buffer.

Questa istruzione si applica alle fasi di shader seguenti:



| Vertice | Scafo | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Modello di shader minimo

Questa istruzione è supportata nei modelli di shader seguenti:



| Modello di shader                                              | Supportato |
|-----------------------------------------------------------|-----------|
| [Modello shader 5](d3d11-graphics-reference-sm5.md)        | sì       |
| [Modello shader 4.1](dx-graphics-hlsl-sm4.md)              | no        |
| [Modello shader 4](dx-graphics-hlsl-sm4.md)                | no        |
| [Modello shader 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Modello shader 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Modello shader 1 (HLSL DirectX)](dx-graphics-hlsl-sm1.md) | no        |



 

cs \_ 4 \_ 0 e cs \_ 4 \_ 1 supportano questa istruzione per UAV e SRV.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Assembly del modello shader 5 (HLSL DirectX)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





