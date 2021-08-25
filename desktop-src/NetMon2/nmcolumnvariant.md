---
description: Fornisce una riga nel riquadro superiore del Visualizzatore eventi che funge da contenitore per tutti i possibili dati inseriti in una colonna.
ms.assetid: 2ad32c23-5dbe-46be-b0cc-ccf7a6fe8ec3
title: Struttura NMCOLUMNVARIANT (Netmon.h)
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
ms.openlocfilehash: 814b419909591e45c07b3ed499072ec4871cdeb1f4c5a355277a03d0623d264c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119890023"
---
# <a name="nmcolumnvariant-structure"></a>Struttura NMCOLUMNVARIANT

La **struttura NMCOLUMNVARIANT** fornisce una riga nel riquadro superiore del Visualizzatore eventi che funge da contenitore per tutti i possibili dati inseriti in una colonna.

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

Valore del tipo [**di enumerazione NMCOLUMNTYPE.**](nmcolumntype.md)

</dd> <dt>

**Valore**
</dt> <dd> <dl> <dt>

**Uint8Val**
</dt> <dd>

Valore intero senza segno a 8 bit.

</dd> <dt>

**Sint8Val**
</dt> <dd>

Valore intero con segno a 8 bit.

</dd> <dt>

**Uint16Val**
</dt> <dd>

Valore intero senza segno a 16 bit.

</dd> <dt>

**Sint16Val**
</dt> <dd>

Valore intero con segno a 16 bit.

</dd> <dt>

**Uint32Val**
</dt> <dd>

Valore integer senza segno a 32 bit.

</dd> <dt>

**Sint32Val**
</dt> <dd>

Valore intero con segno a 32 bit.

</dd> <dt>

**Float64Val**
</dt> <dd>

Valore float a 64 bit.

</dd> <dt>

**FrameVal**
</dt> <dd>

Numero di fotogramma.

</dd> <dt>

**YesNoVal**
</dt> <dd>

Visualizza Sì o No.

</dd> <dt>

**OnOffVal**
</dt> <dd>

Visualizza On o Off.

</dd> <dt>

**TrueFalseVal**
</dt> <dd>

Visualizza True o False.

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

Ora della variante. Usare **VariantTimetoSystemTime** per eseguire la conversione all'ora di sistema.

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
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**NMCOLUMNTYPE**](nmcolumntype.md)
</dt> </dl>

 

 




