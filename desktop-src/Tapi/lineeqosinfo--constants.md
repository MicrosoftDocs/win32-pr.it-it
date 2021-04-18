---
description: Queste costanti vengono utilizzate da un TSP per identificare il risultato di una richiesta QoS (Quality of Service).
ms.assetid: 617ddbf4-212f-4990-93c2-f38f04b035ab
title: Costanti LINEEQOSINFO_ (TSPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 423cc6172a1c6c87c1f3bb38929f727a15dad5c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331594"
---
# <a name="lineeqosinfo_-constants"></a>\_Costanti LINEEQOSINFO

Queste costanti vengono utilizzate da un TSP per identificare il risultato di una richiesta QoS (Quality of Service).

<dl> <dt>

<span id="LINEEQOSINFO_NOQOS"></span><span id="lineeqosinfo_noqos"></span>**\_NOQOS LINEEQOSINFO**
</dt> <dd> <dl> <dt>

 0x00000001
</dt> <dt>



QoS non è disponibile.


</dt> </dl> </dd> <dt>

<span id="LINEEQOSINFO_ADMISSIONFAILURE"></span><span id="lineeqosinfo_admissionfailure"></span>**\_ADMISSIONFAILURE LINEEQOSINFO**
</dt> <dd> <dl> <dt>

 0x00000002
</dt> <dt>



Non è stato possibile soddisfare la richiesta QoS.


</dt> </dl> </dd> <dt>

<span id="LINEEQOSINFO_POLICYFAILURE"></span><span id="lineeqosinfo_policyfailure"></span>**\_POLICYFAILURE LINEEQOSINFO**
</dt> <dd> <dl> <dt>

 0x00000003
</dt> <dt>



Il tipo di QoS richiesto non è supportato.


</dt> </dl> </dd> <dt>

<span id="LINEEQOSINFO_GENERICERROR"></span><span id="lineeqosinfo_genericerror"></span>**\_errore generico LINEEQOSINFO**
</dt> <dd> <dl> <dt>

 0x00000004
</dt> <dt>



Errore QoS non specificato.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2,2<br/>                                                      |
| Intestazione<br/>       | <dl> <dt>TSPI. h</dt> </dl> |



 

 




