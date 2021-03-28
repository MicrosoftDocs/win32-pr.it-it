---
description: Inviato per notificare a CPlApplet che l'utente ha scelto l'icona associata a una determinata finestra di dialogo. CPlApplet dovrebbe visualizzare la finestra di dialogo corrispondente ed eseguire tutte le attività specificate dall'utente.
title: Messaggio CPL_STARTWPARMS (cpl. h)
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
ms.openlocfilehash: 790779c1c45acbc211fe36e28b2e55d5ae2e60da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966523"
---
# <a name="cpl_startwparms-message"></a>\_Messaggio STARTWPARMS cpl

Inviato per notificare a [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) che l'utente ha scelto l'icona associata a una determinata finestra di dialogo. **CPlApplet** dovrebbe visualizzare la finestra di dialogo corrispondente ed eseguire tutte le attività specificate dall'utente.

## <a name="parameters"></a>Parametri

<dl> <dt>

*uAppNum* 
</dt> <dd>

Numero della finestra di dialogo. Questo numero deve essere compreso tra zero e uno minore del valore restituito in risposta al messaggio [**cpl \_ GetCount**](cpl-getcount.md) (cpl \_ GetCount-1).

</dd> <dt>

*lpszExtra* 
</dt> <dd>

Stringa con direzioni aggiuntive per l'esecuzione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se il messaggio è stato gestito; in caso contrario, **false** .

## <a name="remarks"></a>Commenti

**Cpl \_ STARTWPARMS** è simile a [**cpl \_ DBLCLK**](cpl-dblclk.md) ma consente di passare una stringa a [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) anziché a un valore **int**. È possibile utilizzare questa stringa come metodo flessibile per fornire indicazioni dettagliate per l'esecuzione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional, \[ solo app desktop Windows XP\]<br/>           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>Cpl. h</dt> </dl> |



 

 
