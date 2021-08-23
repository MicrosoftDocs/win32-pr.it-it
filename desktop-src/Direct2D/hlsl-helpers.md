---
title: Helper HLSL
description: Per assistere gli autori di effetti nella scrittura di pixel shader collegabili, d2d1effecthelpers.hlsli definisce un set di estensioni del linguaggio HLSL sotto forma di metodi helper e macro.
ms.assetid: 5D0BB99E-7C77-4D45-82E6-F038E4B752A4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 608ae4b47b96616f8818cd45b466c02a7b09b2171383fbe82ecbe055ed0915b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119569561"
---
# <a name="hlsl-helpers"></a>Helper HLSL

Per assistere gli autori di effetti nella scrittura di pixel shader collegabili, d2d1effecthelpers.hlsli definisce un set di estensioni del linguaggio HLSL sotto forma di metodi helper e macro.

Per aggiungere d2d1effecthelpers.hlsli al progetto, aggiungere \# un'istruzione include nel file HLSL. d2d1effecthelpers.hlsli si trova nella stessa posizione delle altre intestazioni Direct2D, ad esempio d2d1.h; È possibile farvi riferimento dalla pagina delle proprietà del file HLSL aggiungendo la macro $(WindowsSDK IncludePath) alla proprietà \_ Directory di inclusione aggiuntive. Si noti che l'istruzione include deve essere presente dopo la definizione di qualsiasi direttiva del preprocessore, ad esempio \# D2D \_ INPUT \_ COUNT.

``` syntax
#include <d2d1effecthelpers.hlsli>
```

Direct2D non supporta il collegamento di calcolo o vertex shader. Tuttavia, se l'effetto usa sia un vertex shader che pixel shader, l'output del pixel shader può comunque essere collegato.

## <a name="preprocessor-directives"></a>Direttive per il preprocessore

Le direttive del preprocessore sono necessarie per comunicare informazioni sull'effetto. Ciò include il numero di input e il tipo di campionamento di ogni input. I valori seguenti devono essere definiti nel codice dell'effetto shader sopra il punto di ingresso dello shader pertinente, se applicabile.

-   `D2D_INPUT_COUNT <N>` : dichiara il numero di input di trama per l'effetto. Se l'effetto ha un numero variabile di input, questo valore deve essere limitato in modo appropriato a ogni punto di ingresso dello shader. La definizione di questo valore è obbligatoria.
-   `D2D_INPUT<N>_SIMPLE` : dichiara l'eesimo input per usare il campionamento semplice. Se non è definito, per impostazione predefinita l'eesimo input è complesso. La definizione di questo valore è facoltativa.
-   `D2D_INPUT<N>_COMPLEX` : dichiara l'eesimo input per usare il campionamento complesso. Se non è definito, per impostazione predefinita l'eesimo input è complesso. La definizione di questo valore è facoltativa.
-   `D2D_REQUIRES_SCENE_POSITION`: indica che la funzione shader chiama i metodi helper che usano il valore della posizione della scena,ovvero la funzione helper [D2DGetScenePosition.](d2dgetsceneposition.md) Questo parametro deve essere incluso solo quando necessario, perché solo una funzione per ogni shader collegato può usare questo parametro. La definizione di questo valore è facoltativa.
-   `D2D_CUSTOM_ENTRY` : indica che la funzione pixel shader utilizza l'output di un vertex shader personalizzato e pertanto dichiara i relativi parametri di input. Tutti gli input di vertex shader personalizzati usano il campionamento complesso e non possono usare l'output di un'altra funzione shader, ovvero sono solo post-collegabili. La definizione di questo valore è facoltativa.

Esempio:

``` syntax
#define D2D_INPUT_COUNT 3
#define D2D_INPUT0_SIMPLE
#define D2D_INPUT1_SIMPLE
#define D2D_INPUT2_COMPLEX
#include <d2d1effecthelpers.hlsli>
          
```

## <a name="helper-functions"></a>Funzioni di supporto

Le funzioni helper vengono usate come sostituzione per alcune funzioni intrinseche HLSL native. In fase di compilazione, queste funzioni helper vengono ridefinite da Direct2D nella versione appropriata a seconda del tipo di destinazione di compilazione (shader completo o funzione di esportazione).

Le funzioni helper:

<dl>

[D2DGetInput](d2dgetinput.md)  
[D2DSampleInput](d2dsampleinput.md)  
[D2DSampleInputAtOffset](d2dsampleinputatoffset.md)  
[D2DSampleInputAtPosition](d2dsampleinputatposition.md)  
[D2DGetInputCoordinate](d2dgetinputcoordinate.md)  
[D2DGetScenePosition](d2dgetsceneposition.md)  
[VOCE D2D \_ \_ PS](d2d-ps-entry.md)  
</dl>

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Collegamento degli effetti shader](effect-shader-linking.md)
</dt> </dl>

 

 




