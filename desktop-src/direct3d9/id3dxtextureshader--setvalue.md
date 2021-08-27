---
description: Imposta la tabella delle costanti con i dati nel buffer.
ms.assetid: 55cf5456-8f23-405d-9329-8ff737c5c139
title: Metodo ID3DXTextureShader::SetValue (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetValue
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9ba652d4fd295103409c073287264d3a01b6352c465532719f01e427ad4dedcd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120095641"
---
# <a name="id3dxtextureshadersetvalue-method"></a>Metodo ID3DXTextureShader::SetValue

Imposta la tabella delle costanti con i dati nel buffer.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetValue(
  [in] D3DXHANDLE hConstant,
  [in] LPCVOID    pData,
  [in] UINT       Bytes
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hConstant* \[ Pollici\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Identificatore univoco di una costante. Vedere [D3DXHANDLE](d3dxfx.md).

</dd> <dt>

*pData* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**

Puntatore a un buffer contenente i dati costanti.

</dd> <dt>

*Byte* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Dimensioni del buffer, in byte.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK. Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXTextureShader](id3dxtextureshader.md)
</dt> </dl>

 

 
