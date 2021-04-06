---
description: La \_ struttura della \_ risorsa T S0PAGE di MXDC XPS \_ \_ include informazioni su una risorsa, ad esempio un'immagine o un tipo di carattere, associato a una pagina del documento XPS e da passare al file di output di Microsoft XPS Document Converter (MXDC).
ms.assetid: af0690a6-3047-4e95-b719-2305948c0f5d
title: Struttura MXDC_XPS_S0PAGE_RESOURCE_T (MXDC. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_XPS_S0PAGE_RESOURCE_T
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: 90f8a52ed3bd1bcba4c8f21a086627781bdbbf67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882514"
---
# <a name="mxdc_xps_s0page_resource_t-structure"></a>\_ \_ \_ Struttura T della risorsa \_ S0PAGE di MXDC XPS

La struttura della **\_ \_ \_ risorsa \_ T S0PAGE di MXDC XPS** include informazioni su una risorsa, ad esempio un'immagine o un tipo di carattere, associato a una pagina del documento XPS e da passare al file di output di Microsoft XPS Document Converter (MXDC).

## <a name="syntax"></a>Sintassi


```C++
typedef struct tagMxdcXpsS0PageResource {
  DWORD dwSize;
  DWORD dwResourceType;
  BYTE  szUri[MAX_PATH];
  DWORD dwDataSize;
  BYTE  bData[1];
} MXDC_XPS_S0PAGE_RESOURCE_T, *P_MXDC_XPS_S0PAGE_RESOURCE_T;
```



## <a name="members"></a>Members

<dl> <dt>

**dwSize**
</dt> <dd>

Dimensioni totali della struttura e della risorsa a cui fa riferimento.

</dd> <dt>

**dwResourceType**
</dt> <dd>

Valore di tipo [**MXDC \_ S0 \_ Page \_ enums**](mxdcs0pageenums.md) che indica il tipo di risorsa, ad esempio l'immagine TIFF o il tipo di carattere TrueType.

</dd> <dt>

**szUri**
</dt> <dd>

URI della risorsa. Non può essere superiore a 260 byte.

</dd> <dt>

**dwDataSize**
</dt> <dd>

Dimensioni in byte della risorsa.

</dd> <dt>

**bData**
</dt> <dd>

I dati della risorsa in una matrice di byte con dimensioni pari a 1 + le dimensioni della risorsa.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa struttura viene aggiunta a una struttura [**MXDC \_ dell' \_ intestazione \_ di escape t**](mxdcescapeheader.md) (il cui **codice operativo** è impostato su **MXDCOP \_ set \_ S0PAGERESOURCE**) per creare una struttura di [**\_ \_ \_ escape \_ t della risorsa MXDC S0PAGE**](mxdcs0pageresourceescape.md) . La struttura **di \_ \_ \_ escape \_ T della risorsa S0PAGE MXDC** risultante viene quindi passata nel parametro *lpszInData* della funzione [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) chiamata con l'escape di [**\_ escape MXDC**](mxdc-escape.md) . L'effetto è l'invio della risorsa a MXDC per la conversione e la scrittura nel file di output.

La chiamata a [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) deve essere compresa tra una chiamata a [**Startpage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) e una chiamata a [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage); Tuttavia, possono essere presenti più chiamate tra le chiamate a **Startpage** e **EndPage**.

Il consumo di flussi è più efficiente se si chiama [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) con **MXDCOP \_ set \_ S0PAGE \_ Resource** **OpCode** per ogni risorsa nella pagina prima di chiamare **ExtEscape** con il **codice operativo** MXDCOP **\_ set \_ S0PAGE** .

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

 

