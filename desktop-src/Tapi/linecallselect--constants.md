---
description: Le costanti del flag di bit LINECALLSELECT \_ descrivono le chiamate da selezionare.
ms.assetid: f19a41bc-403a-4d4b-ab85-240a73514ebb
title: LINECALLSELECT_ costanti (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: feaa76ea5b421b8090f9289431bfee65be61a6b47abd170569beff73a9846533
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003149"
---
# <a name="linecallselect_-constants"></a>Costanti \_ LINECALLSELECT

Le costanti del flag di bit **LINECALLSELECT \_** descrivono le chiamate da selezionare.

<dl> <dt>

<span id="LINECALLSELECT_ADDRESS"></span><span id="linecallselect_address"></span>**LINECALLSELECT \_ ADDRESS**
</dt> <dd> <dl> <dt>



Seleziona la chiamata sull'indirizzo specificato.


</dt> </dl> </dd> <dt>

<span id="LINECALLSELECT_CALL"></span><span id="linecallselect_call"></span>**CHIAMATA \_ LINECALLSELECT**
</dt> <dd> <dl> <dt>



Seleziona le chiamate correlate alla chiamata specificata. Ad esempio, le parti in una conferenza telefonica.


</dt> </dl> </dd> <dt>

<span id="LINECALLSELECT_CALLID"></span><span id="linecallselect_callid"></span>**LINECALLSELECT \_ CALLID**
</dt> <dd> <dl> <dt>



Seleziona le chiamate correlate all'identificatore di chiamata specificato. Questo flag viene esposto solo alle applicazioni che negoziano una versione TAPI 3.0 o successiva.


</dt> </dl> </dd> <dt>

<span id="LINECALLSELECT_DEVICEID"></span><span id="linecallselect_deviceid"></span>**LINECALLSELECT \_ DEVICEID**
</dt> <dd> <dl> <dt>



Seleziona le chiamate sull'identificatore di dispositivo specificato. Questo flag viene esposto solo alle applicazioni che negoziano una versione TAPI 2.1 o successiva. Le applicazioni devono prendere in considerazione l'uso della costante LINECALLSELECT \_ LINE anziché di questa.


</dt> </dl> </dd> <dt>

<span id="LINECALLSELECT_LINE"></span><span id="linecallselect_line"></span>**LINECALLSELECT \_ LINE**
</dt> <dd> <dl> <dt>



Seleziona le chiamate nel dispositivo di linea specificato.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

Nessuna estendibilità. Tutti i 32 bit sono riservati.

Questa costante viene usata in [**lineGetNewCalls**](/windows/desktop/api/Tapi/nf-tapi-linegetnewcalls) e per specificare una selezione (ambito) delle chiamate richieste.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2.0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




