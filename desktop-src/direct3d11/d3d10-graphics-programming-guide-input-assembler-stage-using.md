---
title: Uso System-Generated valori
description: I valori generati dal sistema vengono generati dalla fase IA (in base alla semantica di input fornita dall'utente) per consentire determinate efficienze nelle operazioni dello shader.
ms.assetid: eed1e377-4b0e-4958-b6d4-945b2a952ad8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ccdc723d335fd78277051099ec05b43ed954174d
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335205"
---
# <a name="using-system-generated-values"></a>Uso System-Generated valori

I valori generati dal sistema vengono generati dalla fase IA (in base alla [semantica](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics)di input fornita dall'utente) per consentire determinate efficienze nelle operazioni dello shader.

Collegando dati, ad esempio un ID istanza (visibile a Visual Studio), un ID vertice (visibile a Visual Studio) o un ID primitivo (visibile a GS/PS), una fase dello shader successiva può cercare questi valori di sistema per ottimizzare l'elaborazione in tale fase. Ad esempio, la fase di Visual Studio può cercare l'ID istanza per recuperare dati aggiuntivi per ogni vertice per lo shader o per eseguire altre operazioni. Le fasi GS e PS possono usare l'ID primitivo per acquisire i dati per primitivi nello stesso modo.

-   [VertexID](#vertexid)
-   [PrimitiveID](#primitiveid)
-   [InstanceID](#instanceid)
-   [Esempio](#example)
-   [Argomenti correlati](#related-topics)

## <a name="vertexid"></a>VertexID

Ogni fase dello shader usa un ID vertice per identificare ogni vertice. È un intero senza segno a 32 bit il cui valore predefinito è 0. Viene assegnato a un vertice quando la primitiva viene elaborata dalla fase IA. Collegare la semantica vertex-id alla dichiarazione di input dello shader per informare la fase IA di generare un ID per vertice.

L'IA aggiungerà un ID vertice a ogni vertice per l'uso da parte delle fasi dello shader. Per ogni chiamata di disegno, l'ID vertice viene incrementato di 1. Nelle chiamate di disegno indicizzate, il conteggio viene reimpostato sul valore iniziale. Per [**ID3D11DeviceContext::D rawIndexed**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawindexed) e [**ID3D11DeviceContext::D rawIndexedInstanced**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawindexedinstanced), l'ID vertice rappresenta il valore di indice. Se l'ID vertice supera (supera 2°- 1), esegue il wrapping su 0.

Per tutti i tipi primitivi, ai vertici è associato un ID vertice (indipendentemente dall'adienza).

## <a name="primitiveid"></a>PrimitiveID

Ogni fase dello shader usa un ID primitivo per identificare ogni primitiva. Intero senza segno a 32 bit il cui valore predefinito è 0. Viene assegnato a una primitiva quando la primitiva viene elaborata dalla fase IA. Per informare la fase IA di generare un ID primitivo, collegare la semantica primitiva-id alla dichiarazione di input dello shader.

La fase IA aggiungerà un ID primitivo a ogni primitiva per l'uso da parte dello shader geometry o della fase pixel shader (a seconda della prima fase attiva dopo la fase IA). Per ogni chiamata di disegno indicizzato, l'ID primitivo viene incrementato di 1, tuttavia, l'ID primitivo viene reimpostato su 0 ogni volta che inizia una nuova istanza. Tutte le altre chiamate di disegno non modificano il valore dell'ID istanza. Se l'ID istanza è in overflow (è maggiore di 2-2-1), viene a capo su 0.

La pixel shader non dispone di un input separato per un ID primitivo. Tuttavia, qualsiasi input pixel shader che specifica un ID primitivo usa una modalità di interpolazione costante.

Non è disponibile alcun supporto per la generazione automatica di un ID primitivo per le primitive adiacenti. Per i tipi primitivi con adizia, ad esempio una striscia di triangoli con adizia, un ID primitivo viene mantenuto solo per le primitive interne (primitive non adiacenti), proprio come il set di primitive in una striscia di triangoli senza adigienza.

## <a name="instanceid"></a>InstanceID

Un ID istanza viene usato da ogni fase dello shader per identificare l'istanza della geometria attualmente in fase di elaborazione. Intero senza segno a 32 bit il cui valore predefinito è 0.

La fase IA aggiungerà un ID istanza a ogni vertice se la dichiarazione di input del vertex shader include la semantica dell'ID istanza. Per ogni chiamata di disegno indicizzato, l'ID istanza viene incrementato di 1. Tutte le altre chiamate di disegno non modificano il valore dell'ID istanza. Se l'ID istanza è in overflow (supera 2°- 1), viene a capo su 0.

## <a name="example"></a>Esempio

La figura seguente mostra come i valori di sistema vengono associati a una striscia triangolare con istanze nella fase IA.

![Illustrazione dei valori di sistema per una striscia triangolare con istanze](images/d3d10-ia-example.png)

Queste tabelle mostrano i valori di sistema generati per entrambe le istanze della stessa striscia triangolare. La prima istanza (istanza U) viene visualizzata in blu, la seconda istanza (istanza V) viene visualizzata in verde. Le linee solide connettono i vertici nelle primitive, le linee tratteggiate connettono i vertici adiacenti.

Le tabelle seguenti illustrano i valori generati dal sistema per l'istanza U.



| Vertex Data    | C,U | D, U | E,U | fanculo | G, U | H, U | I,U | J, U | K, U | L,U |
|----------------|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| **VertexID**   | 0   | 1   | 2   | 3   | 4   | 5   | 6   | 7   | 8   | 9   |
| **InstanceID** | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   |



 



|                 | Valore    | Valore    | Valore    |
|-----------------|-----|-----|-----|
| **PrimitiveID** | 0   | 1   | 2   |
| **InstanceID**  | 0   | 0   | 0   |



 

Le tabelle seguenti illustrano i valori generati dal sistema per l'istanza V.



| Vertex Data    | C,V | D, V | E,V | F,V | G,V | H,V | I,V | J,V | K,V | L,V |
|----------------|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| **VertexID**   | 0   | 1   | 2   | 3   | 4   | 5   | 6   | 7   | 8   | 9   |
| **InstanceID** | 1   | 1   | 1   | 1   | 1   | 1   | 1   | 1   | 1   | 1   |



 



|                 |Valore     | Valore    |  Valore   |
|-----------------|-----|-----|-----|
| **PrimitiveID** | 0   | 1   | 2   |
| **InstanceID**  | 1   | 1   | 1   |



 

L'assembler di input genera gli ID (vertice, primitiva e istanza); Si noti anche che a ogni istanza viene assegnato un ID istanza univoco. I dati terminano con la striscia tagliata, che separa ogni istanza della striscia triangolare.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Fase dell'assembler di input](d3d10-graphics-programming-guide-input-assembler-stage.md)
</dt> </dl>

 

 