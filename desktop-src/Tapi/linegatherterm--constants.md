---
description: Le \_ costanti del flag di bit LINEGATHERTERM descrivono le condizioni in base alle quali viene terminata la raccolta dei numeri memorizzati nel buffer.
ms.assetid: 409e1984-e5a4-4636-ab53-5973fe7b78ea
title: Costanti LINEGATHERTERM_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 968492a584024c7750b417a9fd03b68ac1df42ab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333546"
---
# <a name="linegatherterm_-constants"></a>\_Costanti LINEGATHERTERM

Le costanti del flag di bit **LINEGATHERTERM \_** descrivono le condizioni in base alle quali viene terminata la raccolta dei numeri memorizzati nel buffer.

<dl> <dt>

<span id="LINEGATHERTERM_BUFFERFULL"></span><span id="linegatherterm_bufferfull"></span>**\_BUFFERFULL LINEGATHERTERM**
</dt> <dd> <dl> <dt>



Il numero di cifre richiesto è stato raccolto. Il buffer è pieno.


</dt> </dl> </dd> <dt>

<span id="LINEGATHERTERM_CANCEL"></span><span id="linegatherterm_cancel"></span>**\_annullamento LINEGATHERTERM**
</dt> <dd> <dl> <dt>



La richiesta è stata annullata dall'applicazione, da un'altra applicazione o perché la chiamata è stata terminata.


</dt> </dl> </dd> <dt>

<span id="LINEGATHERTERM_FIRSTTIMEOUT"></span><span id="linegatherterm_firsttimeout"></span>**\_FIRSTTIMEOUT LINEGATHERTERM**
</dt> <dd> <dl> <dt>



Timeout della prima cifra scaduto. Il buffer non contiene cifre.


</dt> </dl> </dd> <dt>

<span id="LINEGATHERTERM_INTERTIMEOUT"></span><span id="linegatherterm_intertimeout"></span>**intertimeout LINEGATHERTERM \_**
</dt> <dd> <dl> <dt>



Timeout tra cifre scaduto. Il buffer contiene almeno una cifra.


</dt> </dl> </dd> <dt>

<span id="LINEGATHERTERM_TERMDIGIT"></span><span id="linegatherterm_termdigit"></span>**\_TERMDIGIT LINEGATHERTERM**
</dt> <dd> <dl> <dt>



Una delle cifre di terminazione corrisponde a una cifra ricevuta. La cifra di terminazione corrispondente è l'ultima cifra nel buffer.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

Nessuna estensibilità. Tutti i 32 bit sono riservati.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2,0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




