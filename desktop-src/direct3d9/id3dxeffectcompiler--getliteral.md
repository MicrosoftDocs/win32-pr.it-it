---
description: Ottiene uno stato letterale di un parametro. Un parametro letterale ha un valore che non cambia durante la durata di un effetto.
ms.assetid: 417abbee-5193-462e-b0d1-b4928ad0a041
title: 'Metodo ID3DXEffectCompiler:: GetLiteral (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectCompiler.GetLiteral
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: c16e3798ab66a34e12812a3560572c45b9206b30
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322348"
---
# <a name="id3dxeffectcompilergetliteral-method"></a>Metodo ID3DXEffectCompiler:: GetLiteral

Ottiene uno stato letterale di un parametro. Un parametro letterale ha un valore che non cambia durante la durata di un effetto.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetLiteral(
  [in]  D3DXHANDLE hParameter,
  [out] BOOL       *pLiteral
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hParameter* \[ in\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Identificatore univoco per un parametro. Vedere [handle (Direct3D 9)](handles.md).

</dd> <dt>

*pLiteral* \[ out\]
</dt> <dd>

Tipo: **[ **bool**](../winprog/windows-data-types.md)\***

Restituisce true se il parametro è un valore letterale e false in caso contrario.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK. Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Commenti

Questo metodo cambia solo se il parametro è un valore letterale o meno. Per modificare il valore di un parametro, usare un metodo come [**ID3DXBaseEffect::**](id3dxbaseeffect--setbool.md) SetValue o [**ID3DXBaseEffect:: SetValue**](id3dxbaseeffect--setvalue.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXEffectCompiler](id3dxeffectcompiler.md)
</dt> <dt>

[Utilizzi e valori letterali (Direct3D 9)](usages-and-literals.md)
</dt> <dt>

[**ID3DXEffectCompiler:: seliteral**](id3dxeffectcompiler--setliteral.md)
</dt> </dl>

 

 
