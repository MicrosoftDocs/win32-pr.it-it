---
description: Carica il testo formattato nella memoria video per migliorare l'efficienza del rendering nel dispositivo. Questo metodo supporta le stringhe ANSI e Unicode.
ms.assetid: f2a4e9f5-87c5-46c0-965d-ce1535a6921d
title: Metodo ID3DXFont::P reloadText (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont.PreloadText
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 958979e3008cf9ae0b79e2de3591635187df0f12
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104132402"
---
# <a name="id3dxfontpreloadtext-method"></a>ID3DXFont::P metodo reloadText

Carica il testo formattato nella memoria video per migliorare l'efficienza del rendering nel dispositivo. Questo metodo supporta le stringhe ANSI e Unicode.

## <a name="syntax"></a>Sintassi


```C++
HRESULT PreloadText(
  [in] LPCTSTR *pString,
  [in] INT     Count
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pString* \[ in\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)\***

Puntatore a una stringa di caratteri da caricare nella memoria video. Se le impostazioni del compilatore richiedono Unicode, il tipo di dati LPCTSTR viene risolto in LPCWSTR; in caso contrario, il tipo di dati viene risolto in LPCSTR. Vedere la sezione Osservazioni.

</dd> <dt>

*Numero* \[ di in\]
</dt> <dd>

Tipo: **[ **int**](../winprog/windows-data-types.md)**

Numero di caratteri nella stringa di testo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Commenti

L'impostazione del compilatore determina anche la versione della funzione. Se è definito Unicode, la chiamata di funzione viene risolta in PreloadTextW. In caso contrario, la chiamata di funzione viene risolta in PreloadTextA perché vengono utilizzate le stringhe ANSI.

Questo metodo genera trame che contengono glifi che rappresentano il testo di input. I glifi vengono disegnati come una serie di triangoli.

Il rendering del testo non verrà eseguito nel dispositivo. Per eseguire il rendering del testo, è necessario che l'oggetto [**DrawText**](id3dxfont--drawtext.md) venga ancora chiamato. Tuttavia, precaricando il testo nella memoria video, **DrawText** utilizzerà in modo sostanziale un minor numero di risorse della CPU.

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

 

 
