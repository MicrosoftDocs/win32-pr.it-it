---
description: Ottenere il valore di un parametro o di un'annotazione arbitraria, inclusi tipi semplici, struct, matrici, stringhe, shader e trame. Questo metodo può essere utilizzato al posto di quasi tutte le chiamate GetXXX in ID3DXBaseEffect.
ms.assetid: 41343922-99a7-486f-b4b0-1aa07f339664
title: 'Metodo ID3DXBaseEffect:: GetValue (D3DX9Shader. h)'
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
ms.openlocfilehash: 166635b22875692da0396f1c7c2145f13ca08df3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322087"
---
# <a name="id3dxbaseeffectgetvalue-method"></a>Metodo ID3DXBaseEffect:: GetValue

Ottenere il valore di un parametro o di un'annotazione arbitraria, inclusi tipi semplici, struct, matrici, stringhe, shader e trame. Questo metodo può essere utilizzato al posto di quasi tutte le chiamate GetXXX in [**ID3DXBaseEffect**](id3dxbaseeffect.md).

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

*hParameter* \[ in\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Identificatore univoco. Vedere [handle (Direct3D 9)](handles.md).

</dd> <dt>

*pData* \[ out\]
</dt> <dd>

Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**

Restituisce un buffer che contiene il valore.

</dd> <dt>

*Byte* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

\[\]numero di byte nel buffer. Passare \_ il valore predefinito D3DX se si è certi che il buffer è sufficientemente grande da contenere l'intero parametro e si vuole ignorare la convalida delle dimensioni.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK. Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> <dt>

[**SetValue**](id3dxbaseeffect--setvalue.md)
</dt> </dl>

 

 
