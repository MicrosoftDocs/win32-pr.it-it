---
description: Riceve un valore della classe texel che indica la classe texel in base alla posizione di ogni texel.
ms.assetid: 450739a8-e30c-4e56-9560-8cb705a75672
title: Metodo ID3DXTextureGutterHelper::GetGutterMap (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.GetGutterMap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8ef2ed7b088e54dd82b1cc99422e1488139199ffe034e810de8e0a0bdb242f46
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120095691"
---
# <a name="id3dxtexturegutterhelpergetguttermap-method"></a>Metodo ID3DXTextureGutterHelper::GetGutterMap

Riceve un valore della classe texel che indica la classe texel in base alla posizione di ogni texel.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetGutterMap(
  [in, out] BYTE *pGutterData
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pGutterData* \[ in, out\]
</dt> <dd>

Tipo: **[ **BYTE**](../winprog/windows-data-types.md)\***

Puntatore alla classe texel. Le possibili classi texel sono le seguenti. Non esiste alcuna classe texel 3.



| Classe Texel | Posizione di Texel                                                                                                                                                                                                                                                                                                                                                                |
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0           | Punto non valido. texel non verrà usato.                                                                                                                                                                                                                                                                                                                                        |
| 1           | Triangolo interno.                                                                                                                                                                                                                                                                                                                                                              |
| 2           | All'interno della grondaia.                                                                                                                                                                                                                                                                                                                                                                |
| 4           | All'interno della grondaia; Il texel verrà valutato come esempio completo nei metodi [**ID3DXTextureGutterHelper::ApplyGuttersFloat,**](id3dxtexturegutterhelper--applyguttersfloat.md) [**ID3DXTextureGutterHelper::ApplyGuttersTex**](id3dxtexturegutterhelper--applygutterstex.md)o [**ID3DXTextureGutterHelper::ApplyGuttersPRT.**](id3dxtexturegutterhelper--applyguttersprt.md) |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è S \_ OK. Se il metodo ha esito negativo, verrà restituito il valore seguente. D3DERR \_ INVALIDCALL

## <a name="remarks"></a>Commenti

L'applicazione deve allocare e gestire pGutterData, con le dimensioni specificate da:


```
texture width * texture height * sizeof(BYTE)
```



La larghezza e l'altezza della trama vengono restituite da [**ID3DXTextureGutterHelper::GetWidth**](id3dxtexturegutterhelper--getwidth.md) e [**ID3DXTextureGutterHelper::GetHeight**](id3dxtexturegutterhelper--getheight.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXTextureGutterHelper](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 
