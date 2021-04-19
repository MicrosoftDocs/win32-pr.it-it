---
description: Le \_ costanti del flag di bit LINEGENERATETERM descrivono le condizioni in base alle quali viene terminata la generazione di numeri o toni.
ms.assetid: 5cdc43c0-2349-4ffc-9bf7-3b498b35db95
title: Costanti LINEGENERATETERM_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6804b09879471a77780a95ca4ed35b7aaa5b6e1a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333545"
---
# <a name="linegenerateterm_-constants"></a>\_Costanti LINEGENERATETERM

Le costanti del flag di bit **LINEGENERATETERM \_** descrivono le condizioni in base alle quali viene terminata la generazione di numeri o toni.

<dl> <dt>

<span id="LINEGENERATETERM_CANCEL"></span><span id="linegenerateterm_cancel"></span>**\_annullamento LINEGENERATETERM**
</dt> <dd> <dl> <dt>



La richiesta di generazione di numeri o toni è stata annullata dall'applicazione, da un'altra applicazione o dalla chiamata terminata. Questo valore può essere restituito anche quando non è possibile completare la generazione di numeri o toni a causa di un errore interno del provider di servizi.


</dt> </dl> </dd> <dt>

<span id="LINEGENERATETERM_DONE"></span><span id="linegenerateterm_done"></span>**LINEGENERATETERM \_ completato**
</dt> <dd> <dl> <dt>



Il numero richiesto di cifre o i toni richiesti sono stati generati per la durata richiesta.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

Nessuna estensibilità. Tutti i 32 bit sono riservati.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2,0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




