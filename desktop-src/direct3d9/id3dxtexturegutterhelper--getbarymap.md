---
description: Recupera le coordinate baricentrica Texel.
ms.assetid: f380a37f-b9c1-4433-b1d6-e9feeca79b30
title: 'Metodo ID3DXTextureGutterHelper:: GetBaryMap (D3DX9Mesh. h)'
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
ms.openlocfilehash: 246117569b9106de18a31d08613146a3aa0d88c2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322963"
---
# <a name="id3dxtexturegutterhelpergetbarymap-method"></a>Metodo ID3DXTextureGutterHelper:: GetBaryMap

Recupera le coordinate baricentrica Texel.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetBaryMap(
  [in, out] D3DXVECTOR2 *pBaryData
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pBaryData* \[ in uscita\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***

Puntatore a una struttura [**D3DXVECTOR2**](d3dxvector2.md) che contiene le prime due coordinate baricentrica di ogni Texel.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è \_ OK. Se il metodo ha esito negativo, verrà restituito il valore seguente. \_INVALIDCALL D3DERR

## <a name="remarks"></a>Commenti

La terza coordinata baricentrica viene fornita da:


```
    1 - ( pBaryData.x + pBaryData.y )
```



Le coordinate baricentrica vengono sempre specificate rispetto al triangolo restituito da [**ID3DXTextureGutterHelper:: GetFaceMap**](id3dxtexturegutterhelper--getfacemap.md).

Le coordinate baricentrica restituite da questo metodo sono valide solo per Texel validi (non di classe 0). [**ID3DXTextureGutterHelper:: GetGutterMap**](id3dxtexturegutterhelper--getguttermap.md) restituirà valori diversi da zero per i Texel validi.

Viene eseguito il mapping dei [**Texel della classe 2**](id3dxtexturegutterhelper.md) al punto più vicino sul triangolo nello spazio Texel.

L'applicazione deve allocare e gestire pBaryData.

Le coordinate baricentrica definiscono un punto all'interno di un triangolo in termini di vertici del triangolo. Per una descrizione più approfondita delle coordinate baricentrica, vedere [la descrizione delle coordinate baricentrica di articolo MathWorld](https://mathworld.wolfram.com/BarycentricCoordinates.html).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXTextureGutterHelper](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 




