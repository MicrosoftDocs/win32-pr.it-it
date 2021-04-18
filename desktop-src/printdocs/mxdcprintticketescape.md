---
description: La struttura MXDC di \_ \_ escape PrintTicket \_ t è una \_ struttura di intestazione di escape MXDC \_ \_ t concatenata a una struttura di \_ \_ data t PrintTicket MXDC \_ .
ms.assetid: 79b4f830-3e3f-4c6f-9e61-98e8bf6e2824
title: Struttura MXDC_PRINTTICKET_ESCAPE_T (MXDC. h)
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
ms.openlocfilehash: 158ee2038c83b74077d00e6922b2c7050b76bc62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318360"
---
# <a name="mxdc_printticket_escape_t-structure"></a>\_ \_ Struttura T di escape PRINTTICKET MXDC \_

La struttura **MXDC di \_ \_ escape PrintTicket \_ t** è una struttura di [**intestazione di escape MXDC \_ \_ \_ t**](mxdcescapeheader.md) concatenata a una struttura di [**\_ \_ data \_ t PrintTicket MXDC**](mxdcprintticketpassthrough.md) .

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

Una struttura [**MXDC dell' \_ intestazione di escape \_ \_ T**](mxdcescapeheader.md) con il membro **OpCode** impostato \_ sulla \_ pagina fissa MXDCOP PrintTicket \_ , MXDCOP \_ PrintTicket \_ fixed \_ doc o MXDCOP \_ PrintTicket \_ fixed \_ doc \_ Seq.

</dd> <dt>

**printTicketData**
</dt> <dd>

Struttura [**di \_ \_ data \_ T PRINTTICKET MXDC**](mxdcprintticketpassthrough.md) contenente il ticket di stampa.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa struttura viene passata nel parametro *lpszInData* della funzione [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) quando tale funzione viene chiamata con il escape di [**\_ escape MXDC**](mxdc-escape.md) e il membro **OpCode** della struttura dell' [**\_ \_ intestazione \_ di escape MXDC**](mxdcescapeheader.md) è **MXDCOP \_ \_ \_ pagina fissa** dell'oggetto, **MXDCOP \_ PrintTicket \_ fixed \_ doc** o **MXDCOP \_ PrintTicket \_ fixed \_ doc \_ Seq**. Il risultato è la scrittura del ticket di stampa nel file di documento XPS.

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



Se il **codice operativo** è impostato **su MXDCOP \_ PRINTTICKET \_ fixed \_ Page**, la chiamata a [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) deve essere eseguita tra una chiamata a [**Startpage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) e una chiamata a [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage). Se il **codice operativo** è impostato **su \_ MXDCOP \_ PrintTicket fixed \_ doc** o **MXDCOP \_ PrintTicket \_ fixed \_ doc \_ Seq**, la chiamata a **ExtEscape** deve essere eseguita tra una chiamata a [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) e una chiamata a [**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                    |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                              |
| Intestazione<br/>                   | <dl> <dt>MXDC. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Strutture dell'API spooler di stampa](printing-and-print-spooler-structures.md)
</dt> <dt>

[Funzioni di escape della stampante GDI](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))
</dt> <dt>

[**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)
</dt> <dt>

[**\_escape MXDC**](mxdc-escape.md)
</dt> </dl>

 

