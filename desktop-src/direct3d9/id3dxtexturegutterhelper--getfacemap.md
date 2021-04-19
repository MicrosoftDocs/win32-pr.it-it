---
description: Recupera l'indice della faccia mesh a cui appartiene ogni Texel.
ms.assetid: 3eb3461c-4e16-4c89-9ca9-fc9c6b5638c7
title: 'Metodo ID3DXTextureGutterHelper:: GetFaceMap (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.GetFaceMap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8164ec35c3b3596914577287ecc6b9285142fca8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322962"
---
# <a name="id3dxtexturegutterhelpergetfacemap-method"></a>Metodo ID3DXTextureGutterHelper:: GetFaceMap

Recupera l'indice della faccia mesh a cui appartiene ogni Texel.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetFaceMap(
  [in] UINT *pFaceData
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pFaceData* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)\***

Puntatore all'indice della faccia mesh a cui appartiene ogni Texel.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è \_ OK. Se il metodo ha esito negativo, verrà restituito il valore seguente. \_INVALIDCALL D3DERR

## <a name="remarks"></a>Commenti

I dati della faccia mesh restituiti da questo metodo sono validi solo per Texel validi (non di classe 0). [**ID3DXTextureGutterHelper:: GetGutterMap**](id3dxtexturegutterhelper--getguttermap.md) restituirà valori diversi da zero per Texel validi (non di classe 0).

Per i [**Texel della classe 2**](id3dxtexturegutterhelper.md), questo metodo recupera la faccia più vicina.

L'applicazione deve allocare e gestire pFaceData.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXTextureGutterHelper](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 
