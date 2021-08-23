---
description: Le costanti del flag di bit LINEGENERATETERM descrivono le condizioni in cui viene terminata la generazione di cifre \_ o toni.
ms.assetid: 5cdc43c0-2349-4ffc-9bf7-3b498b35db95
title: LINEGENERATETERM_ costanti (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c34d119f503c677e5c251bb494c5ea991dbd0fccf0bfbdb3affecf4c4ff1914
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119518971"
---
# <a name="linegenerateterm_-constants"></a>Costanti LINEGENERATETERM \_

Le costanti del flag di bit **LINEGENERATETERM \_** descrivono le condizioni in cui viene terminata la generazione di cifre o toni.

<dl> <dt>

<span id="LINEGENERATETERM_CANCEL"></span><span id="linegenerateterm_cancel"></span>**LINEGENERATETERM \_ CANCEL**
</dt> <dd> <dl> <dt>



La richiesta di generazione di cifre o toni è stata annullata da questa applicazione, da un'altra applicazione o perché la chiamata è terminata. Questo valore può essere restituito anche quando non è possibile completare la generazione di cifre o toni a causa di un errore interno del provider di servizi.


</dt> </dl> </dd> <dt>

<span id="LINEGENERATETERM_DONE"></span><span id="linegenerateterm_done"></span>**LINEGENERATETERM \_ DONE**
</dt> <dd> <dl> <dt>



Il numero richiesto di cifre o toni richiesti è stato generato per la durata richiesta.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

Nessuna estendibilità. Tutti i 32 bit sono riservati.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2.0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




