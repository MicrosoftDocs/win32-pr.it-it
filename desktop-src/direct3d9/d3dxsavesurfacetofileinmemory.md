---
description: Salva una superficie in un file di immagine.
ms.assetid: 6320e5ed-e43d-43bf-a746-5478df42941d
title: Funzione D3DXSaveSurfaceToFileInMemory (D3dx9tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSaveSurfaceToFileInMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6dd6715c05be0e6472b1c630ebdda209d48dfc571d4b3d5234b80f3700e597d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119986441"
---
# <a name="d3dxsavesurfacetofileinmemory-function"></a>Funzione D3DXSaveSurfaceToFileInMemory

Salva una superficie in un file di immagine.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXSaveSurfaceToFileInMemory(
  _Out_       LPD3DXBUFFER         *ppDestBuf,
  _In_        D3DXIMAGE_FILEFORMAT DestFormat,
  _In_        LPDIRECT3DSURFACE9   pSrcSurface,
  _In_  const PALETTEENTRY         *pSrcPalette,
  _In_  const RECT                 *pSrcRect
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppDestBuf* \[ Cambio\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Indirizzo di un puntatore a [**un oggetto ID3DXBuffer**](id3dxbuffer.md) che archivierà l'immagine.

</dd> <dt>

*DestFormat* \[ Pollici\]
</dt> <dd>

Tipo: **[ **D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md)**

[**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md) che specifica il formato di file da usare durante il salvataggio. Questa funzione supporta il salvataggio in tutti i formati **\_ FILEFORMAT D3DXIMAGE,** ad eccezione di Portable Pixmap (.ppm) e Dell'adattatore grafico Persica/Truevision (.tga).

</dd> <dt>

*pSrcSurface* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**

Puntatore [**all'interfaccia IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) contenente l'immagine da salvare.

</dd> <dt>

*pSrcPalette* \[ Pollici\]
</dt> <dd>

Tipo: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***

Puntatore a una [**struttura PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) contenente una tavolozza di 256 colori. Questo parametro può essere **NULL**.

</dd> <dt>

*pSrcRect* \[ Pollici\]
</dt> <dd>

Tipo: **const [**RECT**](/previous-versions//dd162897(v=vs.85)) \***

Puntatore a una [**struttura RECT.**](/previous-versions//dd162897(v=vs.85)) Specifica il rettangolo di origine. Impostare questo parametro su **NULL per** specificare l'intera immagine.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. Se la funzione ha esito negativo, il valore restituito può essere il seguente: D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Commenti

Questa funzione gestisce la conversione da e verso formati di trama compressi.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9tex.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni di trama in D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[**D3DXSaveVolumeToFileInMemory**](d3dxsavevolumetofileinmemory.md)
</dt> </dl>

 

 
