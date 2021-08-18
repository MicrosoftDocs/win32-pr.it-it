---
description: Inviato per notificare a CPlApplet che l'utente ha scelto l'icona associata a una determinata finestra di dialogo. CPlApplet dovrebbe visualizzare la finestra di dialogo corrispondente ed eseguire qualsiasi attività specificata dall'utente.
title: CPL_STARTWPARMS messaggio (Cpl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 04ac5117-39c9-4d3f-b32d-8f8d2b515be1
api_name:
- CPL_STARTWPARMS
api_type:
- HeaderDef
api_location:
- Cpl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: f836f868b81daa49e87eb4efc804442bed25690ce126852891327d0eb042aaec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118460610"
---
# <a name="cpl_startwparms-message"></a>Messaggio \_ STARTWPARMS CPL

Inviato per notificare [**a CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) che l'utente ha scelto l'icona associata a una determinata finestra di dialogo. **CPlApplet dovrebbe** visualizzare la finestra di dialogo corrispondente ed eseguire qualsiasi attività specificata dall'utente.

## <a name="parameters"></a>Parametri

<dl> <dt>

*uAppNum* 
</dt> <dd>

Numero della finestra di dialogo. Questo numero deve essere compreso nell'intervallo compreso tra zero e uno minore del valore restituito in risposta al messaggio [**\_ GETCOUNT CPL**](cpl-getcount.md) (CPL \_ GETCOUNT – 1).

</dd> <dt>

*lpszExtra* 
</dt> <dd>

Stringa con istruzioni aggiuntive per l'esecuzione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE se** il messaggio è stato gestito oppure FALSE in caso **contrario.**

## <a name="remarks"></a>Commenti

**Libreria CPL \_ STARTWPARMS è** simile a [**CPL \_ DBLCLK,**](cpl-dblclk.md) ma consente di passare una stringa a [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) anziché a **int**. È possibile usare questa stringa come modo flessibile per fornire indicazioni dettagliate per l'esecuzione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional, Windows solo app \[ desktop XP\]<br/>           |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>Cpl.h</dt> </dl> |



 

 
