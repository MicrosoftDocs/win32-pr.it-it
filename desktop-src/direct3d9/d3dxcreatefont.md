---
description: Crea un oggetto tipo di carattere per un dispositivo e un tipo di carattere.
ms.assetid: 3e65dfdc-9608-420c-9672-c38289d13ab1
title: Funzione D3DXCreateFont (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateFont
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d9bac71e89657f4df176a1ee15e2dca0cda6e4a25b8c47560adc5cf26c982383
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118526155"
---
# <a name="d3dxcreatefont-function"></a>Funzione D3DXCreateFont

Crea un oggetto tipo di carattere per un dispositivo e un tipo di carattere.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXCreateFont(
  _In_  LPDIRECT3DDEVICE9 pDevice,
  _In_  INT               Height,
  _In_  UINT              Width,
  _In_  UINT              Weight,
  _In_  UINT              MipLevels,
  _In_  BOOL              Italic,
  _In_  DWORD             CharSet,
  _In_  DWORD             OutputPrecision,
  _In_  DWORD             Quality,
  _In_  DWORD             PitchAndFamily,
  _In_  LPCTSTR           pFacename,
  _Out_ LPD3DXFONT        *ppFont
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pDevice* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Puntatore a [**un'interfaccia IDirect3DDevice9,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) il dispositivo da associare all'oggetto tipo di carattere.

</dd> <dt>

*Altezza* \[ Pollici\]
</dt> <dd>

Tipo: **[ **INT**](../winprog/windows-data-types.md)**

Altezza dei caratteri in unità logiche.

</dd> <dt>

*Larghezza* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Larghezza dei caratteri in unità logiche.

</dd> <dt>

*Peso* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Spessore carattere tipografico. Un esempio è il grassetto.

</dd> <dt>

*MipLevels* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Numero di livelli mipmap.

</dd> <dt>

*Corsivo* \[ Pollici\]
</dt> <dd>

Tipo: **[ **BOOL**](../winprog/windows-data-types.md)**

True per il tipo di carattere corsivo; in caso contrario, false.

</dd> <dt>

*Set di caratteri* \[ Pollici\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Set di caratteri del tipo di carattere.

</dd> <dt>

*OutputPrecision* \[ Pollici\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Specifica in che modo Windows deve tentare di trovare una corrispondenza tra le dimensioni e le caratteristiche dei caratteri desiderate con i tipi di carattere effettivi. Usare OUT \_ TT ONLY PRECIS, ad esempio, per assicurarsi di ottenere \_ sempre un tipo di carattere \_ TrueType.

</dd> <dt>

*Qualità* \[ Pollici\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Specifica in che modo Windows deve corrispondere al tipo di carattere desiderato con un tipo di carattere reale. Si applica solo ai tipi di carattere raster e non deve influire sui tipi di carattere TrueType.

</dd> <dt>

*PitchAndFamily* \[ Pollici\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Indice di passo e famiglia.

</dd> <dt>

*pFacename* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Stringa contenente il nome del carattere tipografico. Se le impostazioni del compilatore richiedono Unicode, il tipo di dati LPCTSTR viene risolto in LPCWSTR. In caso contrario, il tipo di dati string viene risolto in LPCSTR. Vedere la sezione Osservazioni.

</dd> <dt>

*ppFont* \[ Cambio\]
</dt> <dd>

Tipo: **[ **LPD3DXFONT**](id3dxfont.md)\***

Restituisce un puntatore a [**un'interfaccia ID3DXFont**](id3dxfont.md) che rappresenta l'oggetto tipo di carattere creato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è S \_ OK. Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Commenti

La creazione di un oggetto ID3DXFont richiede che il dispositivo supporti il colore a 32 bit.

L'impostazione del compilatore determina anche la versione della funzione. Se è definito Unicode, la chiamata di funzione viene risolta in D3DXCreateFontW. In caso contrario, la chiamata di funzione viene risolta in D3DXCreateFontA perché vengono usate stringhe ANSI.

Per altre informazioni sui parametri dei tipi di carattere, vedere [Tipo di carattere logico.](../gdi/creating-a-logical-font.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Per utilizzo generico funzioni](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
