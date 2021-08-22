---
description: La struttura MXDC S0PAGE PASSTHROUGH ESCAPE T è una struttura MXDC ESCAPE HEADER T concatenata a una struttura \_ \_ \_ \_ \_ \_ \_ MXDC \_ S0PAGE \_ DATA \_ T.
ms.assetid: 949c1ed4-92d5-4c11-a7da-f9d94bafe3f8
title: MXDC_S0PAGE_PASSTHROUGH_ESCAPE_T struttura (Mxdc.h)
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
ms.openlocfilehash: f8e0a46766f38aec16758a1efc9c0cbc775c2131b1279dcc47f92ed41e77c0e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119099055"
---
# <a name="mxdc_s0page_passthrough_escape_t-structure"></a>Struttura MXDC \_ S0PAGE \_ PASSTHROUGH \_ ESCAPE \_ T

La **struttura MXDC \_ S0PAGE \_ PASSTHROUGH ESCAPE \_ \_ T** è una struttura [**MXDC ESCAPE HEADER \_ \_ \_ T**](mxdcescapeheader.md) concatenata a una struttura [**MXDC \_ S0PAGE \_ DATA \_ T.**](mxdcs0pagedata.md)

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

Struttura [**MXDC \_ ESCAPE HEADER \_ \_ T**](mxdcescapeheader.md) con il membro **opCode** impostato su **MXDCOP \_ SET \_ S0PAGE**.

</dd> <dt>

**xpsS0PageData**
</dt> <dd>

Struttura [**MxdcS0PageData**](mxdcs0pagedata.md) che rappresenta una pagina di documenti XPS.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa struttura viene passata nel parametro *lpszInData* della funzione [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) quando viene chiamata con l'escape [**ESCAPE \_ MXDC**](mxdc-escape.md) e il membro **opCode** della struttura [**MXDC ESCAPE HEADER \_ \_ \_ T**](mxdcescapeheader.md) **è MXDCOP SET \_ \_ S0PAGE.** Il risultato è che Microsoft XML Document Converter (MXDC) passa la pagina alla stampante senza elaborarla.

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



La chiamata a [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) deve essere tra una chiamata a [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) e una chiamata a [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage).

L'applicazione chiamante è responsabile della convalida del codice XML della pagina del documento XPS.

L'utilizzo dello streaming è più efficiente se si chiama [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) con **MXDCOP \_ SET \_ S0PAGE \_ RESOURCE** come **opCode** per ogni risorsa nella pagina prima di chiamarla con **MXDCOP \_ SET \_ S0PAGE**.

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

 

