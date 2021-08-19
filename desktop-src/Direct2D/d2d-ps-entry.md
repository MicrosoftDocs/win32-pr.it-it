---
title: D2D_PS_ENTRY funzione (D2d1effecthelpers.h)
description: Macro che definisce un pixel shader di ingresso con il nome di funzione specificato.
ms.assetid: 4C87369A-EF51-46BA-9CA4-386630A7F866
keywords:
- D2D_PS_ENTRY funzione Direct2D
topic_type:
- apiref
api_name:
- D2D_PS_ENTRY
api_location:
- d2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26369ef5be8c9dea81bf95e60c09ca0041d4275114c8892b85b6b5525f45504b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120087786"
---
# <a name="d2d_ps_entry-function"></a>Funzione D2D \_ PS \_ ENTRY

Macro che definisce un pixel shader di ingresso con il nome di funzione specificato.

## <a name="syntax"></a>Sintassi

``` syntax
void WINAPI D2D_PS_ENTRY(
  in string Entryname
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*Nome voce* \[ Pollici\]
</dt> <dd>

Nome pixel shader punto di ingresso.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

Usare questa macro invece di specificare la firma di input del punto di ingresso nel modo normale: tutti i parametri sono impliciti e aggiunti da Direct2D durante la compilazione a seconda del tipo di destinazione di compilazione (shader completo o funzione di esportazione).

``` syntax
#define D2D_INPUT_COUNT 1 
#define D2D_INPUT0_SIMPLE 
#include  d2d1effectauthor.hlsli  

D2D_PS_ENTRY(LinkingCompatiblePixelShader) 
{ 
    float4 input = D2DGetInput(0);  

    input.rgb *= input.a; 

    return input; 
} 
```

In questo breve esempio si noti che non viene dichiarato alcun parametro di funzione, che il numero di input e il tipo di ogni input vengono dichiarati prima della funzione di immissione, l'input viene recuperato chiamando [D2DGetInput](d2dgetinput.md)e che le direttive del preprocessore devono essere definite prima dell'inserimento del file helper.

Uno shader compatibile con il collegamento deve fornire sia una normale funzione a pixel shader che una funzione di esportazione shader. La macro D2D PS ENTRY consente di generare ognuno di questi elementi dallo stesso codice, se usato in combinazione con \_ lo script di compilazione dello \_ shader.

Quando si compila uno shader completo, le macro vengono espanse nel codice seguente, che ha una firma di input compatibile con gli effetti D2D.

``` syntax
Texture2D<float4> InputTexture0; 
SamplerState InputSampler0; 

float4 LinkingCompatiblePixelShader(
    float4 pos   : SV_POSITION,   
    float4 posScene : SCENE_POSITION,    
    float4 uv0  : TEXCOORD0 
    ) : SV_Target 
{ 
    float4 input = InputTexture0.Sample(InputSampler0, uv0.xy);  

    input.rgb *= input.a; 

    return input; 
} 
```

Quando si compila una versione della funzione di esportazione dello stesso codice, viene generato il codice seguente:

``` syntax
// Shader function version 
export float4 LinkingCompatiblePixelShader_Function( 
    float4 input0 : INPUT0 
    ) 
{ 
    input.rgb *= input.a; 

    return input; 
} 
```

Si noti che l'input della trama, normalmente recuperato tramite il campionamento di un oggetto Texture2D, è stato sostituito con un input di funzione input0.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D2d1effecthelpers.hlsli</dt> </dl> |
| DLL<br/>    | <dl> <dt>D2d1.dll</dt> </dl>                |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Collegamento degli effetti shader](effect-shader-linking.md)
</dt> <dt>

[Helper HLSL](hlsl-helpers.md)
</dt> </dl>

 

 





