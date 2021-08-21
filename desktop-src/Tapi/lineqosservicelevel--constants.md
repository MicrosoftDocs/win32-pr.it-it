---
description: Queste costanti vengono usate da un TSP per identificare il tipo di livello QoS (Quality of Service) richiesto.
ms.assetid: 9fc3f6eb-7103-43c5-84f8-3842757e5be7
title: LINEQOSSERVICELEVEL_ costanti (Tspi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a74a4508b54a8b56e8e9cb359f966122c5c009f0e5ede0f1b8544cd1e46330c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003009"
---
# <a name="lineqosservicelevel_-constants"></a>Costanti LINEQOSSERVICELEVEL \_

Queste costanti vengono usate da un TSP per identificare il tipo di livello QoS (Quality of Service) richiesto.

<dl> <dt>

<span id="LINEQOSSERVICELEVEL_NEEDED"></span><span id="lineqosservicelevel_needed"></span>**LINEQOSSERVICELEVEL \_ NECESSARIO**
</dt> <dd> <dl> <dt>

 0x00000001
</dt> <dt>



La qualità del livello di servizio richiesto è un requisito.


</dt> </dl> </dd> <dt>

<span id="LINEQOSSERVICELEVEL_IFAVAILABLE"></span><span id="lineqosservicelevel_ifavailable"></span>**LINEQOSSERVICELEVEL \_ IFAVAILABLE**
</dt> <dd> <dl> <dt>

 0x00000002
</dt> <dt>



La qualità del livello di servizio richiesto, se disponibile.


</dt> </dl> </dd> <dt>

<span id="LINEQOSSERVICELEVEL_BESTEFFORT"></span><span id="lineqosservicelevel_besteffort"></span>**LINEQOSSERVICELEVEL \_ BESTEFFORT**
</dt> <dd> <dl> <dt>

 0x00000003
</dt> <dt>



La qualità del livello di servizio richiesto è "il massimo sforzo".


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2.2<br/>                                                      |
| Intestazione<br/>       | <dl> <dt>Tspi.h</dt> </dl> |



 

 




