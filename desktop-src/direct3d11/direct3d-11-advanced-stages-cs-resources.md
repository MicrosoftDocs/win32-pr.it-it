---
title: Nuovi tipi di risorse
description: In Direct3D 11 sono stati aggiunti diversi nuovi tipi di risorse.
ms.assetid: 597cc12f-dd0e-4603-b670-3f584f25e192
keywords:
- Buffer indirizzi byte (panoramica)
- Buffer di lettura/scrittura (panoramica)
- Buffer strutturato (panoramica)
- Buffer di accesso non ordinato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6ab9e6f1677770b1a40766b846f4675df9eaa3809b42838783ddb834044bfe2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119566301"
---
# <a name="new-resource-types"></a>Nuovi tipi di risorse

In Direct3D 11 sono stati aggiunti diversi nuovi tipi di risorse.

-   [Buffer e trame di lettura/scrittura](#readwrite-buffers-and-textures)
-   [Buffer strutturato](#structured-buffer)
-   [Byte Address Buffer](#byte-address-buffer)
-   [Buffer di accesso non ordinato o trama](#unordered-access-buffer-or-texture)
    -   [Accodare e utilizzare il buffer](#append-and-consume-buffer)
-   [Argomenti correlati](#related-topics)

## <a name="readwrite-buffers-and-textures"></a>Buffer e trame di lettura/scrittura

Le risorse del modello shader 4 sono di sola lettura. Il modello shader 5 implementa un nuovo set corrispondente di risorse di lettura/scrittura:

-   [RWBuffer](/windows/desktop/direct3dhlsl/sm5-object-rwbuffer)
-   [RWTexture1D](/windows/desktop/direct3dhlsl/sm5-object-rwtexture1d), [RWTexture1DArray](/windows/desktop/direct3dhlsl/sm5-object-rwtexture1darray)
-   [RWTexture2D](/windows/desktop/direct3dhlsl/sm5-object-rwtexture2d), [RWTexture2DArray](/windows/desktop/direct3dhlsl/sm5-object-rwtexture2darray)
-   [RWTexture3D](/windows/desktop/direct3dhlsl/sm5-object-rwtexture3d)

Queste risorse richiedono una variabile di risorsa per accedere alla memoria (tramite indicizzazione) perché non sono disponibili metodi per accedere direttamente alla memoria. Una variabile di risorsa può essere usata sul lato sinistro e destro di un'equazione. Se usato a destra, il tipo di modello deve essere un singolo componente (float, int o uint).

## <a name="structured-buffer"></a>Buffer strutturato

Un buffer strutturato è un buffer che contiene elementi di dimensioni uguali. Usare una struttura con uno o più tipi di membro per definire un elemento. Ecco una struttura con tre membri.


```
struct MyStruct
{
    float4 Color;
    float4 Normal;
    bool isAwesome;
};
```



Usare questa struttura per dichiarare un buffer strutturato simile al seguente:


```
StructuredBuffer<MyStruct> mySB;
```



Oltre all'indicizzazione, un buffer strutturato supporta l'accesso a un singolo membro come il seguente:


```
float4 myColor = mySb[27].Color;
```



Usare i tipi di oggetto seguenti per accedere a un buffer strutturato:

-   [StructuredBuffer è](/windows/desktop/direct3dhlsl/sm5-object-structuredbuffer) un buffer strutturato di sola lettura.
-   [RWStructuredBuffer](/windows/desktop/direct3dhlsl/sm5-object-rwstructuredbuffer) è un buffer strutturato di lettura/scrittura.

[Le funzioni atomiche](direct3d-11-advanced-stages-cs-atomic-functions.md) che implementano operazioni interlocked sono consentite sugli elementi int e uint in **RWStructuredBuffer.**

## <a name="byte-address-buffer"></a>Byte Address Buffer

Un buffer di indirizzi di byte è un buffer il cui contenuto è indirizzabile da un offset di byte. In genere, il contenuto di un [buffer](overviews-direct3d-11-resources-buffers-intro.md) viene indicizzato per ogni elemento usando uno stride per ogni elemento (S) e il numero di elemento (N) come specificato da S \* N. Un buffer di indirizzi di byte, che può anche essere chiamato buffer non elaborato, usa un offset di valore byte dall'inizio del buffer per accedere ai dati. Il valore byte deve essere un multiplo di quattro in modo che sia allineato con DWORD. Se viene specificato qualsiasi altro valore, il comportamento non è definito.

Il modello shader 5 introduce oggetti per l'accesso a un buffer di indirizzi [di byte](/windows/desktop/direct3dhlsl/sm5-object-byteaddressbuffer) di sola lettura e a un buffer di indirizzi byte di [lettura/scrittura.](/windows/desktop/direct3dhlsl/sm5-object-rwbyteaddressbuffer) Il contenuto di un buffer di indirizzi di byte è progettato per essere un intero senza segno a 32 bit; Se il valore nel buffer non è effettivamente un intero senza segno, usare una funzione come [**ad esempiofloat**](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-asfloat) per leggerlo.

## <a name="unordered-access-buffer-or-texture"></a>Buffer di accesso non ordinato o trama

Una risorsa di accesso non ordinato (che include buffer, trame e matrici di trame, senza multicampionamento), consente l'accesso in lettura/scrittura non ordinato a livello temporale da più thread. Ciò significa che questo tipo di risorsa può essere letto/scritto contemporaneamente da più thread senza generare conflitti di memoria tramite l'uso di [Funzioni atomiche](direct3d-11-advanced-stages-cs-atomic-functions.md).

Creare un buffer o una trama di accesso non ordinato chiamando una funzione come [**ID3D11Device::CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) o [**ID3D11Device::CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d) e passando il flag **BIND \_ \_ UNORDERED \_ ACCESS D3D11** dall'enumerazione [**BIND \_ \_ FLAG D3D11.**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag)

Le risorse di accesso non ordinato possono essere associate solo a pixel shader e compute shader. Durante l'esecuzione, i pixel shader o i compute shader in esecuzione in parallelo hanno le stesse risorse di accesso non ordinate associate.

### <a name="append-and-consume-buffer"></a>Accodare e utilizzare il buffer

Un buffer di accodamento e utilizzo è un tipo speciale di una risorsa non ordinata che supporta l'aggiunta e la rimozione di valori dalla fine di un buffer in modo simile al funzionamento di uno stack.

Un buffer di accodamento e utilizzo deve essere un buffer strutturato:

-   [AppendStructuredBuffer](/windows/desktop/direct3dhlsl/sm5-object-appendstructuredbuffer)
-   [ConsumeStructuredBuffer](/windows/desktop/direct3dhlsl/sm5-object-consumestructuredbuffer)

Usare queste risorse tramite i relativi metodi. Queste risorse non usano variabili di risorsa.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Cenni preliminari sul compute shader](direct3d-11-advanced-stages-compute-shader.md)
</dt> </dl>

 

 