---
description: Verifica i parametri di creazione della trama del volume.
ms.assetid: 1a02cb99-2582-4d8f-aacf-67ed75f6deb8
title: Funzione D3DXCheckVolumeTextureRequirements (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCheckVolumeTextureRequirements
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4940cab936ed14c847e7224c9f619244c6e422a9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104401975"
---
# <a name="d3dxcheckvolumetexturerequirements-function"></a>D3DXCheckVolumeTextureRequirements (funzione)

Verifica i parametri di creazione della trama del volume.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXCheckVolumeTextureRequirements(
  _In_    LPDIRECT3DDEVICE9 pDevice,
  _Inout_ UINT              *pWidth,
  _Inout_ UINT              *pHeight,
  _Inout_ UINT              *pDepth,
  _Inout_ UINT              *pNumMipLevels,
  _In_    DWORD             Usage,
  _Inout_ D3DFORMAT         *pFormat,
  _In_    D3DPOOL           Pool
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PDEVICE* \[ in\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Puntatore a un'interfaccia [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , che rappresenta il dispositivo da associare alla trama del volume.

</dd> <dt>

*pWidth* \[ in uscita\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)\***

Puntatore alla larghezza richiesta, in pixel, o **null**. Restituisce la dimensione corretta.

</dd> <dt>

*pHeight* \[ in uscita\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)\***

Puntatore all'altezza richiesta, in pixel, o **null**. Restituisce la dimensione corretta.

</dd> <dt>

*pDepth* \[ in uscita\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)\***

Puntatore alla profondità richiesta in pixel o **null**. Restituisce la dimensione corretta.

</dd> <dt>

*pNumMipLevels* \[ in uscita\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)\***

Puntatore al numero di livelli di mipmap richiesti o **null**. Restituisce il numero corretto di livelli di mipmap.

</dd> <dt>

*Utilizzo* \[ di in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Attualmente non utilizzato, impostato su 0.

</dd> <dt>

*pFormat* \[ in uscita\]
</dt> <dd>

Tipo: **[D3DFORMAT](d3dformat.md)\***

Puntatore a un membro del tipo enumerato [D3DFORMAT](d3dformat.md) . Specifica il formato pixel desiderato o **null**. Restituisce il formato corretto.

</dd> <dt>

*Pool* \[ di in\]
</dt> <dd>

Tipo: **[ **D3DPOOL**](./d3dpool.md)**

Membro del tipo enumerato [**D3DPOOL**](./d3dpool.md) , che descrive la classe di memoria in cui deve essere inserita la trama del volume.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ NOTAVAILABLE, D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Commenti

Se i parametri di questa funzione non sono validi, questa funzione restituisce parametri corretti.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9tex. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni di trama in D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
