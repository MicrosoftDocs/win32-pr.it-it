---
description: Fornisce una riga nel riquadro superiore del Visualizzatore eventi che funge da contenitore per tutti i dati possibili inseriti in una colonna.
ms.assetid: 2ad32c23-5dbe-46be-b0cc-ccf7a6fe8ec3
title: Struttura NMCOLUMNVARIANT (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NMCOLUMNVARIANT
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: e9f70d2d1a0caf63411fcd2b44d5ed8bdcbecd00
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318967"
---
# <a name="nmcolumnvariant-structure"></a>Struttura NMCOLUMNVARIANT

La struttura **NMCOLUMNVARIANT** fornisce una riga nel riquadro superiore del Visualizzatore eventi che funge da contenitore per tutti i dati possibili inseriti in una colonna.

## <a name="syntax"></a>Sintassi


```C++
typedef struct {
  NMCOLUMNTYPE Type;
  union {
    BYTE        Uint8Val;
    char        Sint8Val;
    WORD        Uint16Val;
    short       Sint16Val;
    DWORD       Uint32Val;
    LONG        Sint32Val;
    DOUBLE      Float64Val;
    DWORD       FrameVal;
    BOOL        YesNoVal;
    BOOL        OnOffVal;
    BOOL        TrueFalseVal;
    BYTE        MACAddrVal[MAC_ADDRESS_SIZE];
    IPX_ADDRESS IPXAddrVal;
    DWORD       IPAddrVal;
    DOUBLE      VarTimeVal;
    LPSTR       pStringVal;
  } Value;
} NMCOLUMNVARIANT;
```



## <a name="members"></a>Members

<dl> <dt>

**Tipo**
</dt> <dd>

Valore del tipo di enumerazione [**NMCOLUMNTYPE**](nmcolumntype.md) .

</dd> <dt>

**Valore**
</dt> <dd> <dl> <dt>

**Uint8Val**
</dt> <dd>

valore Unsigned Integer a 8 bit.

</dd> <dt>

**Sint8Val**
</dt> <dd>

valore intero con segno a 8 bit.

</dd> <dt>

**Uint16Val**
</dt> <dd>

valore Unsigned Integer a 16 bit.

</dd> <dt>

**Sint16Val**
</dt> <dd>

valore intero con segno a 16 bit.

</dd> <dt>

**Uint32Val**
</dt> <dd>

valore Unsigned Integer a 32 bit.

</dd> <dt>

**Sint32Val**
</dt> <dd>

valore intero con segno a 32 bit.

</dd> <dt>

**Float64Val**
</dt> <dd>

valore float a 64 bit.

</dd> <dt>

**FrameVal**
</dt> <dd>

Numero di frame.

</dd> <dt>

**YesNoVal**
</dt> <dd>

Viene visualizzato Sì o no.

</dd> <dt>

**OnOffVal**
</dt> <dd>

Visualizza on o off.

</dd> <dt>

**TrueFalseVal**
</dt> <dd>

Visualizza true o false.

</dd> <dt>

**MACAddrVal**
</dt> <dd>

Indirizzo MAC.

</dd> <dt>

**IPXAddrVal**
</dt> <dd>

Indirizzo IPX.

</dd> <dt>

**IPAddrVal**
</dt> <dd>

Un indirizzo IP.

</dd> <dt>

**VarTimeVal**
</dt> <dd>

Tempo Variant. Usare **VariantTimetoSystemTime** per convertire l'ora di sistema.

</dd> <dt>

**pStringVal**
</dt> <dd>

Puntatore a una stringa.

</dd> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**NMCOLUMNTYPE**](nmcolumntype.md)
</dt> </dl>

 

 




