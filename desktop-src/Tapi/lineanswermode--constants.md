---
description: Le \_ costanti del flag di bit LINEANSWERMODE descrivono in che modo una chiamata attiva esistente su un dispositivo linea è interessata dalla risposta di un'altra chiamata all'offerta sulla stessa riga.
ms.assetid: 35f63d92-970f-4fb8-aba9-179fc7de70f4
title: Costanti LINEANSWERMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 658d5b1265d28f8cb719719e4303fde97d3fff3e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332906"
---
# <a name="lineanswermode_-constants"></a>\_Costanti LINEANSWERMODE

Le costanti del flag di bit **LINEANSWERMODE \_** descrivono in che modo una chiamata attiva esistente su un dispositivo linea è interessata dalla risposta di un'altra chiamata all' *offerta* sulla stessa riga.

<dl> <dt>

<span id="LINEANSWERMODE_DROP"></span><span id="lineanswermode_drop"></span>**LINEANSWERMODE \_ Drop**
</dt> <dd> <dl> <dt>



La chiamata attualmente attiva verrà eliminata automaticamente.


</dt> </dl> </dd> <dt>

<span id="LINEANSWERMODE_HOLD"></span><span id="lineanswermode_hold"></span>**LINEANSWERMODE in \_ attesa**
</dt> <dd> <dl> <dt>



La chiamata attualmente attiva verrà automaticamente messa in attesa.


</dt> </dl> </dd> <dt>

<span id="LINEANSWERMODE_NONE"></span><span id="lineanswermode_none"></span>**LINEANSWERMODE \_ None**
</dt> <dd> <dl> <dt>



La risposta a un'altra chiamata sulla stessa riga non ha alcun effetto sulla chiamata attiva esistente sulla riga.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

Nessuna estensibilità. Tutti i 32 bit sono riservati.

Se una chiamata viene offerta (disponibile) quando un'altra chiamata è già attiva, la nuova chiamata viene connessa a richiamando [**lineAnswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer). L'effetto presente sulla chiamata attiva esistente dipende dalle funzionalità del dispositivo della linea. La prima chiamata potrebbe non essere interessata, è possibile che venga eliminata automaticamente o che venga automaticamente messa in attesa.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2,0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




