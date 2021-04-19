---
description: Queste costanti vengono utilizzate da un TSP per identificare il tipo di livello di QoS (Quality of Service) obbligatorio.
ms.assetid: 9fc3f6eb-7103-43c5-84f8-3842757e5be7
title: Costanti LINEQOSSERVICELEVEL_ (TSPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c0629715e461a15e21e1730f86edb61d83d60db
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331249"
---
# <a name="lineqosservicelevel_-constants"></a>\_Costanti LINEQOSSERVICELEVEL

Queste costanti vengono utilizzate da un TSP per identificare il tipo di livello di QoS (Quality of Service) obbligatorio.

<dl> <dt>

<span id="LINEQOSSERVICELEVEL_NEEDED"></span><span id="lineqosservicelevel_needed"></span>**LINEQOSSERVICELEVEL \_ necessario**
</dt> <dd> <dl> <dt>

 0x00000001
</dt> <dt>



La qualità del livello di servizio richiesto è un requisito.


</dt> </dl> </dd> <dt>

<span id="LINEQOSSERVICELEVEL_IFAVAILABLE"></span><span id="lineqosservicelevel_ifavailable"></span>**\_IFAVAILABLE LINEQOSSERVICELEVEL**
</dt> <dd> <dl> <dt>

 0x00000002
</dt> <dt>



Qualità del livello di servizio necessario, se disponibile.


</dt> </dl> </dd> <dt>

<span id="LINEQOSSERVICELEVEL_BESTEFFORT"></span><span id="lineqosservicelevel_besteffort"></span>**\_BESTEFFORT LINEQOSSERVICELEVEL**
</dt> <dd> <dl> <dt>

 0x00000003
</dt> <dt>



La qualità del livello di servizio richiesto è "Best Effort".


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2,2<br/>                                                      |
| Intestazione<br/>       | <dl> <dt>TSPI. h</dt> </dl> |



 

 




