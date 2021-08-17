---
description: Le costanti del flag di bit LINEGATHERTERM descrivono le condizioni in cui viene terminata la raccolta di cifre \_ memorizzate nel buffer.
ms.assetid: 409e1984-e5a4-4636-ab53-5973fe7b78ea
title: LINEGATHERTERM_ costanti (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8a6d5952ac4f69d11fd499df63554d6fda7dca76e46e4aad1a01ae326f363a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119140034"
---
# <a name="linegatherterm_-constants"></a>Costanti LINEGATHERTERM \_

Le costanti del flag di bit **LINEGATHERTERM \_** descrivono le condizioni in cui viene terminata la raccolta di cifre memorizzate nel buffer.

<dl> <dt>

<span id="LINEGATHERTERM_BUFFERFULL"></span><span id="linegatherterm_bufferfull"></span>**LINEGATHERTERM \_ BUFFERFULL**
</dt> <dd> <dl> <dt>



È stato raccolto il numero di cifre richiesto. Il buffer è pieno.


</dt> </dl> </dd> <dt>

<span id="LINEGATHERTERM_CANCEL"></span><span id="linegatherterm_cancel"></span>**LINEGATHERTERM \_ CANCEL**
</dt> <dd> <dl> <dt>



La richiesta è stata annullata da questa applicazione, da un'altra applicazione o perché la chiamata è terminata.


</dt> </dl> </dd> <dt>

<span id="LINEGATHERTERM_FIRSTTIMEOUT"></span><span id="linegatherterm_firsttimeout"></span>**LINEGATHERTERM \_ FIRSTTIMEOUT**
</dt> <dd> <dl> <dt>



Il timeout della prima cifra è scaduto. Il buffer non contiene cifre.


</dt> </dl> </dd> <dt>

<span id="LINEGATHERTERM_INTERTIMEOUT"></span><span id="linegatherterm_intertimeout"></span>**LINEGATHERTERM \_ INTERTIMEOUT**
</dt> <dd> <dl> <dt>



Timeout tra cifre scaduto. Il buffer contiene almeno una cifra.


</dt> </dl> </dd> <dt>

<span id="LINEGATHERTERM_TERMDIGIT"></span><span id="linegatherterm_termdigit"></span>**LINEGATHERTERM \_ TERMDIGIT**
</dt> <dd> <dl> <dt>



Una delle cifre di terminazione corrisponde a una cifra ricevuta. La cifra di terminazione corrispondente è l'ultima cifra nel buffer.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

Nessuna estendibilità. Tutti i 32 bit sono riservati.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2.0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




