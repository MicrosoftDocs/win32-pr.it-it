---
description: Salva un volume in un buffer. Il metodo crea un buffer ID3DXBuffer per archiviare i dati e restituisce tale oggetto.
ms.assetid: 4887ff1f-7904-4764-b284-b2c8e037f806
title: Funzione D3DXSaveVolumeToFileInMemory (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSaveVolumeToFileInMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7daaa41e0cc87ea03a0aedc5fc2f7ca96653329f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235001"
---
# <a name="d3dxsavevolumetofileinmemory-function"></a>D3DXSaveVolumeToFileInMemory (funzione)

Salva un volume in un buffer. Il metodo crea un buffer [**ID3DXBuffer**](id3dxbuffer.md) per archiviare i dati e restituisce tale oggetto.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXSaveVolumeToFileInMemory(
  _Out_       LPD3DXBUFFER         *ppDestBuf,
  _In_        D3DXIMAGE_FILEFORMAT DestFormat,
  _In_        LPDIRECT3DVOLUME9    pSrcVolume,
  _In_  const PALETTEENTRY         *pSrcPalette,
  _In_  const D3DBOX               *pSrcBox
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppDestBuf* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Indirizzo di un puntatore a un buffer [**ID3DXBuffer**](id3dxbuffer.md) che archivia l'immagine.

</dd> <dt>

*DestFormat* \[ in\]
</dt> <dd>

Tipo: **[ **D3DXIMAGE \_ FileFormat**](./d3dximage-fileformat.md)**

[**D3DXIMAGE \_ FileFormat**](./d3dximage-fileformat.md) che specifica il formato di file da utilizzare per il salvataggio. Questa funzione supporta il salvataggio in tutti i formati **D3DXIMAGE \_ FileFormat** ad eccezione di Portable Pixmap (. ppm) e targa/Truevision Graphics Adapter (. tga).

</dd> <dt>

*pSrcVolume* \[ in\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**

Puntatore all'interfaccia [**IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9) che contiene l'immagine da salvare.

</dd> <dt>

*pSrcPalette* \[ in\]
</dt> <dd>

Tipo: **const [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***

Puntatore a una struttura [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) contenente una tavolozza di colori 256. Questo parametro può essere **NULL**.

</dd> <dt>

*pSrcBox* \[ in\]
</dt> <dd>

Tipo: **const [**D3DBOX**](d3dbox.md) \***

Puntatore a una struttura [**D3DBOX**](d3dbox.md) . Specifica la casella di origine. Impostare questo parametro su **null** per specificare l'intero volume.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. Se la funzione ha esito negativo, il valore restituito può essere il seguente: D3DERR \_ INVALIDCALL

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9tex. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni di trama in D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[**D3DXSaveVolumeToFile**](d3dxsavevolumetofile.md)
</dt> </dl>

 

 
