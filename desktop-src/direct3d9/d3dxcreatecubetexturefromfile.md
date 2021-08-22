---
description: Crea una trama del cubo da un file.
ms.assetid: 7ff3b051-568c-4c77-b8a6-b626ba156eb1
title: Funzione D3DXCreateCubeTextureFromFile (D3dx9tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateCubeTextureFromFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e25b6692fc22eed1695b1d60b019a595826de15af87e4ca70f2610a621abc532
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119279891"
---
# <a name="d3dxcreatecubetexturefromfile-function"></a>Funzione D3DXCreateCubeTextureFromFile

Crea una trama del cubo da un file.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXCreateCubeTextureFromFile(
  _In_  LPDIRECT3DDEVICE9      pDevice,
  _In_  LPCTSTR                pSrcFile,
  _Out_ LPDIRECT3DCUBETEXTURE9 *ppCubeTexture
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pDevice* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Puntatore a [**un'interfaccia IDirect3DDevice9,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) che rappresenta il dispositivo da associare alla trama del cubo.

</dd> <dt>

*pSrcFile* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Puntatore a una stringa che specifica il nome file. Se le impostazioni del compilatore richiedono Unicode, il tipo di dati LPCTSTR viene risolto in LPCWSTR. In caso contrario, il tipo di dati stringa viene risolto in LPCSTR. Vedere la sezione Osservazioni.

</dd> <dt>

*ppCubeTexture* \[ Cambio\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)\***

Indirizzo di un puntatore a [**un'interfaccia IDirect3DCubeTexture9,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) che rappresenta l'oggetto trama del cubo creato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. Se la funzione ha esito negativo, il valore restituito può essere uno dei valori seguenti: D3DERR \_ INVALIDCALL, D3DERR \_ NOTAVAILABLE, D3DERR \_ OUTOFVIDEOMEMORY, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Commenti

L'impostazione del compilatore determina anche la versione della funzione. Se unicode è definito, la chiamata di funzione viene risolta in **D3DXCreateCubeTextureFromFileW**. In caso contrario, la chiamata di funzione viene risolta **in D3DXCreateCubeTextureFromFileA** perché vengono usate stringhe ANSI.

La funzione equivale a D3DXCreateCubeTextureFromFileEx(pDevice, pSrcFile, D3DX \_ DEFAULT, D3DX \_ DEFAULT, 0, D3DFMT \_ UNKNOWN, D3DPOOL \_ MANAGED, D3DX \_ DEFAULT, D3DX \_ DEFAULT, 0, **NULL,** **NULL,** ppCubeTexture).

Questa funzione supporta i formati di file .bmp, dds, dib, hdr, .jpg, pfm, .png, ppm e tga. Vedere [**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md).

Si noti che una risorsa creata con questa funzione quando viene chiamata da un oggetto IDirect3DDevice9 verrà inserita nella classe di memoria denotata da D3DPOOL \_ MANAGED. Quando questo metodo viene chiamato da un oggetto IDirect3DDevice9Ex, la risorsa verrà inserita nella classe di memoria indicato da D3DPOOL \_ DEFAULT.

Il filtro viene applicato automaticamente a una trama creata usando questo metodo. Il filtro equivale a D3DX \_ FILTER \_ TRIANGLE \| D3DX \_ FILTER \_ DITHER in [D3DX \_ FILTER](d3dx-filter.md).

**D3DXCreateCubeTextureFromFile** usa il formato di file directdraw surface (DDS). DirectX Texture Editor (Dxtex.exe) consente di generare una mappa cubo da altri formati di file e salvarla nel formato di file DDS. È possibile ottenere Dxtex.exe e ottenere informazioni da DirectX SDK. Per informazioni su DirectX SDK, vedere [Dove si trova DirectX SDK?](../directx-sdk--august-2009-.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9tex.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**D3DXCreateCubeTextureFromFileEx**](d3dxcreatecubetexturefromfileex.md)
</dt> <dt>

[Funzioni di trama in D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
