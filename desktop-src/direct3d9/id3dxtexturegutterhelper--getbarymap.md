---
description: Recupera le coordinate barycentric del texel.
ms.assetid: f380a37f-b9c1-4433-b1d6-e9feeca79b30
title: Metodo ID3DXTextureGutterHelper::GetBaryMap (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.GetBaryMap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4183bf9bfa5065595073b8534e978367c3ec16bf76245d639da81292641afa81
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117729200"
---
# <a name="id3dxtexturegutterhelpergetbarymap-method"></a>Metodo ID3DXTextureGutterHelper::GetBaryMap

Recupera le coordinate barycentric del texel.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetBaryMap(
  [in, out] D3DXVECTOR2 *pBaryData
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pBaryData* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***

Puntatore a [**una struttura D3DXVECTOR2**](d3dxvector2.md) che contiene le prime due coordinate barycentriche di ogni texel.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è S \_ OK. Se il metodo ha esito negativo, verrà restituito il valore seguente. D3DERR \_ INVALIDCALL

## <a name="remarks"></a>Commenti

La terza coordinata barycentric è data da:


```
    1 - ( pBaryData.x + pBaryData.y )
```



Le coordinate barycentriche vengono sempre specificate rispetto al triangolo restituito da [**ID3DXTextureGutterHelper::GetFaceMap**](id3dxtexturegutterhelper--getfacemap.md).

Le coordinate barycentriche restituite da questo metodo sono valide solo per texel validi (non di classe 0). [**ID3DXTextureGutterHelper::GetGutterMap**](id3dxtexturegutterhelper--getguttermap.md) restituirà valori diversi da zero per i texel validi.

[**I texel di classe 2 vengono**](id3dxtexturegutterhelper.md) mappati al punto più vicino sul triangolo nello spazio texel.

L'applicazione deve allocare e gestire pBaryData.

Le coordinate barycentriche definiscono un punto all'interno di un triangolo in termini di vertici del triangolo. Per una descrizione più approfondita delle coordinate barycentric, vedere Descrizione delle [coordinate barycentriche di Mathworld.](https://mathworld.wolfram.com/BarycentricCoordinates.html)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXTextureGutterHelper](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 




