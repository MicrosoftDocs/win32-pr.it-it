---
description: Crea un oggetto del tipo di carattere per un dispositivo e un tipo di carattere. Nota invece di usare questa funzione, è consigliabile usare DirectWrite e la libreria DirectXTK, SpriteFont Class.
ms.assetid: a0dd02f1-c512-46d3-9e83-a785ac3ad7ee
title: Funzione D3DX10CreateFont (D3DX10Core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateFont
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: d6e5966e50c9c997085d35854868a2a7dd0455c7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322943"
---
# <a name="d3dx10createfont-function"></a>D3DX10CreateFont (funzione)

Crea un oggetto del tipo di carattere per un dispositivo e un tipo di carattere.

> [!Note]  
> Invece di usare questa funzione, è consigliabile usare [DirectWrite](../directwrite/direct-write-portal.md) e la libreria [DirectXTK](https://github.com/Microsoft/DirectXTK) , la classe **SpriteFont** .

 

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DX10CreateFont(
  _In_  ID3D10Device *pDevice,
  _In_  INT          Height,
  _In_  UINT         Width,
  _In_  UINT         Weight,
  _In_  UINT         MipLevels,
  _In_  BOOL         Italic,
  _In_  UINT         CharSet,
  _In_  UINT         OutputPrecision,
  _In_  UINT         Quality,
  _In_  UINT         PitchAndFamily,
  _In_  LPCTSTR      pFaceName,
  _Out_ LPD3DX10FONT *ppFont
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PDEVICE* \[ in\]
</dt> <dd>

Tipo: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***

Puntatore a un'interfaccia ID3D10Device, il dispositivo da associare all'oggetto del tipo di carattere.

</dd> <dt>

*Altezza* \[ in\]
</dt> <dd>

Tipo: **[ **int**](../winprog/windows-data-types.md)**

Altezza dei caratteri nelle unità logiche.

</dd> <dt>

*Larghezza* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Larghezza dei caratteri nelle unità logiche.

</dd> <dt>

*Peso* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Spessore carattere. Un esempio è grassetto.

</dd> <dt>

*MipLevels* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Il numero di livelli di mipmap.

</dd> <dt>

*Corsivo* \[ in\]
</dt> <dd>

Tipo: **[ **bool**](../winprog/windows-data-types.md)**

True per il tipo di carattere corsivo, false in caso contrario.

</dd> <dt>

*Set di caratteri* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Set di caratteri del tipo di carattere.

</dd> <dt>

*OutputPrecision* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Specifica il modo in cui Windows deve tentare di trovare le dimensioni e le caratteristiche dei caratteri desiderate con i tipi di carattere effettivi Usare OUT \_ TT \_ solo \_ per l'istanza, per assicurarsi di ottenere sempre un tipo di carattere TrueType.

</dd> <dt>

*Qualità* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Specifica il modo in cui Windows deve corrispondere al tipo di carattere desiderato con un tipo di carattere reale. Si applica solo ai tipi di carattere raster e non deve influire sui tipi di carattere TrueType.

</dd> <dt>

*PitchAndFamily* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Indice di passo e famiglia.

</dd> <dt>

*pFaceName* \[ in\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Stringa contenente il nome del carattere tipografico. Se le impostazioni del compilatore richiedono Unicode, il tipo di dati LPCTSTR viene risolto in LPCWSTR. In caso contrario, il tipo di dati viene risolto in LPCSTR. Vedere la sezione Osservazioni.

</dd> <dt>

*ppFont* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DX10FONT**](id3dx10font.md)\***

Restituisce un puntatore a un'interfaccia ID3DX10Font, che rappresenta l'oggetto del tipo di carattere creato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è \_ OK. Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OutOfMemory.

## <a name="remarks"></a>Commenti

L'impostazione del compilatore determina anche la versione della funzione. Se è definito Unicode, la chiamata di funzione viene risolta in D3DXCreateFontW. In caso contrario, la chiamata di funzione viene risolta in D3DXCreateFontA perché vengono utilizzate le stringhe ANSI.

Per ulteriori informazioni sui parametri dei tipi di carattere, vedere [il tipo di carattere logico](/previous-versions//ms533985(v=vs.85)).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10Core. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni per utilizzo generico](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
