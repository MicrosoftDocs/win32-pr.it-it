---
description: Carica una serie di caratteri nella memoria video per migliorare l'efficienza del rendering nel dispositivo.
ms.assetid: bb49842e-99de-406b-bf4b-139d6499f96e
title: Metodo ID3DXFont::P reloadCharacters (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont.PreloadCharacters
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9262fcb386b9362093ad563bd851946fd2305c7c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323541"
---
# <a name="id3dxfontpreloadcharacters-method"></a>ID3DXFont::P metodo reloadCharacters

Carica una serie di caratteri nella memoria video per migliorare l'efficienza del rendering nel dispositivo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT PreloadCharacters(
  [in] UINT First,
  [in] UINT Last
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Primo* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

ID del primo carattere da caricare nella memoria video.

</dd> <dt>

*Ultima* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

ID dell'ultimo carattere da caricare nella memoria video.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Commenti

Questo metodo genera trame contenenti glifi che rappresentano i caratteri di input. I glifi vengono disegnati come una serie di triangoli.

Non verrà eseguito il rendering dei caratteri nel dispositivo. Per eseguire il rendering dei caratteri, è comunque necessario chiamare [**DrawText**](id3dxfont--drawtext.md) . Tuttavia, se si precaricano i caratteri nella memoria video, **DrawText** utilizzerà in modo sostanziale un minor numero di risorse della CPU.

Questo metodo converte internamente i caratteri in glifi utilizzando la funzione GDI [**GetCharacterPlacement**](/windows/win32/api/wingdi/nf-wingdi-getcharacterplacementa).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXFont](id3dxfont.md)
</dt> </dl>

 

 
