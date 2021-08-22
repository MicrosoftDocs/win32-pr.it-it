---
description: Ottiene il valore di un parametro arbitrario o di un'annotazione, inclusi tipi semplici, struct, matrici, stringhe, shader e trame. Questo metodo può essere usato al posto di quasi tutte le chiamate Getxxx in ID3DXBaseEffect.
ms.assetid: 41343922-99a7-486f-b4b0-1aa07f339664
title: Metodo ID3DXBaseEffect::GetValue (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetValue
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: f957ae3b59f10a086f2326e82478afb6b0ba7fd85bbf6b3f78df5746b7fcb56f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119494701"
---
# <a name="id3dxbaseeffectgetvalue-method"></a>Metodo ID3DXBaseEffect::GetValue

Ottiene il valore di un parametro arbitrario o di un'annotazione, inclusi tipi semplici, struct, matrici, stringhe, shader e trame. Questo metodo può essere usato al posto di quasi tutte le chiamate Getxxx in [**ID3DXBaseEffect.**](id3dxbaseeffect.md)

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetValue(
  [in]  D3DXHANDLE hParameter,
  [out] LPVOID     pData,
  [in]  UINT       Bytes
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hParameter* \[ Pollici\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Identificatore univoco. Vedere [Handle (Direct3D 9).](handles.md)

</dd> <dt>

*pData* \[ Cambio\]
</dt> <dd>

Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**

Restituisce un buffer contenente il valore.

</dd> <dt>

*Byte* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

\[in \] Numero di byte nel buffer. Passare D3DX DEFAULT se si sa che il buffer è sufficientemente grande da contenere l'intero parametro e si vuole ignorare \_ la convalida delle dimensioni.

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

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> <dt>

[**SetValue**](id3dxbaseeffect--setvalue.md)
</dt> </dl>

 

 
