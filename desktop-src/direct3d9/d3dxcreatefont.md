---
description: Crea un oggetto del tipo di carattere per un dispositivo e un tipo di carattere.
ms.assetid: 3e65dfdc-9608-420c-9672-c38289d13ab1
title: Funzione D3DXCreateFont (D3dx9core. h)
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
ms.openlocfilehash: 488a400928ecc270612a307fbede971e02b43b25
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762191"
---
# <a name="d3dxcreatefont-function"></a>D3DXCreateFont (funzione)

Crea un oggetto del tipo di carattere per un dispositivo e un tipo di carattere.

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

*PDEVICE* \[ in\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Puntatore a un'interfaccia [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , il dispositivo da associare all'oggetto del tipo di carattere.

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

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Set di caratteri del tipo di carattere.

</dd> <dt>

*OutputPrecision* \[ in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Specifica il modo in cui Windows deve tentare di trovare le dimensioni e le caratteristiche dei caratteri desiderate con i tipi di carattere effettivi Usare OUT \_ TT \_ solo \_ per l'istanza, per assicurarsi di ottenere sempre un tipo di carattere TrueType.

</dd> <dt>

*Qualità* \[ in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Specifica il modo in cui Windows deve corrispondere al tipo di carattere desiderato con un tipo di carattere reale. Si applica solo ai tipi di carattere raster e non deve influire sui tipi di carattere TrueType.

</dd> <dt>

*PitchAndFamily* \[ in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Indice di passo e famiglia.

</dd> <dt>

*pFacename* \[ in\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Stringa contenente il nome del carattere tipografico. Se le impostazioni del compilatore richiedono Unicode, il tipo di dati LPCTSTR viene risolto in LPCWSTR. In caso contrario, il tipo di dati String viene risolto in LPCSTR. Vedere la sezione Osservazioni.

</dd> <dt>

*ppFont* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXFONT**](id3dxfont.md)\***

Restituisce un puntatore a un'interfaccia [**ID3DXFont**](id3dxfont.md) , che rappresenta l'oggetto del tipo di carattere creato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è \_ OK. Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OutOfMemory.

## <a name="remarks"></a>Commenti

Per la creazione di un oggetto ID3DXFont è necessario che il dispositivo supporti il colore a 32 bit.

L'impostazione del compilatore determina anche la versione della funzione. Se è definito Unicode, la chiamata di funzione viene risolta in D3DXCreateFontW. In caso contrario, la chiamata di funzione viene risolta in D3DXCreateFontA perché vengono utilizzate le stringhe ANSI.

Per ulteriori informazioni sui parametri dei tipi di carattere, vedere [il tipo di carattere logico](../gdi/creating-a-logical-font.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni per utilizzo generico](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
