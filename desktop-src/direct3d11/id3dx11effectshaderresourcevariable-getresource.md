---
title: Metodo GetResource ID3DX11EffectShaderResourceVariable (D3dx11effect.h)
description: Ottenere una risorsa shader.
ms.assetid: 7c56aba0-ce60-4b50-9c1a-802bf1d73c6b
keywords:
- Metodo GetResource Direct3D 11
- Metodo GetResource Interfaccia Direct3D 11, ID3DX11EffectShaderResourceVariable
- ID3DX11EffectShaderResourceVariable interface Direct3D 11 , Metodo GetResource
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderResourceVariable.GetResource
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a11cf0878078ac3152f23a088290f4dd1d046f516dae50e77d22cb7e5ea70a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118533573"
---
# <a name="id3dx11effectshaderresourcevariablegetresource-method"></a>Metodo ID3DX11EffectShaderResourceVariable::GetResource

Ottenere una risorsa shader.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetResource(
   ID3D11ShaderResourceView **ppResource
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppResource* 
</dt> <dd>

Tipo: **[ **ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)\*\***

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

 

 





