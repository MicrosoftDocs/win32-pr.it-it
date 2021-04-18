---
description: Salva una superficie in un file.
ms.assetid: 28bbf728-afde-4d25-8562-9d6a957aab2d
title: Funzione D3DXSaveSurfaceToFile (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSaveSurfaceToFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: cd19e0a8f7b9557b6bcbe6c71afcdca7c9037b70
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322600"
---
# <a name="d3dxsavesurfacetofile-function"></a>D3DXSaveSurfaceToFile (funzione)

Salva una superficie in un file.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXSaveSurfaceToFile(
  _In_       LPCTSTR              pDestFile,
  _In_       D3DXIMAGE_FILEFORMAT DestFormat,
  _In_       LPDIRECT3DSURFACE9   pSrcSurface,
  _In_ const PALETTEENTRY         *pSrcPalette,
  _In_ const RECT                 *pSrcRect
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pDestFile* \[ in\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Puntatore a una stringa che specifica il nome del file dell'immagine di destinazione. Se le impostazioni del compilatore richiedono Unicode, il tipo di dati LPCTSTR viene risolto in LPCWSTR. In caso contrario, il tipo di dati String viene risolto in LPCSTR. Vedere la sezione Osservazioni.

</dd> <dt>

*DestFormat* \[ in\]
</dt> <dd>

Tipo: **[ **D3DXIMAGE \_ FileFormat**](./d3dximage-fileformat.md)**

[**D3DXIMAGE \_ FileFormat**](./d3dximage-fileformat.md) che specifica il formato di file da utilizzare per il salvataggio. Questa funzione supporta il salvataggio in tutti i formati **D3DXIMAGE \_ FileFormat** ad eccezione di Portable Pixmap (. ppm) e targa/Truevision Graphics Adapter (. tga).

</dd> <dt>

*pSrcSurface* \[ in\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**

Puntatore all'interfaccia [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) che contiene l'immagine da salvare.

</dd> <dt>

*pSrcPalette* \[ in\]
</dt> <dd>

Tipo: **const [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***

Puntatore a una struttura [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) contenente una tavolozza di colori 256. Questo parametro può essere **NULL**.

</dd> <dt>

*pSrcRect* \[ in\]
</dt> <dd>

Tipo: **const [**Rect**](/previous-versions//dd162897(v=vs.85)) \***

Puntatore a una struttura [**Rect**](/previous-versions//dd162897(v=vs.85)) . Specifica il rettangolo di origine. Impostare questo parametro su **null** per specificare l'intera immagine.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. Se la funzione ha esito negativo, il valore restituito può essere il seguente: D3DERR \_ INVALIDCALL

## <a name="remarks"></a>Commenti

L'impostazione del compilatore determina anche la versione della funzione. Se è definito Unicode, la chiamata di funzione viene risolta in D3DXSaveSurfaceToFileW. In caso contrario, la chiamata di funzione viene risolta in D3DXSaveSurfaceToFileA perché vengono utilizzate le stringhe ANSI.

Questa funzione gestisce la conversione da e verso formati di trama compressi.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9tex. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni di trama in D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[**D3DXSaveTextureToFile**](d3dxsavetexturetofile.md)
</dt> <dt>

[**D3DXSaveVolumeToFile**](d3dxsavevolumetofile.md)
</dt> </dl>

 

 
