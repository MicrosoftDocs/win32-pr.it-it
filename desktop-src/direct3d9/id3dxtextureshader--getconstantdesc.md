---
description: Ottiene un puntatore alla matrice di costanti nella tabella delle costanti.
ms.assetid: 2476344b-8433-46bb-9242-dff84e3168e7
title: 'Metodo ID3DXTextureShader:: GetConstantDesc (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.GetConstantDesc
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 22898880e5cef5669defae89cda4f7d9818f9f1f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323358"
---
# <a name="id3dxtextureshadergetconstantdesc-method"></a>Metodo ID3DXTextureShader:: GetConstantDesc

Ottiene un puntatore alla matrice di costanti nella tabella delle costanti.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetConstantDesc(
  [in]      D3DXHANDLE        hConstant,
  [in, out] D3DXCONSTANT_DESC *pDesc,
  [in, out] UINT              *pCount
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hConstant* \[ in\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Identificatore univoco di una costante. Vedere [D3DXHANDLE](d3dxfx.md).

</dd> <dt>

*pDesc* \[ in uscita\]
</dt> <dd>

Tipo: **[ **D3DXCONSTANT \_ desc**](d3dxconstant-desc.md)\***

Restituisce un puntatore a una matrice di descrizioni. Vedere [**D3DXCONSTANT \_ desc**](d3dxconstant-desc.md).

</dd> <dt>

*pcount* \[ in uscita\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)\***

L'input specificato deve corrispondere alla dimensione massima della matrice. L'output è il numero di elementi che vengono compilati nella matrice quando la funzione restituisce.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Commenti

I sampler possono essere visualizzati più di una volta in una tabella costante, pertanto questo metodo può restituire una matrice di descrizioni ognuna con un indice di registro diverso.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXTextureShader](id3dxtextureshader.md)
</dt> <dt>

[**ID3DXTextureShader:: getdesc**](id3dxtextureshader--getdesc.md)
</dt> </dl>

 

 
