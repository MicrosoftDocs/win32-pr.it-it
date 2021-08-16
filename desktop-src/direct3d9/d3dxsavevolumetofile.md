---
description: Salva un volume in un file su disco.
ms.assetid: 4d33fba5-e003-4385-b683-aff6723af2a5
title: Funzione D3DXSaveVolumeToFile (D3dx9tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSaveVolumeToFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7e6c5a03f9e1874d7706ecbf43cfd312abc472b8e7127ba9f21a35313374157b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118524446"
---
# <a name="d3dxsavevolumetofile-function"></a>Funzione D3DXSaveVolumeToFile

Salva un volume in un file su disco.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXSaveVolumeToFile(
  _In_       LPCTSTR              pDestFile,
  _In_       D3DXIMAGE_FILEFORMAT DestFormat,
  _In_       LPDIRECT3DVOLUME9    pSrcVolume,
  _In_ const PALETTEENTRY         *pSrcPalette,
  _In_ const D3DBOX               *pSrcBox
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pDestFile* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Puntatore a una stringa che specifica il nome file dell'immagine di destinazione. Se le impostazioni del compilatore richiedono Unicode, il tipo di dati LPCTSTR viene risolto in LPCWSTR. In caso contrario, il tipo di dati stringa viene risolto in LPCSTR. Vedere la sezione Osservazioni.

</dd> <dt>

*DestFormat* \[ Pollici\]
</dt> <dd>

Tipo: **[ **D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md)**

[**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md) che specifica il formato di file da usare durante il salvataggio. Questa funzione supporta il salvataggio in tutti i formati **\_ FILEFORMAT D3DXIMAGE,** ad eccezione di Portable Pixmap (.ppm) e Dell'adattatore grafico Persica/Truevision (.tga).

</dd> <dt>

*pSrcVolume* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**

Puntatore [**all'interfaccia IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9) contenente l'immagine da salvare.

</dd> <dt>

*pSrcPalette* \[ Pollici\]
</dt> <dd>

Tipo: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***

Puntatore a una [**struttura PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) contenente una tavolozza di 256 colori. Questo parametro può essere **NULL**.

</dd> <dt>

*pSrcBox* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DBOX**](d3dbox.md) \***

Puntatore a [**una struttura D3DBOX.**](d3dbox.md) Specifica la casella di origine. Impostare questo parametro su **NULL per** specificare l'intero volume.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. Se la funzione ha esito negativo, il valore restituito può essere il seguente: D3DERR \_ INVALIDCALL

## <a name="remarks"></a>Commenti

L'impostazione del compilatore determina anche la versione della funzione. Se unicode è definito, la chiamata di funzione viene risolta in D3DXSaveVolumeToFileW. In caso contrario, la chiamata di funzione viene risolta >D3DXSaveVolumeToFileA perché vengono usate stringhe ANSI.

Questa funzione gestisce la conversione da e verso formati di trama compressi.

Se il volume non è dinamico (a causa di un parametro di utilizzo impostato su 0 al momento della creazione) e si trova nella memoria video (pool di memoria impostato su D3DPOOL \_ DEFAULT), [**D3DXSaveTextureToFile**](d3dxsavetexturetofile.md) avrà esito negativo perché D3DX non è in grado di bloccare i volumi non dinamici che si trovano nella memoria video.

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

[**D3DXSaveTextureToFile**](d3dxsavetexturetofile.md)
</dt> <dt>

[**D3DXSaveVolumeToFileInMemory**](d3dxsavevolumetofileinmemory.md)
</dt> </dl>

 

 
