---
description: La struttura MXDC S0PAGE DATA T contiene una pagina di documento XPS da passare al file di \_ \_ output di Microsoft \_ XPS Document Converter (MXDC) senza alcuna elaborazione.
ms.assetid: 3dc8e0b9-cf63-4345-93d2-3b60dac42546
title: MXDC_S0PAGE_DATA_T (Mxdc.h)
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
ms.openlocfilehash: 1ff54325859acef6da136c4bce20286bc7c746d8880d8994ca834213adf57b58
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119776551"
---
# <a name="mxdc_s0page_data_t-structure"></a>Struttura MXDC \_ S0PAGE \_ DATA \_ T

La **struttura MXDC \_ S0PAGE \_ DATA \_ T** contiene una pagina di documento XPS da passare al file di output di Microsoft XPS Document Converter (MXDC) senza alcuna elaborazione.

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

Dimensioni del buffer di output, **bData**.

</dd> <dt>

**bData**
</dt> <dd>

Pagina del documento XPS.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa struttura viene aggiunta a una struttura [**MXDC \_ ESCAPE HEADER \_ \_ T**](mxdcescapeheader.md) (la cui proprietà **opCode** è impostata su MXDCOP SET S0PAGE) per creare una struttura \_ \_ [**MXDC \_ S0PAGE \_ PASSTHROUGH ESCAPE \_ \_ T.**](mxdcs0pagepassthroughescape.md) Tale struttura viene quindi passata al parametro *lpszInData* della funzione [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) quando viene chiamata con [**MXDC \_ ESCAPE**](mxdc-escape.md) come escape. Il risultato è che MXDC passa la pagina all'output senza elaborarla.

La chiamata a [**ExtEscape deve**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) essere compresa tra una chiamata a [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) e una chiamata a [**EndPage.**](/windows/desktop/api/Wingdi/nf-wingdi-endpage)

L'applicazione chiamante è responsabile della convalida del codice XML della pagina del documento XPS.

L'utilizzo dello streaming è più efficiente se si chiama [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) con **MXDCOP \_ SET \_ S0PAGE \_ RESOURCE** come **opCode** per ogni risorsa nella pagina prima di chiamarla con **MXDCOP \_ SET \_ S0PAGE.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                    |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                              |
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

 

