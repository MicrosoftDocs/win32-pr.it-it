---
description: Definisce gli attributi di un tipo di carattere.
ms.assetid: 6f456f26-3410-4205-a013-e3c12bf0feb1
title: D3DXFONT_DESC struttura (D3dx9core.h)
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
ms.openlocfilehash: b458d9c3575993dd3d478f886d0b71b3cd5c1af0a53330b0813deafa188ac4c9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119728541"
---
# <a name="d3dxfont_desc-structure"></a>Struttura D3DXFONT \_ DESC

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

Tipo: **[ **INT**](../winprog/windows-data-types.md)**

</dd> <dd>

Altezza, in unità logiche, della cella o del carattere del tipo di carattere.

</dd> <dt>

**Larghezza**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Larghezza, in unità logiche, dei caratteri nel tipo di carattere.

</dd> <dt>

**Weight**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Spessore del tipo di carattere nell'intervallo compreso tra 0 e 1000.

</dd> <dt>

**MipLevels**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Numero di livelli mip richiesti. Se questo valore è zero o D3DX DEFAULT, viene creata una catena \_ mipmap completa. Se il valore è 1, lo spazio della trama viene mappato in modo identico allo spazio dello schermo.

</dd> <dt>

**Corsivo**
</dt> <dd>

Tipo: **[ **BOOL**](../winprog/windows-data-types.md)**

</dd> <dd>

Impostare su **TRUE per** un tipo di carattere corsivo.

</dd> <dt>

**CharSet**
</dt> <dd>

Tipo: **[ **BYTE**](../winprog/windows-data-types.md)**

</dd> <dd>

Set di caratteri.

</dd> <dt>

**OutputPrecision**
</dt> <dd>

Tipo: **[ **BYTE**](../winprog/windows-data-types.md)**

</dd> <dd>

Precisione dell'output. La precisione di output definisce la precisione dell'output che deve corrispondere all'altezza, alla larghezza, all'orientamento dei caratteri, all'escape, all'intonazione e al tipo di carattere richiesti.

</dd> <dt>

**Qualità**
</dt> <dd>

Tipo: **[ **BYTE**](../winprog/windows-data-types.md)**

</dd> <dd>

Qualità dell'output.

</dd> <dt>

**PitchAndFamily**
</dt> <dd>

Tipo: **[ **BYTE**](../winprog/windows-data-types.md)**

</dd> <dd>

Passo e famiglia del tipo di carattere.

</dd> <dt>

**FaceName**
</dt> <dd>

Tipo: **TCHAR**

</dd> <dd>

Stringa o caratteri con terminazione Null che specificano il nome del carattere tipografico del tipo di carattere. La lunghezza della stringa non deve superare i 32 caratteri, incluso il carattere null di terminazione. Se FaceName è una stringa vuota, verrà usato il primo tipo di carattere che corrisponde agli altri attributi specificati. Se le impostazioni del compilatore richiedono Unicode, il tipo di dati TCHAR viene risolto in WCHAR; In caso contrario, il tipo di dati viene risolto in CHAR. Vedere la sezione Osservazioni.

</dd> </dl>

## <a name="remarks"></a>Commenti

L'impostazione del compilatore determina anche il tipo di struttura. Se viene definito Unicode, il tipo di struttura D3DXFONT DESC viene risolto in un D3DXFONT DESCW; in caso contrario, il tipo di struttura viene risolto in una struttura \_ \_ D3DXFONT \_ DESCA.

I valori possibili dei membri precedenti sono specificati nella struttura GDI [**LOGFONT.**](/windows/win32/api/wingdi/ns-wingdi-logfonta)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx9core.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[**GetDesc**](id3dxfont--getdesc.md)
</dt> </dl>

 

 
