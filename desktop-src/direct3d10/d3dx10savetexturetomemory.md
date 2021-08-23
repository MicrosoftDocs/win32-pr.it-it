---
description: Salvare una trama in memoria.
ms.assetid: be541b99-6d07-480e-8f28-b7fc44566e7d
title: Funzione D3DX10SaveTextureToMemory (D3DX10Tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10SaveTextureToMemory
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 3736b2de21df3e77f5b06d34f2b0b64a7592f2212a71ffd4a37b70454667427a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047059"
---
# <a name="d3dx10savetexturetomemory-function"></a>Funzione D3DX10SaveTextureToMemory

Salvare una trama in memoria.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DX10SaveTextureToMemory(
  _In_  ID3D10Resource           *pSrcTexture,
  _In_  D3DX10_IMAGE_FILE_FORMAT DestFormat,
  _Out_ LPD3D10BLOB              *ppDestBuf,
  _In_  UINT                     Flags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pSrcTexture* \[ Pollici\]
</dt> <dd>

Tipo: **[ **ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\***

Puntatore alla trama da salvare. Vedere [**ID3D10Resource Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource).

</dd> <dt>

*DestFormat* \[ Pollici\]
</dt> <dd>

Tipo: **[ **D3DX10 \_ IMAGE \_ FILE \_ FORMAT**](d3dx10-image-file-format.md)**

Formato con cui verrà salvata la trama. Vedere [**D3DX10 \_ IMAGE FILE \_ \_ FORMAT**](d3dx10-image-file-format.md).

</dd> <dt>

*ppDestBuf* \[ Cambio\]
</dt> <dd>

Tipo: **[ **LPD3D10BLOB**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)\***

Indirizzo di un puntatore alla memoria contenente la trama salvata. Vedere [**ID3D10 Interface (Interfaccia ID3D10Blob).**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)

</dd> <dt>

*Flag* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

facoltativo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Il valore restituito è uno dei valori elencati in Codici restituiti [Direct3D 10.](d3d10-graphics-reference-returnvalues.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10Tex.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3DX10.lib</dt> </dl>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni di trama in D3DX 10](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> <dt>

[per utilizzo generico funzioni](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
