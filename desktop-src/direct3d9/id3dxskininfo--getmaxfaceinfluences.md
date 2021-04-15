---
description: Ottiene le influenze massime della faccia in una mesh triangolare con il buffer di indice specificato.
ms.assetid: 72dc2440-87df-461e-80d0-9ad9b1e4d8ee
title: 'Metodo ID3DXSkinInfo:: GetMaxFaceInfluences (D3DX9Mesh. h)'
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
ms.openlocfilehash: 11724c50d5224f0bcb2c9ced25523b869f3e347f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104401922"
---
# <a name="id3dxskininfogetmaxfaceinfluences-method"></a>Metodo ID3DXSkinInfo:: GetMaxFaceInfluences

Ottiene le influenze massime della faccia in una mesh triangolare con il buffer di indice specificato.

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

*pIB* \[ in\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DINDEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9)**

Puntatore al buffer di indice contenente i dati dell'indice mesh.

</dd> <dt>

*NumFaces* \[ in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Numero di visi nella rete.

</dd> <dt>

*maxFaceInfluences* \[ in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Puntatore alle influenze massime della faccia.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK. Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXSkinInfo](id3dxskininfo.md)
</dt> </dl>

 

 
