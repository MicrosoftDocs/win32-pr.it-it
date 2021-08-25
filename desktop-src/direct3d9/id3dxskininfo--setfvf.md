---
description: Imposta il tipo FVF (Flexible Vertex Format).
ms.assetid: e581dcd4-7e17-4c36-aac9-c2942924cf51
title: Metodo ID3DXSkinInfo::SetFVF (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.SetFVF
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: fe57d1d2c879d1242cd9358e1f74c346e68586c8ea84c1be14b1e2994b899908
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119985211"
---
# <a name="id3dxskininfosetfvf-method"></a>Metodo ID3DXSkinInfo::SetFVF

Imposta il tipo FVF (Flexible Vertex Format).

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetFVF(
  [in] DWORD FVF
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*FVF* \[ Pollici\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Formato dei vertici flessibile. Vedere [D3DFVF](d3dfvf.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK. Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXSkinInfo](id3dxskininfo.md)
</dt> </dl>

 

 
