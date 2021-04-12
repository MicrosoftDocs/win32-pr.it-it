---
description: Imposta le coordinate del baricentrica Texel.
ms.assetid: 6c7c74aa-71a3-45aa-9b18-6409fbd63bda
title: 'Metodo ID3DXTextureGutterHelper:: SetBaryMap (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.SetBaryMap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5e3de61913041a4e59e075ea42dacc308c1ce5f2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235162"
---
# <a name="id3dxtexturegutterhelpersetbarymap-method"></a>Metodo ID3DXTextureGutterHelper:: SetBaryMap

Imposta le coordinate del baricentrica Texel.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetBaryMap(
  [in] D3DXVECTOR2 *pBaryData
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pBaryData* \[ in\]
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



Il baricentrica coordina l'input per questo metodo è valido solo per Texel validi (non di classe 0). [**ID3DXTextureGutterHelper:: GetGutterMap**](id3dxtexturegutterhelper--getguttermap.md) restituirà valori diversi da zero per i Texel validi.

Le coordinate baricentrica definiscono un punto all'interno di un triangolo in termini di vertici del triangolo. Per una descrizione più approfondita delle coordinate baricentrica, vedere [la descrizione delle coordinate baricentrica di articolo MathWorld](http://mathworld.wolfram.com/BarycentricCoordinates.html).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXTextureGutterHelper](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 




