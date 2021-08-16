---
title: Metodo SetResource ID3DX11EffectShaderResourceVariable (D3dx11effect.h)
description: Impostare una risorsa shader.
ms.assetid: f85c33ff-dc00-4421-939c-74f9317faadc
keywords:
- Metodo SetResource Direct3D 11
- Metodo SetResource Interfaccia Direct3D 11, ID3DX11EffectShaderResourceVariable
- ID3DX11EffectShaderResourceVariable interface Direct3D 11 , SetResource method
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderResourceVariable.SetResource
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf0db2db1886298633ba70fa9af6ce1d475b5c511487b35e65d20373f8282f3c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118533439"
---
# <a name="id3dx11effectshaderresourcevariablesetresource-method"></a>Metodo ID3DX11EffectShaderResourceVariable::SetResource

Impostare una risorsa shader.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetResource(
   ID3D11ShaderResourceView *pResource
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pResource* 
</dt> <dd>

Tipo: **[ **ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)\***

Indirizzo di un puntatore a un'interfaccia shader-resource-view. Vedere [**ID3D11ShaderResourceView.**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Restituisce uno dei seguenti [codici restituiti Direct3D 11.](d3d11-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Commenti

> [!Note]  
> DirectX SDK non fornisce file binari compilati per gli effetti. È necessario usare l'origine Effects 11 per compilare l'applicazione del tipo di effetti. Per altre informazioni sull'uso dell'origine effetti 11, vedere Differenze tra gli [effetti 10 e gli effetti 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Libreria<br/> | <dl> <dt>N/D (una libreria di Effetti 11 è disponibile online come origine condivisa).</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DX11EffectShaderResourceVariable](id3dx11effectshaderresourcevariable.md)
</dt> </dl>

 

 





