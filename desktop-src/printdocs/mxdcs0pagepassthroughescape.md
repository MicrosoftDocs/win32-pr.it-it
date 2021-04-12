---
description: La struttura MXDC \_ S0PAGE \_ PassThrough \_ escape \_ t è una \_ \_ \_ struttura di escape t MXDC concatenata a una struttura MXDC \_ S0PAGE \_ data \_ t.
ms.assetid: 949c1ed4-92d5-4c11-a7da-f9d94bafe3f8
title: Struttura MXDC_S0PAGE_PASSTHROUGH_ESCAPE_T (MXDC. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_S0PAGE_PASSTHROUGH_ESCAPE_T
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: 7c1a8370d2cfa1ada9fda2d2d99b9fe500b79d31
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346486"
---
# <a name="mxdc_s0page_passthrough_escape_t-structure"></a>\_Struttura MXDC S0PAGE \_ PassThrough \_ escape \_ T

La struttura **MXDC \_ S0PAGE \_ PassThrough \_ escape \_ t** è una struttura di [**\_ escape \_ \_ t MXDC**](mxdcescapeheader.md) concatenata a una struttura [**MXDC \_ S0PAGE \_ data \_ t**](mxdcs0pagedata.md) .

## <a name="syntax"></a>Sintassi


```C++
typedef struct tagMxdcS0PagePassthroughEscape {
  MXDC_ESCAPE_HEADER_T mxdcEscape;
  MXDC_S0PAGE_DATA_T   xpsS0PageData;
} MXDC_S0PAGE_PASSTHROUGH_ESCAPE_T, *P_MXDC_S0PAGE_PASSTHROUGH_ESCAPE_T;
```



## <a name="members"></a>Members

<dl> <dt>

**mxdcEscape**
</dt> <dd>

Una struttura [**MXDC dell' \_ intestazione di escape \_ \_ T**](mxdcescapeheader.md) con il relativo membro **OpCode** impostato su **MXDCOP \_ impostare \_ S0PAGE**.

</dd> <dt>

**xpsS0PageData**
</dt> <dd>

Struttura [**MxdcS0PageData**](mxdcs0pagedata.md) che rappresenta una pagina XPS-Document.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa struttura viene passata nel parametro *lpszInData* della funzione [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) quando viene chiamata con l'escape di [**\_ escape MXDC**](mxdc-escape.md) e il membro **OpCode** della struttura dell' [**intestazione di \_ escape \_ MXDC \_ T**](mxdcescapeheader.md) è **MXDCOP \_ set \_ S0PAGE**. Il risultato è che il convertitore di documenti XML Microsoft (MXDC) passa la pagina alla stampante senza elaborarla.

Allocare memoria per l'escape come illustrato di seguito, impostare i campi in base alle esigenze e quindi chiamare [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape).


```C++
// Compute size of buffer required adding the
//  size of the escape structure to the size
//  of the resource data buffer.
SIZE_T iTotalDataSize = sizeof(MXDC_S0PAGE_PASSTHROUGH_ESCAPE_T) + 
                        iS0PageDataSize - 1;

// Allocate the memory buffer.
P_MXDC_S0PAGE_PASSTHROUGH_ESCAPE_T pS0PageEscapeData = 
                        (P_MXDC_S0PAGE_PASSTHROUGH_ESCAPE_T)HeapAlloc(
                            GetProcessHeap(),
                            0,
                            iTotalDataSize);
```



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

 

