---
description: Definisce gli attributi di un tipo di carattere.
ms.assetid: 6f456f26-3410-4205-a013-e3c12bf0feb1
title: Struttura D3DXFONT_DESC (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFONT_DESC
api_type:
- HeaderDef
api_location:
- d3dx9core.h
ms.openlocfilehash: d7c142787e4e4fac5be53763a3c19fd86a27efd9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322687"
---
# <a name="d3dxfont_desc-structure"></a>\_Struttura D3DXFONT DESC

Definisce gli attributi di un tipo di carattere.

## <a name="syntax"></a>Sintassi


```C++
typedef struct D3DXFONT_DESC {
  INT   Height;
  UINT  Width;
  UINT  Weight;
  UINT  MipLevels;
  BOOL  Italic;
  BYTE  CharSet;
  BYTE  OutputPrecision;
  BYTE  Quality;
  BYTE  PitchAndFamily;
  TCHAR FaceName;
} D3DXFONT_DESC, *LPD3DXFONT_DESC;
```



## <a name="members"></a>Members

<dl> <dt>

**Altezza**
</dt> <dd>

Tipo: **[ **int**](../winprog/windows-data-types.md)**

</dd> <dd>

Altezza, in unità logiche, della cella del carattere o del carattere del tipo di carattere.

</dd> <dt>

**Larghezza**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Larghezza, in unità logiche, di caratteri nel tipo di carattere.

</dd> <dt>

**Weight**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Spessore del tipo di carattere nell'intervallo compreso tra 0 e 1000.

</dd> <dt>

**MipLevels**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Numero di livelli MIP richiesti. Se questo valore è zero o D3DX \_ default, viene creata una catena mipmap completa. Se il valore è 1, lo spazio della trama viene mappato in modo identico allo spazio dello schermo.

</dd> <dt>

**Corsivo**
</dt> <dd>

Tipo: **[ **bool**](../winprog/windows-data-types.md)**

</dd> <dd>

Impostare su **true** per un tipo di carattere corsivo.

</dd> <dt>

**CharSet**
</dt> <dd>

Tipo: **[ **byte**](../winprog/windows-data-types.md)**

</dd> <dd>

Set di caratteri.

</dd> <dt>

**OutputPrecision**
</dt> <dd>

Tipo: **[ **byte**](../winprog/windows-data-types.md)**

</dd> <dd>

Precisione dell'output. La precisione di output definisce la distanza con cui l'output deve corrispondere all'altezza, alla larghezza, all'orientamento dei caratteri, alla rotazione, al passo e al tipo di carattere richiesti.

</dd> <dt>

**Qualità**
</dt> <dd>

Tipo: **[ **byte**](../winprog/windows-data-types.md)**

</dd> <dd>

Qualità dell'output.

</dd> <dt>

**PitchAndFamily**
</dt> <dd>

Tipo: **[ **byte**](../winprog/windows-data-types.md)**

</dd> <dd>

Pitch e Family del tipo di carattere.

</dd> <dt>

**Contemplato**
</dt> <dd>

Tipo: **TCHAR**

</dd> <dd>

Stringa o caratteri con terminazione null che specifica il nome tipografico del tipo di carattere. La lunghezza della stringa non deve superare i 32 caratteri, incluso il carattere null di terminazione. Se FaceName è una stringa vuota, verrà utilizzato il primo carattere corrispondente agli altri attributi specificati. Se le impostazioni del compilatore richiedono Unicode, il tipo di dati TCHAR viene risolto in WCHAR; in caso contrario, il tipo di dati viene risolto in CHAR. Vedere la sezione Osservazioni.

</dd> </dl>

## <a name="remarks"></a>Commenti

L'impostazione del compilatore determina anche il tipo di struttura. Se è definito Unicode, il \_ tipo di struttura D3DXFONT desc viene risolto in un \_ DESCW D3DXFONT; in caso contrario, il tipo di struttura viene risolto in un D3DXFONT \_ Desca.

I valori possibili dei membri precedenti sono forniti nella struttura GDI [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx9core. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[**Getdesc**](id3dxfont--getdesc.md)
</dt> </dl>

 

 
