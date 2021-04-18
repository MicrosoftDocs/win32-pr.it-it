---
description: Convalidare una tecnica.
ms.assetid: d69eaafa-da4d-4599-86fb-83d72e1664cc
title: 'Metodo ID3DXEffect:: ValidateTechnique (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.ValidateTechnique
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b48ffa8707a3f78e76555d57225c11f89160fdd7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322351"
---
# <a name="id3dxeffectvalidatetechnique-method"></a>Metodo ID3DXEffect:: ValidateTechnique

Convalidare una tecnica.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ValidateTechnique(
  [in] D3DXHANDLE hTechnique
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hTechnique* \[ in\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Identificatore univoco. Vedere [handle (Direct3D 9)](handles.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DERR \_ CONFLICTINGRENDERSTATE, D3DERR CONFLICTINGTEXTUREFILTER, D3DERR DEVICELOST, D3DERR DRIVERINTERNALERROR, D3DERR TOOMANYOPERATIONS, D3DERR UNSUPPORTEDALPHAARG, D3DERR UNSUPPORTEDALPHAOPERATION, D3DERR UNSUPPORTEDCOLORARG, D3DERR UNSUPPORTEDCOLOROPERATION, D3DERR UNSUPPORTEDFACTORVALUE, \_ \_ D3DERR UNSUPPORTEDTEXTUREFILTER \_ \_ \_ \_ \_ \_ \_ \_ e D3DERR WRONGTEXTUREFORMAT \_ .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> <dt>

[**ID3DXEffect:: setechnique**](id3dxeffect--settechnique.md)
</dt> </dl>

 

 




