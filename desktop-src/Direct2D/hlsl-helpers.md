---
title: Helper HLSL
description: Per assistere gli autori degli effetti nella scrittura di pixel shader collegabili, d2d1effecthelpers. hlsli definisce un set di estensioni del linguaggio HLSL sotto forma di metodi di supporto e macro.
ms.assetid: 5D0BB99E-7C77-4D45-82E6-F038E4B752A4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec8f43447c16d93ef9e1839ac319c761b975222a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955236"
---
# <a name="hlsl-helpers"></a>Helper HLSL

Per assistere gli autori degli effetti nella scrittura di pixel shader collegabili, d2d1effecthelpers. hlsli definisce un set di estensioni del linguaggio HLSL sotto forma di metodi di supporto e macro.

Per aggiungere d2d1effecthelpers. hlsli al progetto, aggiungere un' \# istruzione include nel file HLSL. d2d1effecthelpers. hlsli si trova nella stessa posizione di altre intestazioni Direct2D, ad esempio d2d1. h; è possibile farvi riferimento dalla pagina delle proprietà del file HLSL aggiungendo la macro $ (WindowsSDK \_ IncludePath) alla proprietà directory di inclusione aggiuntive. Si noti che l' \# istruzione include deve provenire dopo la definizione di tutte le direttive per il preprocessore, come il \_ numero di input D2D \_ .

``` syntax
#include <d2d1effecthelpers.hlsli>
```

Direct2D non supporta il collegamento di COMPUTE o vertex shader. Tuttavia, se l'effetto USA sia un vertex shader che un pixel shader, l'output del pixel shader può ancora essere collegato.

## <a name="preprocessor-directives"></a>Direttive per il preprocessore

Le direttive per il preprocessore sono necessarie per comunicare informazioni sull'effetto. Sono inclusi il numero di input e il tipo di campionamento di ogni input. Quando applicabile, è necessario definire i valori seguenti nel codice dello shader di effetto sopra il punto di ingresso dello shader pertinente.

-   `D2D_INPUT_COUNT <N>` : Dichiara il numero di input di trama all'effetto. Se l'effetto ha un numero variabile di input, questo valore deve essere definito in modo appropriato per ogni punto di ingresso dello shader. La definizione di questo valore è obbligatoria.
-   `D2D_INPUT<N>_SIMPLE` : Dichiara l'ennesimo input per usare il campionamento semplice. Se non è definito, l'ennesimo input predefinito è complesso. La definizione di questo valore è facoltativa.
-   `D2D_INPUT<N>_COMPLEX` : Dichiara l'ennesimo input per usare il campionamento complesso. Se non è definito, l'ennesimo input predefinito è complesso. La definizione di questo valore è facoltativa.
-   `D2D_REQUIRES_SCENE_POSITION` : Indica che la funzione shader chiama metodi helper che usano il valore della posizione della scena, ovvero la funzione di supporto [D2DGetScenePosition](d2dgetsceneposition.md) . Questo parametro deve essere incluso solo quando necessario, perché solo una funzione per shader collegato può utilizzare questo parametro. La definizione di questo valore è facoltativa.
-   `D2D_CUSTOM_ENTRY` : Indica che la funzione pixel shader utilizza l'output di un vertex shader personalizzato e quindi dichiara i parametri di input. Tutti gli input di vertex shader personalizzati usano il campionamento complesso e non possono utilizzare l'output di un'altra funzione shader, ovvero sono solo post-Linkable. La definizione di questo valore è facoltativa.

Ad esempio:

``` syntax
#define D2D_INPUT_COUNT 3
#define D2D_INPUT0_SIMPLE
#define D2D_INPUT1_SIMPLE
#define D2D_INPUT2_COMPLEX
#include <d2d1effecthelpers.hlsli>
          
```

## <a name="helper-functions"></a>Funzioni di supporto

Le funzioni di supporto vengono usate come sostituzione per alcune funzioni intrinseche HLSL native. In fase di compilazione, queste funzioni di supporto vengono ridefinite da Direct2D nella versione appropriata a seconda del tipo di destinazione della compilazione (funzione shader completa o funzione di esportazione).

Funzioni helper:

<dl>

[D2DGetInput](d2dgetinput.md)  
[D2DSampleInput](d2dsampleinput.md)  
[D2DSampleInputAtOffset](d2dsampleinputatoffset.md)  
[D2DSampleInputAtPosition](d2dsampleinputatposition.md)  
[D2DGetInputCoordinate](d2dgetinputcoordinate.md)  
[D2DGetScenePosition](d2dgetsceneposition.md)  
[\_Voce D2D PS \_](d2d-ps-entry.md)  
</dl>

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Collegamento Effect shader](effect-shader-linking.md)
</dt> </dl>

 

 




