---
description: Carica un volume da un file in memoria.
ms.assetid: d450b652-3a74-45ea-9506-e05da87821d7
title: Funzione D3DXLoadVolumeFromFileInMemory (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadVolumeFromFileInMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 97ac67ab66a0072598bfea3b190bdf2c81ceba9a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969338"
---
# <a name="d3dxloadvolumefromfileinmemory-function"></a>D3DXLoadVolumeFromFileInMemory (funzione)

Carica un volume da un file in memoria.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXLoadVolumeFromFileInMemory(
  _In_       LPDIRECT3DVOLUME9 pDestVolume,
  _In_ const PALETTEENTRY      *pDestPalette,
  _In_ const D3DBOX            *pDestBox,
  _In_       LPCVOID           pSrcData,
  _In_       UINT              SrcDataSize,
  _In_ const D3DBOX            *pSrcBox,
  _In_       DWORD             Filter,
  _In_       D3DCOLOR          ColorKey,
  _In_       D3DXIMAGE_INFO    *pSrcInfo
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pDestVolume* \[ in\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**

Puntatore a un'interfaccia [**IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9) . Specifica il volume di destinazione.

</dd> <dt>

*pDestPalette* \[ in\]
</dt> <dd>

Tipo: **const [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***

Puntatore a una struttura [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , la tavolozza di destinazione di 256 colori o **null**.

</dd> <dt>

*pDestBox* \[ in\]
</dt> <dd>

Tipo: **const [**D3DBOX**](d3dbox.md) \***

Puntatore a una struttura [**D3DBOX**](d3dbox.md) . Specifica la casella di destinazione. Impostare questo parametro su **null** per specificare l'intero volume.

</dd> <dt>

*pSrcData* \[ in\]
</dt> <dd>

Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**

Puntatore al file in memoria da cui caricare il volume.

</dd> <dt>

*SrcDataSize* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Dimensioni in byte del file in memoria.

</dd> <dt>

*pSrcBox* \[ in\]
</dt> <dd>

Tipo: **const [**D3DBOX**](d3dbox.md) \***

Puntatore a una struttura [**D3DBOX**](d3dbox.md) . Specifica la casella di origine. Impostare questo parametro su **null** per specificare l'intero volume.

</dd> <dt>

*Filtro* \[ di in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Combinazione di uno o più [ \_ filtri D3DX](d3dx-filter.md), che controllano il modo in cui l'immagine viene filtrata. Specificare \_ il valore predefinito di D3DX per questo parametro equivale a specificare \_ il \_ \| \_ dithering del filtro D3DX del triangolo di filtro D3DX \_ .

</dd> <dt>

*ColorKey* \[ in\]
</dt> <dd>

Tipo: **[ **D3DCOLOR**](d3dcolor.md)**

Valore [**D3DCOLOR**](d3dcolor.md) da sostituire con nero trasparente oppure 0 per disabilitare il colorkey. Si tratta sempre di un colore ARGB a 32 bit, indipendente dal formato di immagine di origine. Alfa è significativo e in genere deve essere impostato su FF per le chiavi di colore opache. Pertanto, per il nero opaco, il valore sarà uguale a 0xFF000000.

</dd> <dt>

*pSrcInfo* \[ in\]
</dt> <dd>

Tipo: **[ **D3DXIMAGE \_ info**](d3dximage-info.md)\***

Puntatore a una struttura di [**\_ informazioni D3DXIMAGE**](d3dximage-info.md) per la compilazione di una descrizione dei dati nel file di immagine di origine o **null**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Commenti

Questa funzione gestisce la conversione da e verso formati di trama compressi e supporta i formati di file seguenti: BMP, DDS, DIB, HDR, jpg, PFM, PNG, ppm e TGA. Vedere [**D3DXIMAGE \_ FileFormat**](./d3dximage-fileformat.md).

La scrittura in una superficie non di livello zero della trama del volume non comporterà l'aggiornamento del rettangolo modificato. Se viene chiamato **D3DXLoadVolumeFromFileInMemory** e la trama non è già sporca (probabilmente in scenari di utilizzo normali), l'applicazione deve chiamare in modo esplicito [**IDirect3DVolumeTexture9:: AddDirtyBox**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-adddirtybox) sulla trama del volume.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9tex. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**D3DXLoadVolumeFromFile**](d3dxloadvolumefromfile.md)
</dt> <dt>

[**D3DXLoadVolumeFromMemory**](d3dxloadvolumefrommemory.md)
</dt> <dt>

[**D3DXLoadVolumeFromResource**](d3dxloadvolumefromresource.md)
</dt> <dt>

[**D3DXLoadVolumeFromVolume**](d3dxloadvolumefromvolume.md)
</dt> <dt>

[Funzioni di trama in D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
