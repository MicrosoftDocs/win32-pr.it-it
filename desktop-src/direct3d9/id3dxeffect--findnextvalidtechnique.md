---
description: Cerca la tecnica valida successiva, iniziando dalla tecnica dopo la tecnica specificata.
ms.assetid: 0d2f3f80-90fd-495d-acb8-075f50e9a974
title: 'Metodo ID3DXEffect:: FindNextValidTechnique (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.FindNextValidTechnique
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: adcaaa5194abeb17d110118de922811eb84af7fa
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104401971"
---
# <a name="id3dxeffectfindnextvalidtechnique-method"></a>Metodo ID3DXEffect:: FindNextValidTechnique

Cerca la tecnica valida successiva, iniziando dalla tecnica dopo la tecnica specificata.

## <a name="syntax"></a>Sintassi


```C++
HRESULT FindNextValidTechnique(
  [in]  D3DXHANDLE hTechnique,
  [out] D3DXHANDLE *pTechnique
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hTechnique* \[ in\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Identificatore univoco di una tecnica. Vedere [handle (Direct3D 9)](handles.md). Specificare **null** per questo parametro per trovare la prima tecnica valida.

</dd> <dt>

*pTechnique* \[ out\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)\***

Puntatore a un identificatore per la tecnica successiva. Se si tratta dell'ultima tecnica, viene restituito **null** . Vedere [handle (Direct3D 9)](handles.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK. Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> <dt>

[**D3DXTECHNIQUE \_ DESC**](d3dxtechnique-desc.md)
</dt> <dt>

[**ID3DXEffect::ValidateTechnique**](id3dxeffect--validatetechnique.md)
</dt> </dl>

 

 




