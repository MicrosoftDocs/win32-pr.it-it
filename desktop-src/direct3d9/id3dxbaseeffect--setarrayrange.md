---
description: Impostare l'intervallo di una matrice da passare al dispositivo.
ms.assetid: 43f1c258-770c-4756-9033-e5667b379fe6
title: Metodo ID3DXBaseEffect::SetArrayRange (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetArrayRange
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 1cf4f51bfca29f1aa46238197818bb10bc4d0fe811218e5cedc59c24deb2446f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987631"
---
# <a name="id3dxbaseeffectsetarrayrange-method"></a>Metodo ID3DXBaseEffect::SetArrayRange

Impostare l'intervallo di una matrice da passare al dispositivo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetArrayRange(
  [in] D3DXHANDLE hParameter,
  [in] UINT       Start,
  [in] UINT       Stop
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hParameter* \[ Pollici\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Identificatore univoco. Vedere [Handle (Direct3D 9)](handles.md).

</dd> <dt>

*Avvio* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Indice iniziale.

</dd> <dt>

*Arresta* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Arrestare l'indice.

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
</dt> </dl>

 

 
