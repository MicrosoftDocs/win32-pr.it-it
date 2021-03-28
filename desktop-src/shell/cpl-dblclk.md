---
description: Inviato alla funzione CPlApplet di un'applicazione del pannello di controllo quando l'utente fa doppio clic sull'icona di una finestra di dialogo supportata dall'applicazione.
title: Messaggio CPL_DBLCLK (cpl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 68d74372-2fc2-45ed-8f77-574b943d28fa
api_name:
- CPL_DBLCLK
api_type:
- HeaderDef
api_location:
- Cpl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: d6c67204c7b4fae5275e50d428a0371af4cf2e2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104993725"
---
# <a name="cpl_dblclk-message"></a>\_Messaggio DBLCLK cpl

Inviato alla funzione [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) di un'applicazione del pannello di controllo quando l'utente fa doppio clic sull'icona di una finestra di dialogo supportata dall'applicazione.

## <a name="parameters"></a>Parametri

<dl> <dt>

*uAppNum* 
</dt> <dd>

Numero della finestra di dialogo. Questo numero deve essere compreso tra zero e uno minore del valore restituito in risposta al messaggio [**cpl \_ GetCount**](cpl-getcount.md) (cpl \_ GetCount-1).

</dd> <dt>

*lData* 
</dt> <dd>

Valore che l'applicazione del pannello di controllo è stata caricata nel membro **lpData** della struttura [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo) o [**NEWCPLINFO**](/windows/win32/api/cpl/ns-cpl-newcplinfoa) per la finestra di dialogo. L'applicazione carica il membro **lpData** in risposta al messaggio [**cpl \_ Inquirer**](cpl-inquire.md) o [**cpl \_ NEWINQUIRE**](cpl-newinquire.md) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) elabora questo messaggio correttamente, il valore restituito è zero; in caso contrario, è diverso da zero.

## <a name="remarks"></a>Commenti

In risposta a questo messaggio, un'applicazione del pannello di controllo deve visualizzare la finestra di dialogo corrispondente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                      |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>Cpl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_selezione cpl**](cpl-select.md)
</dt> </dl>

 

 
