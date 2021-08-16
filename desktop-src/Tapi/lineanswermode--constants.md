---
description: Le costanti del flag di bit LINEANSWERMODE descrivono in che modo una chiamata attiva esistente su un dispositivo line viene interessata rispondendo a un'altra chiamata di offerta \_ sulla stessa riga.
ms.assetid: 35f63d92-970f-4fb8-aba9-179fc7de70f4
title: LINEANSWERMODE_ costanti (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abfb9d6491864f5be8788575d718e42cc5f5c7c337fd046c110bd5bd82eae110
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117761843"
---
# <a name="lineanswermode_-constants"></a>Costanti LINEANSWERMODE \_

Le costanti del flag di bit **LINEANSWERMODE \_** descrivono in che modo  una chiamata attiva esistente su un dispositivo line viene interessata rispondendo a un'altra chiamata di offerta sulla stessa riga.

<dl> <dt>

<span id="LINEANSWERMODE_DROP"></span><span id="lineanswermode_drop"></span>**LINEANSWERMODE \_ DROP**
</dt> <dd> <dl> <dt>



La chiamata attualmente attiva verrà eliminata automaticamente.


</dt> </dl> </dd> <dt>

<span id="LINEANSWERMODE_HOLD"></span><span id="lineanswermode_hold"></span>**LINEANSWERMODE \_ HOLD**
</dt> <dd> <dl> <dt>



La chiamata attualmente attiva verrà automaticamente messa in attesa.


</dt> </dl> </dd> <dt>

<span id="LINEANSWERMODE_NONE"></span><span id="lineanswermode_none"></span>**LINEANSWERMODE \_ NONE**
</dt> <dd> <dl> <dt>



La risposta a un'altra chiamata sulla stessa riga non ha alcun effetto sulla chiamata attiva esistente sulla riga.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

Nessuna estendibilità. Tutti i 32 bit sono riservati.

Se una chiamata entra (viene offerta) nel momento in cui un'altra chiamata è già attiva, la nuova chiamata viene connessa a richiamando [**lineAnswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer). L'effetto di questa operazione sulla chiamata attiva esistente dipende dalle funzionalità del dispositivo della riga. La prima chiamata potrebbe non essere interrotta, essere eliminata automaticamente o essere automaticamente messa in attesa.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2.0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




