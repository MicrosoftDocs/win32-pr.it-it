---
description: Le \_ costanti LINEDIGITMODE descrivono tipi diversi di generazione di cifre inband.
ms.assetid: d603ea28-2b93-4548-bb16-78e93087f828
title: Costanti LINEDIGITMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50bedd7f508368a84ab2fa70fac37c316dcc6c85
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325016"
---
# <a name="linedigitmode_-constants"></a>\_Costanti LINEDIGITMODE

Le **costanti \_ LINEDIGITMODE** descrivono tipi diversi di generazione di cifre inband.

<dl> <dt>

<span id="LINEDIGITMODE_DTMF"></span><span id="linedigitmode_dtmf"></span>**LINEDIGITMODE \_ DTMF**
</dt> <dd> <dl> <dt>



USA i toni DTMF per segnalare le cifre. Le cifre valide sono comprese tra 0 e 9,' \* ',' \# ',' A ',' B ',' c'è d'.


</dt> </dl> </dd> <dt>

<span id="LINEDIGITMODE_DTMFEND"></span><span id="linedigitmode_dtmfend"></span>**\_DTMFEND LINEDIGITMODE**
</dt> <dd> <dl> <dt>



USA i toni DTMF per segnalare le cifre e rilevare i bordi inferiori. Le cifre valide sono comprese tra 0 e 9,' \* ',' \# ',' A ',' B ',' c'è d'.


</dt> </dl> </dd> <dt>

<span id="LINEDIGITMODE_PULSE"></span><span id="linedigitmode_pulse"></span>**\_impulso LINEDIGITMODE**
</dt> <dd> <dl> <dt>



USA sequenze di impulsi rotanti per segnalare le cifre. Le cifre valide sono comprese tra 0 e 9.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

Nessuna estensibilità. Tutti i 32 bit sono riservati.

È possibile specificare una modalità digit durante la generazione o il rilevamento di cifre. Si noti che le cifre a impulsi vengono generate rendendo e suddividendo il circuito del ciclo locale. Questi impulsi vengono assorbiti dall'opzione. Il termine remoto lo osserva semplicemente come una serie di clic audio inband. Il rilevamento di cifre inviate come impulsi deve pertanto essere in grado di rilevare queste sequenze da 1 a 10 clic acustici.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2,0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




