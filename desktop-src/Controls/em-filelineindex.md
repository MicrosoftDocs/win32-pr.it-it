---
title: Messaggio EM_FILELINEINDEX (CommCtrl. h)
description: Ottiene l'indice dei caratteri del primo carattere di una riga specificata in un controllo di modifica su più righe, indipendentemente dalla modalità di visualizzazione delle linee sullo schermo.
ms.assetid: vs|controls|~\controls\editcontrols\editcontrolreference\editcontrolmessages\em_lineindex.htm
keywords:
- Controlli di Windows Message EM_FILELINEINDEX
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
ms.openlocfilehash: a4ce5f5ca07fc9fb9869898965422c7c8a6aa3fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120135"
---
# <a name="em_filelineindex-message-commctrlh"></a>Messaggio EM_FILELINEINDEX (CommCtrl. h)

Ottiene l'indice dei caratteri del primo carattere di una riga specificata in un controllo di modifica su più righe, indipendentemente dalla modalità di visualizzazione delle linee sullo schermo. Un indice dei caratteri è l'indice in base zero del carattere a partire dall'inizio del controllo di modifica.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Numero di riga in base zero. Il valore-1 specifica il numero di riga corrente, ovvero la riga che contiene il punto di inserimento.

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è l'indice dei caratteri della riga specificata nel parametro *wParam* , indipendentemente dalla modalità di visualizzazione delle linee sullo schermo, oppure-1 se il numero di riga specificato è maggiore del numero di righe nel controllo di modifica.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows 10, 1809 \[\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2019\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>CommCtrl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_FILELINEFROMCHAR em**](em-filelinefromchar.md)
</dt> </dl>

 

 





