---
title: Nuovi tipi di risorse
description: In Direct3D 11 sono stati aggiunti diversi nuovi tipi di risorse.
ms.assetid: 597cc12f-dd0e-4603-b670-3f584f25e192
keywords:
- Buffer degli indirizzi byte (panoramica)
- Buffer di lettura/scrittura (panoramica)
- Buffer strutturato (panoramica)
- Buffer di accesso non ordinato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4b7a75ec95917a5ee819126e42dce3117994574
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399360"
---
# <a name="new-resource-types"></a>Nuovi tipi di risorse

In Direct3D 11 sono stati aggiunti diversi nuovi tipi di risorse.

-   [Buffer e trame di lettura/scrittura](#readwrite-buffers-and-textures)
-   [Buffer strutturato](#structured-buffer)
-   [Buffer degli indirizzi byte](#byte-address-buffer)
-   [Buffer o trama di accesso non ordinato](#unordered-access-buffer-or-texture)
    -   [Accoda e utilizza buffer](#append-and-consume-buffer)
-   [Argomenti correlati](#related-topics)

## <a name="readwrite-buffers-and-textures"></a>Buffer e trame di lettura/scrittura

Le risorse del modello Shader 4 sono di sola lettura. Shader Model 5 implementa un nuovo set corrispondente di risorse di lettura/scrittura:

-   [RWBuffer](/windows/desktop/direct3dhlsl/sm5-object-rwbuffer)
-   [RWTexture1D](/windows/desktop/direct3dhlsl/sm5-object-rwtexture1d), [RWTexture1DArray](/windows/desktop/direct3dhlsl/sm5-object-rwtexture1darray)
-   [RWTexture2D](/windows/desktop/direct3dhlsl/sm5-object-rwtexture2d), [RWTexture2DArray](/windows/desktop/direct3dhlsl/sm5-object-rwtexture2darray)
-   [RWTexture3D](/windows/desktop/direct3dhlsl/sm5-object-rwtexture3d)

Queste risorse richiedono una variabile di risorsa per accedere alla memoria (tramite l'indicizzazione) perché non sono disponibili metodi per accedere direttamente alla memoria. Una variabile di risorsa può essere usata a destra e a sinistra di un'equazione. Se usato sul lato destro, il tipo di modello deve essere un singolo componente (float, int o uint).

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



Usare questa struttura per dichiarare un buffer strutturato come il seguente:


```
StructuredBuffer<MyStruct> mySB;
```



Oltre all'indicizzazione, un buffer strutturato supporta l'accesso a un singolo membro come il seguente:


```
float4 myColor = mySb[27].Color;
```



Usare i tipi di oggetti seguenti per accedere a un buffer strutturato:

-   [StructuredBuffer](/windows/desktop/direct3dhlsl/sm5-object-structuredbuffer) è un buffer strutturato di sola lettura.
-   [RWStructuredBuffer](/windows/desktop/direct3dhlsl/sm5-object-rwstructuredbuffer) è un buffer strutturato di lettura/scrittura.

Le [funzioni atomiche](direct3d-11-advanced-stages-cs-atomic-functions.md) che implementano operazioni interlocked sono consentite su elementi int e uint in un **RWStructuredBuffer**.

## <a name="byte-address-buffer"></a>Buffer degli indirizzi byte

Un buffer di indirizzi byte è un buffer il cui contenuto è indirizzabile da un offset di byte. In genere, il contenuto di un [buffer](overviews-direct3d-11-resources-buffers-intro.md) viene indicizzato per ogni elemento usando uno stride per ogni elemento e il numero di elemento (N) come specificato da S \* N. Un buffer di indirizzi byte, che può essere chiamato anche buffer non elaborato, usa un offset di valore byte dall'inizio del buffer per accedere ai dati. Il valore byte deve essere un multiplo di quattro in modo che sia DWORD allineato. Se viene specificato un altro valore, il comportamento non è definito.

Shader Model 5 introduce gli oggetti per l'accesso a un [buffer di indirizzi byte](/windows/desktop/direct3dhlsl/sm5-object-byteaddressbuffer) di sola lettura, oltre a un [buffer di indirizzi byte di lettura e scrittura](/windows/desktop/direct3dhlsl/sm5-object-rwbyteaddressbuffer). Il contenuto di un buffer di indirizzi byte è progettato per essere un Unsigned Integer a 32 bit; Se il valore nel buffer non è effettivamente un Unsigned Integer, usare una funzione come [**AsFloat**](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-asfloat) per leggerlo.

## <a name="unordered-access-buffer-or-texture"></a>Buffer o trama di accesso non ordinato

Una risorsa di accesso non ordinato, che include buffer, trame e matrici di trama, senza campionamento multiplo, consente un accesso in lettura/scrittura non ordinato da più thread. Questo significa che questo tipo di risorsa può essere letto/scritto simultaneamente da più thread senza generare conflitti di memoria tramite l'utilizzo di [funzioni atomiche](direct3d-11-advanced-stages-cs-atomic-functions.md).

Creare una trama o un buffer di accesso non ordinato chiamando una funzione, ad esempio [**ID3D11Device:: CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) o [**ID3D11Device:: CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d) , e passando il flag di **accesso non \_ \_ ordinato \_ di binding d3d11** dall'enumerazione del [**\_ \_ flag di binding d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag) .

Le risorse di accesso non ordinato possono essere limitate solo a pixel shader e compute shader. Durante l'esecuzione, i pixel shader o i compute shader eseguiti in parallelo hanno le stesse risorse di accesso non ordinato associato.

### <a name="append-and-consume-buffer"></a>Accoda e utilizza buffer

Un buffer di Accodamento e utilizzo è un tipo speciale di risorsa non ordinata che supporta l'aggiunta e la rimozione di valori dalla fine di un buffer in modo analogo al funzionamento di uno stack.

Un buffer di Accodamento e di utilizzo deve essere un buffer strutturato:

-   [AppendStructuredBuffer](/windows/desktop/direct3dhlsl/sm5-object-appendstructuredbuffer)
-   [ConsumeStructuredBuffer](/windows/desktop/direct3dhlsl/sm5-object-consumestructuredbuffer)

Usare queste risorse tramite i relativi metodi, che non usano variabili di risorsa.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Panoramica di Compute Shader](direct3d-11-advanced-stages-compute-shader.md)
</dt> </dl>

 

 