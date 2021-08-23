---
description: La struttura MXDC PRINTTICKET ESCAPE T è una struttura \_ \_ \_ MXDC ESCAPE HEADER T concatenata a una \_ \_ struttura \_ MXDC \_ PRINTTICKET \_ DATA \_ T.
ms.assetid: 79b4f830-3e3f-4c6f-9e61-98e8bf6e2824
title: MXDC_PRINTTICKET_ESCAPE_T struttura (Mxdc.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_PRINTTICKET_ESCAPE_T
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: eca1858bbbf09d4e3c3af8a91f9bb91550eddfd703f59e86112e65c56a43d553
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119099065"
---
# <a name="mxdc_printticket_escape_t-structure"></a>Struttura MXDC \_ PRINTTICKET \_ ESCAPE \_ T

La **struttura MXDC \_ PRINTTICKET \_ ESCAPE \_ T** è una struttura [**MXDC ESCAPE HEADER \_ \_ \_ T**](mxdcescapeheader.md) concatenata a una [**struttura MXDC \_ PRINTTICKET \_ DATA \_ T.**](mxdcprintticketpassthrough.md)

## <a name="syntax"></a>Sintassi


```C++
typedef struct tagMxdcPrintTicketEscape {
  MXDC_ESCAPE_HEADER_T    mxdcEscape;
  MXDC_PRINTTICKET_DATA_T printTicketData;
} MXDC_PRINTTICKET_ESCAPE_T, *P_MXDC_PRINTTICKET_ESCAPE_T;
```



## <a name="members"></a>Members

<dl> <dt>

**mxdcEscape**
</dt> <dd>

Struttura [**MXDC \_ ESCAPE HEADER \_ \_ T**](mxdcescapeheader.md) con il membro **opCode** impostato su MXDCOP \_ PRINTTICKET \_ FIXED \_ PAGE, MXDCOP \_ PRINTTICKET \_ FIXED DOC o \_ MXDCOP \_ PRINTTICKET \_ FIXED DOC \_ \_ SEQ.

</dd> <dt>

**printTicketData**
</dt> <dd>

Struttura [**MXDC \_ PRINTTICKET \_ DATA \_ T**](mxdcprintticketpassthrough.md) contenente il ticket di stampa.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa struttura viene passata nel parametro *lpszInData* della funzione [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) quando tale funzione viene chiamata con l'escape [**ESCAPE \_ MXDC**](mxdc-escape.md) e il membro **opCode** della struttura [**MXDC ESCAPE HEADER \_ \_ \_ T**](mxdcescapeheader.md) è **MXDCOP \_ PRINTTICKET \_ FIXED \_ PAGE,** **MXDCOP \_ PRINTTICKET \_ FIXED \_ DOC** o **MXDCOP \_ PRINTTICKET \_ FIXED DOC \_ \_ SEQ.** Il risultato è scrivere il ticket di stampa nel file di documento XPS.

Allocare memoria per l'escape come illustrato di seguito, impostare i campi in base alle esigenze e quindi chiamare [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape).


```C++
// Compute size of buffer required adding the
//  size of the escape structure to the size
//  of the resource data buffer.
SIZE_T iTotalDataSize = sizeof(MXDC_PRINTTICKET_ESCAPE_T) + 
                        iS0PageDataSize - 1;

// Allocate the memory buffer.
P_MXDC_PRINTTICKET_ESCAPE_T pS0PageEscapeData = 
                        (P_MXDC_PRINTTICKET_ESCAPE_T)HeapAlloc(
                            GetProcessHeap(),
                            0,
                            iTotalDataSize);
```



Se **opCode è** impostato su **MXDCOP \_ PRINTTICKET \_ FIXED \_ PAGE,** la chiamata a [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) deve verificarsi tra una chiamata a [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) e una chiamata a [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage). Se **opCode** è impostato su **MXDCOP \_ PRINTTICKET \_ FIXED \_ DOC** o **MXDCOP \_ PRINTTICKET \_ FIXED DOC \_ \_ SEQ,** la chiamata a **ExtEscape** deve verificarsi tra una chiamata a [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) e una chiamata a [**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                    |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                              |
| Intestazione<br/>                   | <dl> <dt>Mxdc.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Strutture dell'API Spooler di stampa](printing-and-print-spooler-structures.md)
</dt> <dt>

[Funzioni di escape della stampante GDI](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))
</dt> <dt>

[**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)
</dt> <dt>

[**MXDC \_ ESCAPE**](mxdc-escape.md)
</dt> </dl>

 

