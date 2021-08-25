---
title: EM_FILELINEINDEX messaggio (CommCtrl.h)
description: Ottiene l'indice dei caratteri del primo carattere di una riga specificata in un controllo di modifica su più righe, indipendentemente dalla modalità di visualizzazione delle righe sullo schermo.
ms.assetid: vs|controls|~\controls\editcontrols\editcontrolreference\editcontrolmessages\em_lineindex.htm
keywords:
- EM_FILELINEINDEX di controllo Windows messaggio
topic_type:
- apiref
api_name:
- EM_FILELINEINDEX
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df7c4bd1f21ee6bcdf7bec56828ea9c2996c837def614c0c537ef83ee053ebfc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119915611"
---
# <a name="em_filelineindex-message-commctrlh"></a>EM_FILELINEINDEX messaggio (CommCtrl.h)

Ottiene l'indice dei caratteri del primo carattere di una riga specificata in un controllo di modifica su più righe, indipendentemente dalla modalità di visualizzazione delle righe sullo schermo. Un indice di caratteri è l'indice in base zero del carattere dall'inizio del controllo di modifica.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Numero di riga in base zero. Il valore -1 specifica il numero di riga corrente (la riga che contiene il punto di interruzione).

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è l'indice dei caratteri della riga specificata nel *parametro wParam,* indipendentemente dalla modalità di visualizzazione delle righe sullo schermo oppure è -1 se il numero di riga specificato è maggiore del numero di righe nel controllo di modifica.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 10, solo app desktop 1809 \[\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop server 2019 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>CommCtrl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**EM \_ FILELINEFROMCHAR**](em-filelinefromchar.md)
</dt> </dl>

 

 





