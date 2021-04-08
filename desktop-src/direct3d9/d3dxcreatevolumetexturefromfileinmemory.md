---
description: Crea una trama del volume da un file in memoria.
ms.assetid: 8ea22209-6110-4bef-a0d6-667f59017adc
title: Funzione D3DXCreateVolumeTextureFromFileInMemory (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateVolumeTextureFromFileInMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 380aadd9e26940b2a67c2064b3941a0965a782f0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762059"
---
# <a name="d3dxcreatevolumetexturefromfileinmemory-function"></a>D3DXCreateVolumeTextureFromFileInMemory (funzione)

Crea una trama del volume da un file in memoria.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXCreateVolumeTextureFromFileInMemory(
  _In_  LPDIRECT3DDEVICE9        pDevice,
  _In_  LPCVOID                  pSrcFile,
  _In_  UINT                     SrcData,
  _Out_ LPDIRECT3DVOLUMETEXTURE9 ppVolumeTexture
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PDEVICE* \[ in\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Puntatore a un'interfaccia [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , che rappresenta il dispositivo da associare alla trama del volume.

</dd> <dt>

*pSrcFile* \[ in\]
</dt> <dd>

Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**

Puntatore al file in memoria da cui creare la trama del volume.

</dd> <dt>

*SrcData* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Dimensioni in byte del file in memoria.

</dd> <dt>

*ppVolumeTexture* \[ out\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)**

Indirizzo di un puntatore a un'interfaccia [**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) , che rappresenta l'oggetto trama creato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ NOTAVAILABLE, D3DERR \_ OUTOFVIDEOMEMORY, D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OutOfMemory.

## <a name="remarks"></a>Commenti

Questa funzione supporta i formati di file seguenti:. bmp,. DDS,. DIB,. HDR,. jpg,. PFM,. png,. ppm e. tga. Vedere [**D3DXIMAGE \_ FileFormat**](./d3dximage-fileformat.md).

La funzione è equivalente a D3DXCreateVolumeTextureFromFileInMemoryEx (pDevice, pSrcFile, SrcData, D3DX \_ default, D3DX \_ default, D3DX \_ default, D3DX \_ default, 0, D3DFMT \_ Unknown, D3DPOOL \_ Managed, D3DX default \_ , D3DX \_ default, 0, **null**, **null**, ppVolumeTexture).

Si noti che una risorsa creata con questa funzione quando viene chiamata da un oggetto IDirect3DDevice9 verrà inserita nella classe di memoria indicata da D3DPOOL \_ gestito. Quando questo metodo viene chiamato da un oggetto IDirect3DDevice9Ex, la risorsa verrà inserita nella classe di memoria indicata da D3DPOOL \_ default.

Il filtro viene applicato automaticamente a una trama creata utilizzando questo metodo. Il filtro è equivalente a D3DX Filter D3DX del filtro \_ \_ \| \_ \_ di retinazione nel [ \_ filtro D3DX](d3dx-filter.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9tex. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**D3DXCreateVolumeTextureFromFile**](d3dxcreatevolumetexturefromfile.md)
</dt> <dt>

[**D3DXCreateVolumeTextureFromFileEx**](d3dxcreatevolumetexturefromfileex.md)
</dt> <dt>

[**D3DXCreateVolumeTextureFromFileInMemoryEx**](d3dxcreatevolumetexturefromfileinmemoryex.md)
</dt> <dt>

[**D3DXCreateVolumeTextureFromResource**](d3dxcreatevolumetexturefromresource.md)
</dt> <dt>

[**D3DXCreateVolumeTextureFromResourceEx**](d3dxcreatevolumetexturefromresourceex.md)
</dt> <dt>

[Funzioni di trama in D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
