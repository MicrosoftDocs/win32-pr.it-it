---
description: Le \_ costanti del flag di bit LINECALLSELECT descrivono quali chiamate devono essere selezionate.
ms.assetid: f19a41bc-403a-4d4b-ab85-240a73514ebb
title: Costanti LINECALLSELECT_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8330b4c4e4e14ac399595d10d4a208a3c67f5b2a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332894"
---
# <a name="linecallselect_-constants"></a>\_Costanti LINECALLSELECT

Le costanti del flag di bit **LINECALLSELECT \_** descrivono quali chiamate devono essere selezionate.

<dl> <dt>

<span id="LINECALLSELECT_ADDRESS"></span><span id="linecallselect_address"></span>**\_Indirizzo LINECALLSELECT**
</dt> <dd> <dl> <dt>



Seleziona la chiamata sull'indirizzo specificato.


</dt> </dl> </dd> <dt>

<span id="LINECALLSELECT_CALL"></span><span id="linecallselect_call"></span>**\_chiamata LINECALLSELECT**
</dt> <dd> <dl> <dt>



Seleziona le chiamate correlate alla chiamata specificata. Ad esempio, le entità in una chiamata di conferenza.


</dt> </dl> </dd> <dt>

<span id="LINECALLSELECT_CALLID"></span><span id="linecallselect_callid"></span>**\_CALLID LINECALLSELECT**
</dt> <dd> <dl> <dt>



Seleziona le chiamate correlate all'identificatore di chiamata specificato. Questo flag viene esposto solo alle applicazioni che negoziano una versione di TAPI 3,0 o successiva.


</dt> </dl> </dd> <dt>

<span id="LINECALLSELECT_DEVICEID"></span><span id="linecallselect_deviceid"></span>**\_DEVICEID LINECALLSELECT**
</dt> <dd> <dl> <dt>



Seleziona le chiamate sull'identificatore di dispositivo specificato. Questo flag viene esposto solo alle applicazioni che negoziano una versione di TAPI 2,1 o successiva. Le applicazioni devono prendere in considerazione l'uso della \_ costante della riga LINECALLSELECT invece di questa.


</dt> </dl> </dd> <dt>

<span id="LINECALLSELECT_LINE"></span><span id="linecallselect_line"></span>**\_linea LINECALLSELECT**
</dt> <dd> <dl> <dt>



Seleziona le chiamate sul dispositivo a linee specificato.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

Nessuna estensibilità. Tutti i 32 bit sono riservati.

Questa costante viene utilizzata in [**lineGetNewCalls**](/windows/desktop/api/Tapi/nf-tapi-linegetnewcalls) e per specificare una selezione (ambito) delle chiamate richieste.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2,0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




