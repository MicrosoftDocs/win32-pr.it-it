---
title: Metodo ID3DX11EffectVariable AsShader (D3dx11effect.h)
description: Ottenere una variabile shader.
ms.assetid: 660ba087-5320-44f7-946f-e500101fc6bb
keywords:
- Metodo AsShader Direct3D 11
- Metodo AsShader Direct3D 11, interfaccia ID3DX11EffectVariable
- ID3DX11EffectVariable interface Direct3D 11 , AsShader method
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.AsShader
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 050ed69e9a4f498cb28062dcf493f88f4132e7578b436e3c0f54420d57264fd4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119376481"
---
# <a name="id3dx11effectvariableasshader-method"></a>Metodo ID3DX11EffectVariable::AsShader

Ottenere una variabile shader.

## <a name="syntax"></a>Sintassi


```C++
ID3DX11EffectShaderVariable* AsShader();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Tipo: **[ **ID3DX11EffectShaderVariable**](id3dx11effectshadervariable.md)\***

Puntatore a una variabile shader. Vedere [**ID3DX11EffectShaderVariable.**](id3dx11effectshadervariable.md)

## <a name="remarks"></a>Commenti

AsShader restituisce una versione della variabile dell'effetto specializzata in una variabile shader. Analogamente a un cast, questa specializzazione restituirà un oggetto non valido se la variabile dell'effetto non contiene dati shader.

Le applicazioni possono testare la validità dell'oggetto restituito chiamando [**IsValid.**](id3dx11effectvariable-isvalid.md)

> [!Note]  
> DirectX SDK non fornisce file binari compilati per gli effetti. È necessario usare l'origine Effects 11 per compilare l'applicazione del tipo di effetti. Per altre informazioni sull'uso dell'origine effetti 11, vedere Differenze tra gli [effetti 10 e gli effetti 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Libreria<br/> | <dl> <dt>N/D (una libreria di Effetti 11 è disponibile online come origine condivisa).</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DX11EffectVariable](id3dx11effectvariable.md)
</dt> </dl>

 

 





