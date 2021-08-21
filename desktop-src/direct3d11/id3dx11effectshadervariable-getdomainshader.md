---
title: Metodo GetDomainShader ID3DX11EffectShaderVariable (D3dx11effect.h)
description: Ottenere uno shader di dominio.
ms.assetid: fd95a4f0-7df3-4098-843f-0a1e22209603
keywords:
- Metodo GetDomainShader Direct3D 11
- Metodo GetDomainShader Direct3D 11, interfaccia ID3DX11EffectShaderVariable
- ID3DX11EffectShaderVariable interface Direct3D 11 , Metodo GetDomainShader
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
ms.openlocfilehash: 0e66bb99f170e6b638587d7da5a8d3cc57a34d3cab6bb04968b049d39dcb09c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118533297"
---
# <a name="id3dx11effectshadervariablegetdomainshader-method"></a>Metodo ID3DX11EffectShaderVariable::GetDomainShader

Ottenere uno shader di dominio.

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

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Indice dello shader di dominio.

</dd> <dt>

*Ppp* 
</dt> <dd>

Tipo: **[ **ID3D11DomainShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11domainshader)\*\***

Puntatore a [**un puntatore ID3D11DomainShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11domainshader) che verrà impostato sullo shader di dominio al ritorno.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Restituisce uno dei codici [restituiti Direct3D 11 seguenti.](d3d11-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Commenti

> [!Note]  
> DirectX SDK non fornisce alcun file binario compilato per gli effetti. È necessario usare l'origine Effects 11 per compilare l'applicazione effects-type. Per altre informazioni sull'uso dell'origine Effetti 11, vedere Differenze [tra effetti 10 ed effetti 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Libreria<br/> | <dl> <dt>N/D (una libreria effects 11 è disponibile online come origine condivisa).</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DX11EffectShaderVariable](id3dx11effectshadervariable.md)
</dt> </dl>

 

