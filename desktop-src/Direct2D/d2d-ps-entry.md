---
title: Funzione D2D_PS_ENTRY (D2d1effecthelpers. h)
description: Una macro che definisce un punto di ingresso di pixel shader con il nome di funzione specificato.
ms.assetid: 4C87369A-EF51-46BA-9CA4-386630A7F866
keywords:
- Direct2D funzione D2D_PS_ENTRY
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
ms.openlocfilehash: 7525416eed7700709d02d2ec17823cd57a8c12ba
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324434"
---
# <a name="d2d_ps_entry-function"></a>\_Funzione di \_ immissione D2D PS

Una macro che definisce un punto di ingresso di pixel shader con il nome di funzione specificato.

## <a name="syntax"></a>Sintassi

``` syntax
void WINAPI D2D_PS_ENTRY(
  in string Entryname
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*Entryname* \[ in\]
</dt> <dd>

Nome del punto di ingresso del pixel shader.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

Usare questa macro invece di specificare la firma di input del punto di ingresso in modo normale: tutti i parametri sono impliciti e vengono aggiunti da Direct2D durante la compilazione a seconda del tipo di destinazione della compilazione (funzione shader completa o esportazione).

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

In questo breve esempio si noti che non vengono dichiarati parametri di funzione, che il numero di input e il tipo di ogni input sono dichiarati prima della funzione entry, che l'input viene recuperato chiamando [D2DGetInput](d2dgetinput.md)e che le direttive per il preprocessore devono essere definite prima che il file helper venga incluso.

Uno shader compatibile con il collegamento deve fornire sia un pixel shader a singolo passaggio normale che una funzione di esportazione dello shader. La \_ macro di immissione D2D PS consente la generazione di \_ ognuno di questi dallo stesso codice, se usato insieme allo script di compilazione dello shader.

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

Quando si compila una versione della funzione Export dello stesso codice, viene generato il codice seguente:

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

Si noti che l'input di trama, generalmente recuperato tramite il campionamento di un Texture2D, è stato sostituito con un input0 di input della funzione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D2d1effecthelpers. hlsli</dt> </dl> |
| DLL<br/>    | <dl> <dt>D2d1.dll</dt> </dl>                |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Collegamento Effect shader](effect-shader-linking.md)
</dt> <dt>

[Helper HLSL](hlsl-helpers.md)
</dt> </dl>

 

 





