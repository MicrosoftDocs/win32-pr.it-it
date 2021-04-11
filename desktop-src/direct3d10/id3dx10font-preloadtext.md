---
description: Caricare il testo formattato nella memoria video per migliorare l'efficienza del rendering nel dispositivo. Questo metodo supporta le stringhe ANSI e Unicode.
ms.assetid: 0e5380fc-7a01-4e09-9c18-22087be56780
title: Metodo ID3DX10Font::P reloadText (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Font.PreloadText
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: c7294fb7e86b3532960a34a15e1118dc33f748f2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235037"
---
# <a name="id3dx10fontpreloadtext-method"></a>ID3DX10Font::P metodo reloadText

Caricare il testo formattato nella memoria video per migliorare l'efficienza del rendering nel dispositivo. Questo metodo supporta le stringhe ANSI e Unicode.

## <a name="syntax"></a>Sintassi


```C++
HRESULT PreloadText(
  [in] LPCSTR pString,
  [in] INT    Count
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pString* \[ in\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

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

Il rendering del testo non verrà eseguito nel dispositivo. ID3DX10Font: è necessario chiamare:D rawText per eseguire il rendering del testo. Tuttavia, precaricando il testo nella memoria video, ID3DX10Font::D rawText utilizzerà in modo sostanziale un minor numero di risorse della CPU.

Questo metodo converte internamente i caratteri in glifi utilizzando la funzione GDI [GetCharacterPlacement](/previous-versions//ms534004(v=vs.85)).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DX10Font](id3dx10font.md)
</dt> <dt>

[Interfacce D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
