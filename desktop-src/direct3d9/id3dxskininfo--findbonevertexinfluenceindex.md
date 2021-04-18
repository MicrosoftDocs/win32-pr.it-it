---
description: Recupera l'indice dell'influenza ossea che interessa un singolo vertice.
ms.assetid: vs|directx_sdk|~\id3dxskininfo__findbonevertexinfluenceindex.htm
title: 'Metodo ID3DXSkinInfo:: FindBoneVertexInfluenceIndex (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.FindBoneVertexInfluenceIndex
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 05a86e98e5001092700fdec12f2a7afc33ddf082
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322067"
---
# <a name="id3dxskininfofindbonevertexinfluenceindex-method"></a>Metodo ID3DXSkinInfo:: FindBoneVertexInfluenceIndex

Recupera l'indice dell'influenza ossea che interessa un singolo vertice.

## <a name="syntax"></a>Sintassi


```C++
HRESULT FindBoneVertexInfluenceIndex(
  [in]      DWORD boneNum,
  [in]      DWORD vertexNum,
  [in, out] DWORD *pInfluenceIndex
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*boneNum* \[ in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Indice dell'osso. Deve essere compreso tra 0 e il numero di ossa.

</dd> <dt>

*vertexNum* \[ in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Indice del vertice per il quale è necessario trovare l'influenza dell'osso. Deve essere compreso tra 0 e il numero di vertici nella rete.

</dd> <dt>

*pInfluenceIndex* \[ in uscita\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Puntatore all'indice dell'influenza dell'osso che interessa vertexNum.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è \_ OK. Se l'osso specificato non influenza il vertice dato, \_ viene restituito S false. Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXSkinInfo](id3dxskininfo.md)
</dt> <dt>

[**ID3DXSkinInfo::GetBoneVertexInfluence**](id3dxskininfo--getbonevertexinfluence.md)
</dt> <dt>

[**ID3DXSkinInfo::SetBoneVertexInfluence**](id3dxskininfo--setbonevertexinfluence.md)
</dt> <dt>

[**ID3DXSkinInfo::GetBoneInfluence**](id3dxskininfo--getboneinfluence.md)
</dt> </dl>

 

 
