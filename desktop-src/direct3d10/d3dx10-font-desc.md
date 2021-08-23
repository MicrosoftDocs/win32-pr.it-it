---
description: Definisce gli attributi del tipo di carattere.
ms.assetid: 66e8a320-2b83-4766-a9a7-5571ee6c9f2a
title: D3DX10_FONT_DESC struttura (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_FONT_DESC
api_type:
- HeaderDef
api_location:
- D3DX10.h
ms.openlocfilehash: f3ee6dea032475eb94a723229751d9523c12d118f7319da8f0296cc8c8c42a2c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119634951"
---
# <a name="d3dx10_font_desc-structure"></a>Struttura \_ DESC FONT D3DX10 \_

Definisce gli attributi del tipo di carattere.

## <a name="syntax"></a>Sintassi


```C++
typedef struct D3DX10_FONT_DESC {
  INT   Height;
  UINT  Width;
  UINT  Weight;
  UINT  MipLevels;
  BOOL  Italic;
  BYTE  CharSet;
  BYTE  OutputPrecision;
  BYTE  Quality;
  BYTE  PitchAndFamily;
  TCHAR FaceName[LF_FACESIZE];
} D3DX10_FONT_DESC, *LPD3DX10_FONT_DESC;
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

Spessore del tipo di carattere compreso nell'intervallo compreso tra 0 e 1000.

</dd> <dt>

**MipLevels**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Numero di livelli mipmap richiesti. Se questo valore è zero o D3DX DEFAULT, viene creata una catena \_ mipmap completa. Se il valore è 1, lo spazio trame viene mappato in modo identico allo spazio dello schermo.

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

Precisione dell'output. La precisione dell'output definisce la precisione dell'output che deve corrispondere all'altezza, alla larghezza, all'orientamento dei caratteri, all'escape, all'altezza e al tipo di carattere richiesti.

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

Pitch e famiglia del tipo di carattere.

</dd> <dt>

**FaceName \[ LF \_ FACESIZE\]**
</dt> <dd>

Tipo: **TCHAR**

</dd> <dd>

Stringa con terminazione NULL che specifica il nome del carattere tipografico del tipo di carattere. La lunghezza della stringa non deve superare i 32 caratteri, incluso il carattere **NULL di** terminazione. Se FaceName è una stringa vuota, verrà usato il primo tipo di carattere che corrisponde agli altri attributi specificati. Se le impostazioni del compilatore richiedono Unicode, il tipo di dati TCHAR viene risolto in WCHAR. In caso contrario, il tipo di dati viene risolto in CHAR. Vedere la sezione Osservazioni.

</dd> </dl>

## <a name="remarks"></a>Commenti

L'impostazione del compilatore determina anche il tipo di struttura. Se è definito Unicode, il tipo di struttura D3DX10 FONT DESC viene risolto in un D3DX10 FONT DESCW; in caso contrario, il tipo di struttura viene risolto in \_ \_ un \_ \_ D3DX10 \_ FONT \_ DESCA.

I valori possibili dei membri precedenti sono indicati nella struttura [GDI LOGFONT.](/previous-versions//ms533931(v=vs.85))

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3DX10.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture D3DX](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
