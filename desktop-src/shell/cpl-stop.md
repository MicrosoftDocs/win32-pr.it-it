---
description: Inviato alla funzione CPlApplet di un'applicazione del pannello di controllo quando si chiude l'applicazione di controllo del pannello di controllo. L'applicazione di controllo Invia il messaggio una volta per ogni finestra di dialogo supportata dall'applicazione.
title: Messaggio CPL_STOP (cpl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 4f632b91-8200-42a3-90cc-a98889704ca4
api_name:
- CPL_STOP
api_type:
- HeaderDef
api_location:
- Cpl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 78f8926d85b35b8cf5e55188c6cd76b014b3c4c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977338"
---
# <a name="cpl_stop-message"></a>\_Messaggio di arresto cpl

Inviato alla funzione [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) di un'applicazione del pannello di controllo quando si chiude l'applicazione di controllo del pannello di controllo. L'applicazione di controllo Invia il messaggio una volta per ogni finestra di dialogo supportata dall'applicazione.

## <a name="parameters"></a>Parametri

<dl> <dt>

*uAppNum* 
</dt> <dd>

Numero della finestra di dialogo.

</dd> <dt>

*lData* 
</dt> <dd>

Valore che l'applicazione del pannello di controllo è stata caricata nel membro **lpData** della struttura [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo) o [**NEWCPLINFO**](/windows/win32/api/cpl/ns-cpl-newcplinfoa) per la finestra di dialogo. L'applicazione carica il membro **lpData** in risposta al messaggio [**cpl \_ Inquirer**](cpl-inquire.md) o [**cpl \_ NEWINQUIRE**](cpl-newinquire.md) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) elabora correttamente questo messaggio, deve restituire zero.

## <a name="remarks"></a>Commenti

In risposta a questo messaggio, un'applicazione del pannello di controllo deve eseguire la pulizia per la finestra di dialogo specificata.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                      |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>Cpl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_uscita cpl**](cpl-exit.md)
</dt> <dt>

[**\_conteggio cpl**](cpl-getcount.md)
</dt> </dl>

 

 
