---
description: Ottiene il numero massimo di influenze del viso in una mesh triangolare con l'oggetto index buffer.
ms.assetid: 72dc2440-87df-461e-80d0-9ad9b1e4d8ee
title: Metodo ID3DXSkinInfo::GetMaxFaceInfluences (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.GetMaxFaceInfluences
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 84e949c0b6140b4be0f55c47c0f24b3e3b2843009c5c0cd039c76caefa0667a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118800670"
---
# <a name="id3dxskininfogetmaxfaceinfluences-method"></a>Metodo ID3DXSkinInfo::GetMaxFaceInfluences

Ottiene il numero massimo di influenze del viso in una mesh triangolare con l'oggetto index buffer.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetMaxFaceInfluences(
  [in] LPDIRECT3DINDEXBUFFER9 pIB,
  [in] DWORD                  NumFaces,
  [in] DWORD                  *maxFaceInfluences
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pIB* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DINDEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9)**

Puntatore all'index buffer che contiene i dati dell'indice mesh.

</dd> <dt>

*NumFaces* \[ Pollici\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Numero di visi nella mesh.

</dd> <dt>

*maxFaceInfluences* \[ Pollici\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Puntatore al numero massimo di influenze del viso.

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

 

 
