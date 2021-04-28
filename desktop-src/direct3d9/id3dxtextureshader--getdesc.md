---
description: 'Metodo ID3DXTextureShader::GetDesc: ottiene una descrizione della tabella costante.'
ms.assetid: 91b537bb-5f7a-448b-a21f-c0ddf66d7238
title: Metodo ID3DXTextureShader::GetDesc (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.GetDesc
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6ea94f0e22d838f09dae9b423f85aa1d55d2365b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117639"
---
# <a name="id3dxtextureshadergetdesc-method"></a>Metodo ID3DXTextureShader::GetDesc

Ottiene una descrizione della tabella delle costanti.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetDesc(
  [in] D3DXCONSTANTTABLE_DESC *pDesc
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pDesc* \[ Pollici\]
</dt> <dd>

Tipo: **[ **D3DXCONSTANTTABLE \_ DESC**](d3dxconstanttable-desc.md)\***

Attributi della tabella delle costanti. Vedere [**D3DXCONSTANTTABLE \_ DESC**](d3dxconstanttable-desc.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXTextureShader](id3dxtextureshader.md)
</dt> </dl>

 

 




