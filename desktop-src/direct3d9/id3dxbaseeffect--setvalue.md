---
description: Impostare il valore di un parametro o di un'annotazione arbitraria, inclusi tipi semplici, struct, matrici, stringhe, shader e trame.
ms.assetid: ab71f1a1-3e10-4883-99b4-607e0b5751c2
title: Metodo ID3DXBaseEffect::SetValue (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetValue
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 2bb619c9d0ef469b36f96d1e35ee70719ede8f6eee494cc950f6fabadbf86304
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119748971"
---
# <a name="id3dxbaseeffectsetvalue-method"></a>Metodo ID3DXBaseEffect::SetValue

Impostare il valore di un parametro o di un'annotazione arbitraria, inclusi tipi semplici, struct, matrici, stringhe, shader e trame.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetValue(
  [in] D3DXHANDLE hParameter,
  [in] LPCVOID    pData,
  [in] UINT       Bytes
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hParameter* \[ Pollici\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Identificatore univoco. Vedere [Handle (Direct3D 9).](handles.md)

</dd> <dt>

*pData* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**

Puntatore a un buffer contenente dati.

</dd> <dt>

*Byte* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

\[in \] Numero di byte nel buffer. Passare D3DX DEFAULT se si sa che il buffer è sufficientemente grande da contenere l'intero parametro e si vuole ignorare \_ la convalida delle dimensioni.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK. Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Commenti

Questo metodo può essere usato al posto di quasi tutte le chiamate API del set di effetti.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> <dt>

[**Getvalue**](id3dxbaseeffect--getvalue.md)
</dt> </dl>

 

 
