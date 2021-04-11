---
title: Sintassi stringa (generalizzata-Time)
description: Formato di stringa dell'ora definito dagli standard ASN. 1. | Sintassi stringa (generalizzata-Time)
ms.assetid: c69ab29b-5877-47d4-b58d-4f103758dfac
ms.tgt_platform: multiple
keywords:
- Stringa (generalizzata-ora) sintassi di AD schema
topic_type:
- apiref
api_name:
- String(Generalized-Time)
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81e754fe622d3ff6f010521b7bc9b9e4ff7a5f34
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104234705"
---
# <a name="stringgeneralized-time-syntax"></a>Sintassi stringa (generalizzata-Time)

Formato di stringa dell'ora definito dagli standard ASN. 1. Usare questa sintassi per archiviare i valori temporali nel formato Generalized-Time.

Il formato della sintassi del Generalized-Time è "ad aaaammgghhmmss. 0Z". Un esempio di valore accettabile è "20010928060000.0 Z". "Z" indica nessun differenziale temporale. Active Directory archivia data/ora come ora di Greenwich (GMT). Se non viene specificato alcun intervallo di tempo, GMT è il valore predefinito.

Se l'ora viene specificata in un fuso orario diverso da GMT, il differenziale tra il fuso orario e il GMT viene aggiunto alla stringa anziché "Z" nel formato "ad aaaammgghhmmss. 0 \[ +/- \] hhmm". Un esempio di valore accettabile è "20010928060000.0 + 0200". Il differenziale è basato sulla formula: GMT = local + differenziale.

Per ulteriori informazioni, vedere ISO 8601 e X680.



| Voce | Valore |
|--------------|----------------------------------------------------------------------------|
| Nome         | String(Generalized-Time)                                                   |
| ID sintassi    | 2.5.5.11                                                                   |
| ID OM        | 24                                                                         |
| Tipo MAPI    | SYSTIME                                                                    |
| Tipo di annunci     | ADSTYPE \_ \_ ora UTC                                                         |
| Tipo Variant | \_Data VT                                                                   |
| Tipo SDS     | [System.DateTime](/dotnet/api/system.datetime) |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[System.DateTime](/dotnet/api/system.datetime)
</dt> </dl>

 

 
