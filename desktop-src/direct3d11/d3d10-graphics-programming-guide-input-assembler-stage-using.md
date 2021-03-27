---
title: Utilizzo di valori System-Generated
description: I valori generati dal sistema vengono generati dalla fase IA (in base alla semantica di input fornita dall'utente) per consentire una certa efficienza nelle operazioni dello shader.
ms.assetid: eed1e377-4b0e-4958-b6d4-945b2a952ad8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d484a42992206cb04aaef8fdd8ebaef6e08d7f4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047015"
---
# <a name="using-system-generated-values"></a>Utilizzo di valori System-Generated

I valori generati dal sistema vengono generati dalla fase IA (in base alla [semantica](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics)di input fornita dall'utente) per consentire una certa efficienza nelle operazioni dello shader.

Tramite il fissaggio dei dati, ad esempio un ID istanza (visibile a VS), un ID vertice (visibile a Visual Studio) o un ID primitivo (visibile a GS/PS), una fase successiva dello shader può cercare questi valori di sistema per ottimizzare l'elaborazione in tale fase. Ad esempio, la fase di VS può cercare l'ID dell'istanza per acquisire dati aggiuntivi per ogni vertice per lo shader o per eseguire altre operazioni; le fasi GS e PS possono usare l'ID primitivo per recuperare i dati per primitiva nello stesso modo.

-   [VertexID](#vertexid)
-   [PrimitiveID](#primitiveid)
-   [InstanceID](#instanceid)
-   [Esempio](#example)
-   [Argomenti correlati](#related-topics)

## <a name="vertexid"></a>VertexID

Un ID Vertex viene usato da ogni fase dello shader per identificare ogni vertice. Si tratta di un Unsigned Integer a 32 bit il cui valore predefinito è 0. Viene assegnato a un vertice quando la primitiva viene elaborata dalla fase IA. Alleghi la semantica dell'ID vertice alla dichiarazione di input dello shader per informare la fase IA per generare un ID per vertice.

L'IA aggiungerà un ID vertice a ogni vertice per l'uso da parte delle fasi dello shader. Per ogni chiamata di progetto, l'ID Vertex viene incrementato di 1. Nelle chiamate di disegni indicizzati, il conteggio viene reimpostato nuovamente sul valore iniziale. Per [**sul ID3D11DeviceContext::D rawindexed**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawindexed) e [**sul ID3D11DeviceContext::D rawindexedinstanced**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawindexedinstanced), l'ID vertice rappresenta il valore di indice. Se l'ID vertice si verifica in overflow (supera 2 ³ ²-1), viene eseguito il wrapping a 0.

Per tutti i tipi primitivi, ai vertici è associato un ID vertice (indipendentemente da adiacenza).

## <a name="primitiveid"></a>PrimitiveID

Un ID primitivo viene usato da ogni fase dello shader per identificare ogni primitiva. Si tratta di un Unsigned Integer a 32 bit il cui valore predefinito è 0. Viene assegnato a una primitiva quando la primitiva viene elaborata dalla fase IA. Per informare la fase IA per generare un ID primitivo, alleghi la semantica dell'ID primitivo alla dichiarazione di input dello shader.

La fase IA aggiungerà un ID primitivo a ogni primitiva per l'uso da parte del geometry shader o della fase pixel shader (a seconda della fase attiva dopo la fase IA). Per ogni chiamata di creazione indicizzata, l'ID primitivo viene incrementato di 1, tuttavia, l'ID primitivo viene reimpostato su 0 ogni volta che viene avviata una nuova istanza. Tutte le altre chiamate di estrazione non modificano il valore dell'ID istanza. Se l'ID dell'istanza ha un overflow (supera 2 ³ ²-1), viene eseguito il wrapping a 0.

La fase pixel shader non dispone di un input separato per un ID primitivo. Tuttavia, qualsiasi input pixel shader che specifica un ID primitivo usa una modalità di interpolazione costante.

Non è disponibile alcun supporto per la generazione automatica di un ID primitivo per le primitive adiacenti. Per i tipi primitivi con adiacenza, ad esempio una striscia di triangolo con adiacenza, un ID primitivo viene mantenuto solo per le primitive interne (le primitive non adiacenti), proprio come il set di primitive in una striscia di triangolo senza adiacenza.

## <a name="instanceid"></a>InstanceID

Un ID istanza viene usato da ogni fase dello shader per identificare l'istanza della geometria attualmente in fase di elaborazione. Si tratta di un Unsigned Integer a 32 bit il cui valore predefinito è 0.

La fase IA aggiungerà un ID istanza a ogni vertice se la dichiarazione di input vertex shader include la semantica dell'ID istanza. Per ogni chiamata di estrazione indicizzata, l'ID istanza viene incrementato di 1. Tutte le altre chiamate di estrazione non modificano il valore di ID istanza. Se l'ID dell'istanza ha un overflow (supera 2 ³ ²-1), viene eseguito il wrapping a 0.

## <a name="example"></a>Esempio

Nella figura seguente viene illustrato il modo in cui i valori di sistema sono collegati a una striscia di triangolo con istanza nella fase IA.

![illustrazione dei valori di sistema per una striscia di triangolo con istanza](images/d3d10-ia-example.png)

In queste tabelle vengono illustrati i valori di sistema generati per entrambe le istanze della stessa striscia di triangolo. La prima istanza (istanza U) viene visualizzata in blu, la seconda istanza (istanza V) viene visualizzata in verde. Le linee continue connettono i vertici nelle primitive, le linee tratteggiate connettono i vertici adiacenti.

Nelle tabelle seguenti vengono illustrati i valori generati dal sistema per l'istanza U.



| Dati dei vertici    | C, U | D, U | E, U | F, U | G, U | H, U | I, U | J, U | K, U | L, U |
|----------------|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| **VertexID**   | 0   | 1   | 2   | 3   | 4   | 5   | 6   | 7   | 8   | 9   |
| **InstanceID** | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   |



 



|                 |     |     |     |
|-----------------|-----|-----|-----|
| **PrimitiveID** | 0   | 1   | 2   |
| **InstanceID**  | 0   | 0   | 0   |



 

Nelle tabelle seguenti vengono illustrati i valori generati dal sistema per l'istanza V.



| Dati dei vertici    | C, V | D, V | E, V | F, V | G, V | H, V | I, V | J, V | K, V | L, V |
|----------------|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| **VertexID**   | 0   | 1   | 2   | 3   | 4   | 5   | 6   | 7   | 8   | 9   |
| **InstanceID** | 1   | 1   | 1   | 1   | 1   | 1   | 1   | 1   | 1   | 1   |



 



|                 |     |     |     |
|-----------------|-----|-----|-----|
| **PrimitiveID** | 0   | 1   | 2   |
| **InstanceID**  | 1   | 1   | 1   |



 

L'assembler di input genera gli ID (vertice, primitiva e istanza); Si noti inoltre che a ogni istanza viene assegnato un ID istanza univoco. I dati terminano con lo strip Cut, che separa ogni istanza della striscia di triangolo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Fase input-assembler](d3d10-graphics-programming-guide-input-assembler-stage.md)
</dt> </dl>

 

 