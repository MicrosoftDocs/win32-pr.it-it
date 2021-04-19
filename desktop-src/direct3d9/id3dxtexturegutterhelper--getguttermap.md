---
description: Riceve un valore della classe Texel che indica la classe Texel in base alla posizione di ogni Texel.
ms.assetid: 450739a8-e30c-4e56-9560-8cb705a75672
title: 'Metodo ID3DXTextureGutterHelper:: GetGutterMap (D3DX9Mesh. h)'
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
ms.openlocfilehash: 9d973e716c598eaceaf7f75e6694a35691df4266
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322961"
---
# <a name="id3dxtexturegutterhelpergetguttermap-method"></a>Metodo ID3DXTextureGutterHelper:: GetGutterMap

Riceve un valore della classe Texel che indica la classe Texel in base alla posizione di ogni Texel.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetGutterMap(
  [in, out] BYTE *pGutterData
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pGutterData* \[ in uscita\]
</dt> <dd>

Tipo: **[ **byte**](../winprog/windows-data-types.md)\***

Puntatore alla classe Texel. Di seguito sono riportate le classi Texel possibili. Nessuna classe Texel 3.



| Classe Texel | Percorso Texel                                                                                                                                                                                                                                                                                                                                                                |
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0           | Punto non valido; Texel non verrà usato.                                                                                                                                                                                                                                                                                                                                        |
| 1           | Triangolo interno.                                                                                                                                                                                                                                                                                                                                                              |
| 2           | Barra interna.                                                                                                                                                                                                                                                                                                                                                                |
| 4           | Barra interna; Texel verrà valutato come un esempio completo nei metodi [**ID3DXTextureGutterHelper:: ApplyGuttersFloat**](id3dxtexturegutterhelper--applyguttersfloat.md), [**ID3DXTextureGutterHelper:: ApplyGuttersTex**](id3dxtexturegutterhelper--applygutterstex.md)o [**ID3DXTextureGutterHelper:: ApplyGuttersPRT**](id3dxtexturegutterhelper--applyguttersprt.md) . |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è \_ OK. Se il metodo ha esito negativo, verrà restituito il valore seguente. \_INVALIDCALL D3DERR

## <a name="remarks"></a>Commenti

L'applicazione deve allocare e gestire pGutterData, con le dimensioni fornite da:


```
texture width * texture height * sizeof(BYTE)
```



La larghezza e l'altezza della trama vengono restituite da [**ID3DXTextureGutterHelper:: GetWidth**](id3dxtexturegutterhelper--getwidth.md) e [**ID3DXTextureGutterHelper:: GetHeight**](id3dxtexturegutterhelper--getheight.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXTextureGutterHelper](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 
