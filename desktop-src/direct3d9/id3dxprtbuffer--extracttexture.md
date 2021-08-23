---
description: Estrae i dati dei coefficienti da un canale di colore del buffer per un intervallo specificato di coefficienti e aggiunge i dati a un oggetto IDirect3DTexture9.
ms.assetid: 75854676-706a-4675-857e-4f2f8fc8365b
title: Metodo ID3DXPRTBuffer::ExtractTexture (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.ExtractTexture
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6f91186a15aa166928103073fdaca30d79809ad8c0a522abf3b136cb20a1d43a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119120625"
---
# <a name="id3dxprtbufferextracttexture-method"></a>Metodo ID3DXPRTBuffer::ExtractTexture

Estrae i dati dei coefficienti da un canale di colore del buffer per un intervallo specificato di coefficienti e aggiunge i dati a un [**oggetto IDirect3DTexture9.**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)

## <a name="syntax"></a>Sintassi


```C++
HRESULT ExtractTexture(
  [in] UINT               Channel,
  [in] UINT               StartCoefficient,
  [in] UINT               NumCoefficients,
  [in] LPDIRECT3DTEXTURE9 pTexture
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Canale* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Canale di colore del buffer da cui estrarre i dati della trama.

</dd> <dt>

*StartCoefficient* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Valore iniziale del coefficiente del buffer da cui estrarre i dati della trama.

</dd> <dt>

*NumCoefficients* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Numero di scalari, a partire da StartCoefficient, da cui estrarre i dati della trama.

</dd> <dt>

*pTexture* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**

Puntatore a un [**oggetto trama IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) che archivierà i coefficienti.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è S \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXPRTBuffer](id3dxprtbuffer.md)
</dt> </dl>

 

 
