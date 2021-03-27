---
title: Metodo ID3DX11EffectShaderVariable GetDomainShader (D3dx11effect. h)
description: Ottenere un Domain shader.
ms.assetid: fd95a4f0-7df3-4098-843f-0a1e22209603
keywords:
- Metodo GetDomainShader Direct3D 11
- Metodo GetDomainShader Direct3D 11, interfaccia ID3DX11EffectShaderVariable
- Interfaccia ID3DX11EffectShaderVariable Direct3D 11, metodo GetDomainShader
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderVariable.GetDomainShader
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b7f097fb950b60aaa9c7fa2d5b763b393d5e275
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235223"
---
# <a name="id3dx11effectshadervariablegetdomainshader-method"></a>Metodo ID3DX11EffectShaderVariable:: GetDomainShader

Ottenere un Domain shader.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetDomainShader(
   UINT               ShaderIndex,
   ID3D11DomainShader **ppPS
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ShaderIndex* 
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Indice dello shader del dominio.

</dd> <dt>

*PPP* 
</dt> <dd>

Tipo: **[ **ID3D11DomainShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11domainshader)\*\***

Puntatore a un puntatore [**ID3D11DomainShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11domainshader) che verrà impostato sullo shader del dominio al ritorno.

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

[ID3DX11EffectShaderVariable](id3dx11effectshadervariable.md)
</dt> </dl>

 

