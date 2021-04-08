---
description: La \_ struttura MXDC S0PAGE \_ data \_ T include una pagina di documento XPS da passare al file di output di Microsoft XPS Document Converter (MXDC) senza alcuna elaborazione.
ms.assetid: 3dc8e0b9-cf63-4345-93d2-3b60dac42546
title: Struttura MXDC_S0PAGE_DATA_T (MXDC. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_S0PAGE_DATA_T
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: 2da9df454b8741f2203072fd25856118407ef5c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757742"
---
# <a name="mxdc_s0page_data_t-structure"></a>MXDC \_ S0PAGE \_ data \_ T Structure

La struttura **MXDC \_ S0PAGE \_ data \_ T** include una pagina di documento XPS da passare al file di output di Microsoft XPS Document Converter (MXDC) senza alcuna elaborazione.

## <a name="syntax"></a>Sintassi


```C++
typedef struct tagMxdcS0PageData {
  ULONG dwSize;
  BYTE  bData[1];
} MXDC_S0PAGE_DATA_T, *P_MXDC_S0PAGE_DATA_T;
```



## <a name="members"></a>Members

<dl> <dt>

**dwSize**
</dt> <dd>

Dimensioni del buffer di output, **bdata**.

</dd> <dt>

**bData**
</dt> <dd>

Pagina del documento XPS.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa struttura viene aggiunta a una struttura [**MXDC \_ dell' \_ intestazione \_ di escape t**](mxdcescapeheader.md) (il cui **codice operativo** è impostato su MXDCOP \_ set \_ S0PAGE) per creare una struttura [**MXDC \_ S0PAGE \_ PassThrough \_ escape \_ t**](mxdcs0pagepassthroughescape.md) . Tale struttura viene quindi passata al parametro *lpszInData* della funzione [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) quando viene chiamata con l' [**\_ escape MXDC**](mxdc-escape.md) come escape. Il risultato è che il MXDC passa la pagina all'output senza elaborarla.

La chiamata a [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) deve essere compresa tra una chiamata a [**Startpage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) e una chiamata a [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage).

L'applicazione chiamante è responsabile della convalida del codice XML della pagina del documento XPS.

Il consumo di flussi è più efficiente se si chiama [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) con **MXDCOP \_ impostare la \_ \_ risorsa S0PAGE** come **OpCode** per ogni risorsa nella pagina prima di chiamarla con **MXDCOP \_ set \_ S0PAGE**.

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

 

