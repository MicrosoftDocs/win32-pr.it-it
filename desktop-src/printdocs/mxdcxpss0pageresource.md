---
description: La struttura MXDC XPS S0PAGE RESOURCE T contiene informazioni su una risorsa, ad esempio un'immagine o un tipo di carattere, associato a una pagina di documento XPS e deve essere passata al file di \_ \_ output di Microsoft \_ \_ XPS Document Converter (MXDC).
ms.assetid: af0690a6-3047-4e95-b719-2305948c0f5d
title: MXDC_XPS_S0PAGE_RESOURCE_T (Mxdc.h)
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
ms.openlocfilehash: 21035a99b6237c481a5b7560f469086ef2960d655ba32582ed273edb48910ba8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971180"
---
# <a name="mxdc_xps_s0page_resource_t-structure"></a>Struttura MXDC \_ XPS \_ S0PAGE \_ RESOURCE \_ T

La struttura **MXDC \_ XPS \_ S0PAGE \_ RESOURCE \_ T** contiene informazioni su una risorsa, ad esempio un'immagine o un tipo di carattere, associato a una pagina di documento XPS e deve essere passata al file di output di Microsoft XPS Document Converter (MXDC).

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

Dimensione totale della struttura e della risorsa a cui punta.

</dd> <dt>

**dwResourceType**
</dt> <dd>

Valore di tipo [**MXDC \_ S0 \_ PAGE \_ ENUMS**](mxdcs0pageenums.md) che indica il tipo di risorsa, ad esempio l'immagine TIFF o il tipo di carattere TrueType.

</dd> <dt>

**szUri**
</dt> <dd>

URI della risorsa. Non può essere superiore a 260 byte.

</dd> <dt>

**dwDataSize**
</dt> <dd>

Dimensioni della risorsa in byte.

</dd> <dt>

**bData**
</dt> <dd>

Dati della risorsa in una matrice di byte con dimensioni 1 + dimensioni della risorsa.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa struttura viene aggiunta a una struttura [**MXDC \_ ESCAPE HEADER \_ \_ T**](mxdcescapeheader.md) (la cui proprietà **opCode** è impostata su **MXDCOP \_ SET \_ S0PAGERESOURCE)** per creare una struttura [**MXDC \_ S0PAGE \_ RESOURCE ESCAPE \_ \_ T.**](mxdcs0pageresourceescape.md) La struttura **MXDC \_ S0PAGE \_ RESOURCE ESCAPE \_ \_ T** risultante viene quindi passata nel parametro *lpszInData* della funzione [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) che viene chiamata con l'escape [**MXDC \_ ESCAPE.**](mxdc-escape.md) L'effetto è l'invio della risorsa a MXDC per la conversione e la scrittura nel file di output.

La chiamata a [**ExtEscape deve**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) essere compresa tra una chiamata a [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) e una chiamata a [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage). tuttavia possono essere presenti più chiamate di questo tipo tra le chiamate a **StartPage** ed **EndPage.**

L'utilizzo dello streaming è più efficiente se si chiama [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) con il **codice** operativo **MXDCOP \_ SET \_ S0PAGE \_ RESOURCE** per ogni risorsa nella pagina prima di chiamare **ExtEscape** con il codice operativo **MXDCOP \_ SET \_ S0PAGE** **.**

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

 

