---
title: Metodo ID3DX11EffectVariable AsShaderResource (D3dx11effect.h)
description: Ottenere una variabile di risorsa shader.
ms.assetid: 02db94eb-980a-4677-af89-3006aef6faca
keywords:
- Metodo AsShaderResource Direct3D 11
- Metodo AsShaderResource Direct3D 11, interfaccia ID3DX11EffectVariable
- ID3DX11EffectVariable interface Direct3D 11 , AsShaderResource method
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.AsShaderResource
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ef87874c005f12d3e49962ee438f516df3631c12ff17fc4db27e0a82fe1a654
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118531384"
---
# <a name="id3dx11effectvariableasshaderresource-method"></a>Metodo ID3DX11EffectVariable::AsShaderResource

Ottenere una variabile di risorsa shader.

## <a name="syntax"></a>Sintassi


```C++
ID3DX11EffectShaderResourceVariable* AsShaderResource();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Tipo: **[ **ID3DX11EffectShaderResourceVariable**](id3dx11effectshaderresourcevariable.md)\***

Puntatore a una variabile di risorsa shader. Vedere [**ID3DX11EffectShaderResourceVariable.**](id3dx11effectshaderresourcevariable.md)

## <a name="remarks"></a>Commenti

AsShaderResource restituisce una versione della variabile dell'effetto specializzata in una variabile shader-risorsa. Analogamente a un cast, questa specializzazione restituirà un oggetto non valido se la variabile dell'effetto non contiene dati di risorse shader.

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

 

 





