---
description: Applica le grondature a un buffer di trama FLOAT.
ms.assetid: 822483d7-ae62-498a-bce7-3a925ab21c04
title: 'Metodo ID3DXTextureGutterHelper:: ApplyGuttersFloat (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.ApplyGuttersFloat
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 00ee6eac7328ee5f6adceb5b3966c222509237b4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322965"
---
# <a name="id3dxtexturegutterhelperapplyguttersfloat-method"></a>Metodo ID3DXTextureGutterHelper:: ApplyGuttersFloat

Applica le grondature a un buffer di trama FLOAT.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ApplyGuttersFloat(
  [in] FLOAT *pDataIn,
  [in] UINT  *NumCoeffs,
  [in] UINT  *Width,
  [in] UINT  *Height
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pDataIn* \[ in\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)\***

Puntatore a un buffer di dati di trama FLOAT.

</dd> <dt>

*NumCoeffs* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)\***

Numero di scalari per canale di colore utilizzato in memoria per archiviare esempi. Ogni Texel contiene valori FLOAT NumCoeffs.

</dd> <dt>

*Larghezza* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)\***

Larghezza della trama, in pixel, ottenuta da [**ID3DXTextureGutterHelper:: GetWidth**](id3dxtexturegutterhelper--getwidth.md).

</dd> <dt>

*Altezza* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)\***

Altezza della trama, in pixel, ottenuta da [**ID3DXTextureGutterHelper:: GetHeight**](id3dxtexturegutterhelper--getheight.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è \_ OK. Se il metodo ha esito negativo, verrà restituito il valore seguente. \_INVALIDCALL D3DERR

## <a name="remarks"></a>Commenti

I [**Texel della classe 2**](id3dxtexturegutterhelper.md) vengono generati ricampionando la classe 1 e 4 Texel.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXTextureGutterHelper](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 
