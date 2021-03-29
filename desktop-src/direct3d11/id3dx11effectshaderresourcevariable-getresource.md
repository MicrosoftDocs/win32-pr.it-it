---
title: Metodo GetResource ID3DX11EffectShaderResourceVariable (D3dx11effect. h)
description: Ottenere una risorsa shader.
ms.assetid: 7c56aba0-ce60-4b50-9c1a-802bf1d73c6b
keywords:
- Metodo GetResource Direct3D 11
- Metodo GetResource Direct3D 11, interfaccia ID3DX11EffectShaderResourceVariable
- Interfaccia ID3DX11EffectShaderResourceVariable Direct3D 11, metodo GetResource
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
ms.openlocfilehash: cea841ae63646958603396d5b65305c242961942
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104234949"
---
# <a name="id3dx11effectshaderresourcevariablegetresource-method"></a>Metodo ID3DX11EffectShaderResourceVariable:: GetResource

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

Indirizzo di un puntatore a un'interfaccia shader-Resource-View. Vedere [**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Restituisce uno dei seguenti [codici restituiti Direct3D 11](d3d11-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Commenti

> [!Note]  
> DirectX SDK non fornisce binari compilati per gli effetti. È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects. Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Libreria<br/> | <dl> <dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DX11EffectShaderResourceVariable](id3dx11effectshaderresourcevariable.md)
</dt> </dl>

 

 





