---
description: La struttura MXDC PRINTTICKET DATA T contiene un ticket di stampa di documenti XPS, che contiene le impostazioni della stampante e del processo di stampa, da passare al file di \_ \_ output di Microsoft \_ XPS Document Converter (MXDC) senza alcuna elaborazione.
ms.assetid: d30ba8bb-f429-49d5-963c-b770c3086e97
title: MXDC_PRINTTICKET_DATA_T struttura (Mxdc.h)
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
ms.openlocfilehash: 3cf778781340323a78495f87b1408e1011641797ed52a3565bafe41ca450d551
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118471643"
---
# <a name="mxdc_printticket_data_t-structure"></a>Struttura MXDC \_ PRINTTICKET \_ DATA \_ T

La struttura **MXDC \_ PRINTTICKET \_ DATA \_ T** contiene un ticket di stampa di documenti XPS, che contiene le impostazioni della stampante e del processo di stampa, da passare al file di output di Microsoft XPS Document Converter (MXDC) senza alcuna elaborazione.

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

Ticket di stampa del documento XPS.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa struttura viene aggiunta a una struttura [**MXDC \_ ESCAPE HEADER \_ \_ T**](mxdcescapeheader.md) con il membro **opCode** impostato su **MXDCOP \_ PRINTTICKET \_ FIXED \_ PAGE,** **MXDCOP \_ PRINTTICKET \_ FIXED \_ DOC** o **MXDCOP \_ PRINTTICKET \_ FIXED DOC \_ \_ SEQ** per creare una struttura [**MXDC \_ PRINTTICKET \_ ESCAPE \_ T.**](mxdcprintticketescape.md) La **struttura MXDC \_ PRINTTICKET \_ ESCAPE \_ T** viene quindi passata al parametro *lpszInData* della funzione [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) quando viene chiamata con l'escape [**ESCAPE \_ MXDC.**](mxdc-escape.md) L'effetto è scrivere il ticket di stampa nel file di documento XPS.

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

 

