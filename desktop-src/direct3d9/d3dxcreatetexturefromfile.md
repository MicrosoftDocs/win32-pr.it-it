---
description: Crea una trama da un file.
ms.assetid: 247b0ee2-ee31-4090-b94c-41951b46675f
title: Funzione D3DXCreateTextureFromFile (D3dx9tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateTextureFromFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b3ffce68a8044267e67d874412264d5a915c65b88ea5cc13b0cd8d2cd1400828
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117732160"
---
# <a name="d3dxcreatetexturefromfile-function"></a>Funzione D3DXCreateTextureFromFile

Crea una trama da un file.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXCreateTextureFromFile(
  _In_  LPDIRECT3DDEVICE9  pDevice,
  _In_  LPCTSTR            pSrcFile,
  _Out_ LPDIRECT3DTEXTURE9 *ppTexture
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pDevice* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Puntatore a [**un'interfaccia IDirect3DDevice9,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) che rappresenta il dispositivo da associare alla trama.

</dd> <dt>

*pSrcFile* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Puntatore a una stringa che specifica il nome file. Se le impostazioni del compilatore richiedono Unicode, il tipo di dati LPCTSTR viene risolto in LPCWSTR. In caso contrario, il tipo di dati stringa viene risolto in LPCSTR. Vedere la sezione Osservazioni.

</dd> <dt>

*ppTexture* \[ Cambio\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***

Indirizzo di un puntatore a [**un'interfaccia IDirect3DTexture9,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) che rappresenta l'oggetto trama creato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ NOTAVAILABLE, D3DERR \_ OUTOFVIDEOMEMORY, D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Commenti

L'impostazione del compilatore determina anche la versione della funzione. Se unicode è definito, la chiamata di funzione viene risolta in D3DXCreateTextureFromFileW. In caso contrario, la chiamata di funzione viene risolta in D3DXCreateTextureFromFileA perché vengono usate stringhe ANSI.

Questa funzione supporta i formati di file .bmp, dds, dib, hdr, .jpg, pfm, .png, ppm e tga. Vedere [**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md).

La funzione equivale a D3DXCreateTextureFromFileEx(pDevice, pSrcFile, D3DX \_ DEFAULT, \_ D3DX DEFAULT, D3DX \_ DEFAULT, 0, \_ D3DFMT UNKNOWN, D3DPOOL \_ MANAGED, D3DX \_ DEFAULT, D3DX \_ DEFAULT, 0, **NULL,** **NULL,** ppTexture).

Le trame mipmapped hanno automaticamente ogni livello riempito con la trama caricata.

Quando si caricano immagini in trame mipmapped, alcuni dispositivi non sono in grado di passare a un'immagine 1x1 e questa funzione avrà esito negativo. In questo caso, le immagini devono essere caricate manualmente.

Si noti che una risorsa creata con questa funzione verrà inserita nella classe di memoria denotata da D3DPOOL \_ MANAGED.

Il filtro viene applicato automaticamente a una trama creata usando questo metodo. Il filtro equivale a D3DX \_ FILTER \_ TRIANGLE \| D3DX \_ FILTER \_ DITHER in [D3DX \_ FILTER](d3dx-filter.md).

Per prestazioni ottimali quando si usa **D3DXCreateTextureFromFile**:

1.  L'esecuzione del ridimensionamento delle immagini e della conversione del formato in fase di caricamento può essere lenta. Archiviare le immagini nel formato e nella risoluzione che verranno usate. Se l'hardware di destinazione richiede potenza di due dimensioni, creare e archiviare immagini usando la potenza di due dimensioni.
2.  Prendere in considerazione l'uso di file DDS (DirectDraw Surface). Poiché i file DDS possono essere usati per rappresentare qualsiasi formato di trama Direct3D 9, sono molto facili da leggere per D3DX. Inoltre, possono archiviare mipmap, in modo che qualsiasi algoritmo di generazione mipmap possa essere usato per creare le immagini.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9tex.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**D3DXCreateTextureFromFileEx**](d3dxcreatetexturefromfileex.md)
</dt> <dt>

[Funzioni di trama in D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
