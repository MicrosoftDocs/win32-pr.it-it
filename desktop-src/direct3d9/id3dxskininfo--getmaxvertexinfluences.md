---
description: Ottiene il numero massimo di fattori di influenza per qualsiasi vertice nella mesh.
ms.assetid: 012168e8-30e5-4571-b793-647ab23df068
title: Metodo ID3DXSkinInfo::GetMaxVertexInfluences (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.GetMaxVertexInfluences
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5cd33155ba5b306fc24e345f535a083c78031da243b291f2c36c5894561e270d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120095711"
---
# <a name="id3dxskininfogetmaxvertexinfluences-method"></a>Metodo ID3DXSkinInfo::GetMaxVertexInfluences

Ottiene il numero massimo di fattori di influenza per qualsiasi vertice nella mesh.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetMaxVertexInfluences(
  [in] DWORD *maxVertexInfluences
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*maxVertexInfluences* \[ Pollici\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Puntatore all'influenza massima del vertice.

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

 

 
