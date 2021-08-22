---
description: Salva una trama in un file.
ms.assetid: b14dd893-e967-4be9-81e8-aeb52035d91c
title: Funzione D3DXSaveTextureToFile (D3dx9tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSaveTextureToFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 954b761f8980a7397be1c79fbd8beb88ddbb29f29ce74557ca90cc77dee2ea5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118988319"
---
# <a name="d3dxsavetexturetofile-function"></a>Funzione D3DXSaveTextureToFile

Salva una trama in un file.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXSaveTextureToFile(
  _In_       LPCTSTR                pDestFile,
  _In_       D3DXIMAGE_FILEFORMAT   DestFormat,
  _In_       LPDIRECT3DBASETEXTURE9 pSrcTexture,
  _In_ const PALETTEENTRY           *pSrcPalette
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pDestFile* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Puntatore a una stringa che specifica il nome file dell'immagine di destinazione. Se le impostazioni del compilatore richiedono Unicode, il tipo di dati LPCTSTR viene risolto in LPCWSTR. In caso contrario, il tipo di dati string viene risolto in LPCSTR. Vedere la sezione Osservazioni.

</dd> <dt>

*DestFormat* \[ Pollici\]
</dt> <dd>

Tipo: **[ **D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md)**

[**D3DXIMAGE \_ FILEFORMAT che**](./d3dximage-fileformat.md) specifica il formato di file da usare durante il salvataggio. Questa funzione supporta il salvataggio in tutti i formati **\_ FILEFORMAT D3DXIMAGE,** ad eccezione di Portable Pixmap (con estensione ppm) e Dell'adattatore grafico Bitmap/Truevision (TGA).

</dd> <dt>

*pSrcTexture* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)**

Puntatore [**all'interfaccia IDirect3DBaseTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9) contenente la trama da salvare.

</dd> <dt>

*pSrcPalette* \[ Pollici\]
</dt> <dd>

Tipo: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***

Puntatore a [**una struttura PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) contenente una tavolozza di 256 colori. Questo parametro può essere **NULL**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. Se la funzione ha esito negativo, il valore restituito può essere il seguente: D3DERR \_ INVALIDCALL

## <a name="remarks"></a>Commenti

L'impostazione del compilatore determina anche la versione della funzione. Se unicode è definito, la chiamata di funzione viene risolta in D3DXSaveTextureToFileW. In caso contrario, la chiamata di funzione viene risolta in D3DXSaveTextureToFileA perché vengono usate stringhe ANSI.

Questa funzione gestisce la conversione da e verso formati di trama compressi.

Se il volume è non dinamico (a causa di un parametro di utilizzo impostato su 0 al momento della creazione) e si trova nella memoria video (il pool di memoria impostato su D3DPOOL \_ DEFAULT), **D3DXSaveTextureToFile** avrà esito negativo perché D3DX non è in grado di bloccare i volumi non dinamici che si trovano nella memoria video.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9tex.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni di trama in D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[**D3DXSaveSurfaceToFile**](d3dxsavesurfacetofile.md)
</dt> <dt>

[**D3DXSaveVolumeToFile**](d3dxsavevolumetofile.md)
</dt> </dl>

 

 
