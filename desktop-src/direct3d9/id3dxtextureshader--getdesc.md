---
description: Ottiene una descrizione della tabella delle costanti.
ms.assetid: 91b537bb-5f7a-448b-a21f-c0ddf66d7238
title: 'Metodo ID3DXTextureShader:: getdesc (D3DX9Shader. h)'
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
ms.openlocfilehash: 97302b7e0f8c9f05e6229e20c2c9c158173ed944
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235044"
---
# <a name="id3dxtextureshadergetdesc-method"></a>Metodo ID3DXTextureShader:: getdesc

Ottiene una descrizione della tabella delle costanti.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetDesc(
  [in] D3DXCONSTANTTABLE_DESC *pDesc
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pDesc* \[ in\]
</dt> <dd>

Tipo: **[ **D3DXCONSTANTTABLE \_ desc**](d3dxconstanttable-desc.md)\***

Attributi della tabella delle costanti. Vedere [**D3DXCONSTANTTABLE \_ desc**](d3dxconstanttable-desc.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXTextureShader](id3dxtextureshader.md)
</dt> </dl>

 

 




