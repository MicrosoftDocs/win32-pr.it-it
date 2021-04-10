---
description: La struttura MXDC \_ S0PAGE \_ Resource \_ escape \_ t è una \_ \_ \_ struttura di escape t MXDC concatenata a una struttura della \_ \_ \_ risorsa \_ t S0PAGE XPS MXDC.
ms.assetid: e5caa280-f0a5-4a89-b4f1-4f195a537dc6
title: Struttura MXDC_S0PAGE_RESOURCE_ESCAPE_T (MXDC. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_S0PAGE_RESOURCE_ESCAPE_T
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: ed1d78aad1ede2a318dcde2d3a2d39fd8e666ddc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227464"
---
# <a name="mxdc_s0page_resource_escape_t-structure"></a>MXDC \_ S0PAGE \_ risorsa \_ escape \_ T struttura

La struttura **MXDC \_ S0PAGE \_ Resource \_ escape \_ t** è una struttura di [**\_ escape \_ \_ t MXDC**](mxdcescapeheader.md) concatenata a una struttura della [**\_ \_ \_ risorsa \_ t S0PAGE XPS MXDC**](mxdcxpss0pageresource.md) .

## <a name="syntax"></a>Sintassi


```C++
typedef struct tagMxdcS0PageResourceEscape {
  MXDC_ESCAPE_HEADER_T       mxdcEscape;
  MXDC_XPS_S0PAGE_RESOURCE_T xpsS0PageResourcePassthrough;
} MXDC_S0PAGE_RESOURCE_ESCAPE_T, *P_MXDC_S0PAGE_RESOURCE_ESCAPE_T;
```



## <a name="members"></a>Members

<dl> <dt>

**mxdcEscape**
</dt> <dd>

Una struttura [**MXDC dell' \_ intestazione di escape \_ \_ T**](mxdcescapeheader.md) con il membro **OpCode** impostato su MXDCOP \_ imposta la \_ risorsa S0PAGE \_ .

</dd> <dt>

**xpsS0PageResourcePassthrough**
</dt> <dd>

Una struttura della [**\_ \_ \_ risorsa \_ T MXDC XPS S0PAGE**](mxdcxpss0pageresource.md) che rappresenta una risorsa, ad esempio un tipo di carattere o un file di immagine, in una pagina del documento XPS.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa struttura viene passata nel parametro *lpszInData* della funzione [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) quando tale funzione viene chiamata con l'escape di [**\_ escape MXDC**](mxdc-escape.md) e il membro **OpCode** della struttura dell' [**intestazione di \_ escape \_ MXDC \_ T**](mxdcescapeheader.md) è **MXDCOP \_ set \_ S0PAGE \_ Resource**. Il risultato è una risorsa di pagina da inviare a MXDC.

Allocare memoria per l'escape come illustrato di seguito, impostare i campi in base alle esigenze e quindi chiamare [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape).


```C++
// Compute size of buffer required adding the
//  size of the escape structure to the size
//  of the resource data buffer.
SIZE_T iTotalDataSize = sizeof(MXDC_S0PAGE_RESOURCE_ESCAPE_T) + 
                        iS0PageResourceDataSize - 1;

// Allocate the memory buffer.
P_MXDC_S0PAGE_RESOURCE_ESCAPE_T pS0PageResourceEscapeData = 
                        (P_MXDC_S0PAGE_RESOURCE_ESCAPE_T)HeapAlloc(
                            GetProcessHeap(),
                            0,
                            iTotalDataSize);
```



La chiamata a [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) deve essere compresa tra una chiamata a [**Startpage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) e una chiamata a [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage); Tuttavia, può essere presente più di una di queste chiamate tra le chiamate a **Startpage** e **EndPage**.

Il consumo di flussi è più efficiente se si chiama [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) con **MXDCOP \_ set \_ S0PAGE \_ Resource** **OpCode** per ogni risorsa nella pagina prima di chiamare **ExtEscape** con il **codice operativo** MXDCOP **\_ set \_ S0PAGE**.  

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

 

