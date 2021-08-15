---
description: Applica le grondaie a un buffer di trama FLOAT.
ms.assetid: 822483d7-ae62-498a-bce7-3a925ab21c04
title: Metodo ID3DXTextureGutterHelper::ApplyGuttersFloat (D3DX9Mesh.h)
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
ms.openlocfilehash: 6c0401a6d0692331adf9e80c800530690e59eeec5e6a9463b57425af1a3f9330
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118800364"
---
# <a name="id3dxtexturegutterhelperapplyguttersfloat-method"></a>Metodo ID3DXTextureGutterHelper::ApplyGuttersFloat

Applica le grondaie a un buffer di trama FLOAT.

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

*pDataIn* \[ Pollici\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Puntatore a un buffer di dati di trama FLOAT.

</dd> <dt>

*NumCoeff* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)\***

Numero di scalari per canale di colore usati in memoria per archiviare gli esempi. Ogni texel contiene valori FLOAT NumCoeffs.

</dd> <dt>

*Larghezza* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)\***

Larghezza della trama, in pixel, ottenuta da [**ID3DXTextureGutterHelper::GetWidth**](id3dxtexturegutterhelper--getwidth.md).

</dd> <dt>

*Altezza* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)\***

Altezza della trama, in pixel, ottenuta da [**ID3DXTextureGutterHelper::GetHeight**](id3dxtexturegutterhelper--getheight.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è S \_ OK. Se il metodo ha esito negativo, verrà restituito il valore seguente. D3DERR \_ INVALIDCALL

## <a name="remarks"></a>Commenti

[**I texel di**](id3dxtexturegutterhelper.md) classe 2 vengono generati tramite il ricampionamento delle classi 1 e 4 texel.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXTextureGutterHelper](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 
