---
description: Le \_ costanti del flag di bit LINECALLPARTYID descrivono la natura delle informazioni disponibili sulle entità coinvolte in una chiamata.
ms.assetid: e2a89f25-15f0-4f3c-9ac8-1e6b72c0d8db
title: Costanti LINECALLPARTYID_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5dd8cca75fe6e91b97fac63dca6c0fdda554394
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332896"
---
# <a name="linecallpartyid_-constants"></a>\_Costanti LINECALLPARTYID

Le costanti del flag di bit **LINECALLPARTYID \_** descrivono la natura delle informazioni disponibili sulle entità coinvolte in una chiamata.

<dl> <dt>

<span id="LINECALLPARTYID_ADDRESS"></span><span id="linecallpartyid_address"></span>**\_Indirizzo LINECALLPARTYID**
</dt> <dd> <dl> <dt>



Le informazioni sull'identificatore dell'entità sono costituite dall'indirizzo dell'entità nel formato di indirizzo canonico o nel formato di indirizzo di composizione.


</dt> </dl> </dd> <dt>

<span id="LINECALLPARTYID_BLOCKED"></span><span id="linecallpartyid_blocked"></span>**LINECALLPARTYID \_ bloccati**
</dt> <dd> <dl> <dt>



Le informazioni sull'identificatore dell'entità non sono disponibili perché sono state bloccate dalla parte remota.


</dt> </dl> </dd> <dt>

<span id="LINECALLPARTYID_NAME"></span><span id="linecallpartyid_name"></span>**\_nome LINECALLPARTYID**
</dt> <dd> <dl> <dt>



Le informazioni sull'identificatore dell'entità sono costituite dal nome dell'entità, ad esempio da una directory mantenuta all'interno dell'opzione.


</dt> </dl> </dd> <dt>

<span id="LINECALLPARTYID_OUTOFAREA"></span><span id="linecallpartyid_outofarea"></span>**\_OUTOFAREA LINECALLPARTYID**
</dt> <dd> <dl> <dt>



Le informazioni relative all'ID chiamante per la chiamata non sono disponibili perché la rete non viene propagata.


</dt> </dl> </dd> <dt>

<span id="LINECALLPARTYID_PARTIAL"></span><span id="linecallpartyid_partial"></span>**LINECALLPARTYID \_ parziale**
</dt> <dd> <dl> <dt>



Le informazioni sull'identificatore dell'entità sono valide ma sono limitate solo a informazioni parziali.


</dt> </dl> </dd> <dt>

<span id="LINECALLPARTYID_UNAVAIL"></span><span id="linecallpartyid_unavail"></span>**LINECALLPARTYID non \_ disponibile**
</dt> <dd> <dl> <dt>



Le informazioni sull'identificatore dell'entità non sono disponibili e non saranno disponibili in un secondo momento. Le informazioni potrebbero non essere disponibili per motivi non specificati. Ad esempio, le informazioni non sono state recapitate dalla rete, ma sono state ignorate dal provider di servizi e così via.


</dt> </dl> </dd> <dt>

<span id="LINECALLPARTYID_UNKNOWN"></span><span id="linecallpartyid_unknown"></span>**LINECALLPARTYID \_ sconosciuto**
</dt> <dd> <dl> <dt>



Le informazioni sull'identificatore dell'entità sono attualmente sconosciute, ma possono essere note successivamente.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

Nessuna estensibilità. Tutti i 32 bit sono riservati.

Per ognuna delle entità possibili coinvolte in una chiamata, le **costanti \_ LINECALLPARTYID** descrivono come vengono formattate le informazioni sull'identificatore dell'entità. Queste informazioni vengono fornite nella struttura dei dati [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2,0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




