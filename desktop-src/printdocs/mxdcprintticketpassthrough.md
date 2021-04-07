---
description: La \_ \_ struttura di data T PRINTTICKET MXDC contiene \_ un ticket di stampa del documento XPS, che contiene le impostazioni della stampante e del processo di stampa, da passare al file di output Microsoft XPS Document Converter (MXDC) senza alcuna elaborazione.
ms.assetid: d30ba8bb-f429-49d5-963c-b770c3086e97
title: Struttura MXDC_PRINTTICKET_DATA_T (MXDC. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_PRINTTICKET_DATA_T
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: 94308527437316dda75fc5a50a6a7829e9315c3b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881605"
---
# <a name="mxdc_printticket_data_t-structure"></a>\_ \_ Struttura T di dati PRINTTICKET MXDC \_

La struttura di **\_ \_ data \_ T PRINTTICKET MXDC** contiene un ticket di stampa del documento XPS, che contiene le impostazioni della stampante e del processo di stampa, da passare al file di output Microsoft XPS Document Converter (MXDC) senza alcuna elaborazione.

## <a name="syntax"></a>Sintassi


```C++
typedef struct tagMxdcPrintTicketData {
  DWORD dwDataSize;
  BYTE  bData[1];
} MXDC_PRINTTICKET_DATA_T, *P_MXDC_PRINTTICKET_DATA_T;
```



## <a name="members"></a>Members

<dl> <dt>

**dwDataSize**
</dt> <dd>

Dimensioni in byte del ticket di stampa.

</dd> <dt>

**bData**
</dt> <dd>

Il ticket di stampa del documento XPS.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa struttura viene aggiunta a una struttura [**MXDC \_ di \_ intestazione \_ di escape T**](mxdcescapeheader.md) con il membro **OpCode** impostato su **MXDCOP \_ PrintTicket \_ fixed \_ Page**, **MXDCOP \_ PrintTicket \_ fixed \_ doc** o **MXDCOP \_ PrintTicket \_ fixed \_ doc \_ Seq** per creare una struttura [**MXDC \_ PrintTicket di \_ escape \_ t**](mxdcprintticketescape.md) . La **struttura \_ \_ \_ T di escape PRINTTICKET MXDC** viene quindi passata al parametro *lpszInData* della funzione [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) quando viene chiamata con l'escape di [**escape \_ MXDC**](mxdc-escape.md) . L'effetto è quello di scrivere il ticket di stampa nel file di documento XPS.

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

 

