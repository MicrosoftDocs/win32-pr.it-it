---
title: Sintassi di Object(DS-DN)
description: Stringa che contiene un nome distinto (DN).
ms.assetid: 089104c4-ff82-49ea-a8db-a6dadc3a18bc
ms.tgt_platform: multiple
keywords:
- Schema AD della sintassi object(DS-DN)
topic_type:
- apiref
api_name:
- Object(DS-DN)
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad0c9adf4138de56d90ac89743c3b428a1f25b45027bc19f0b5dccc2e005b143
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117835684"
---
# <a name="objectds-dn-syntax"></a>Sintassi di Object(DS-DN)

Stringa che contiene un nome distinto (DN). Per gli attributi con questa sintassi, Active Directory gestisce i valori degli attributi come riferimenti all'oggetto identificato dal DN e aggiorna automaticamente il valore se l'oggetto viene spostato o rinominato. Per le query che includono attributi della sintassi DN in un filtro, specificare nomi distinti completi. I caratteri jolly (ad esempio, cn=John) \* non sono supportati.



| Voce | Valore |
|--------------|------------------------------------------------------------------------|
| Nome         | Object(DS-DN)                                                           |
| ID sintassi    | 2.5.5.1                                                                |
| OM ID        | 127                                                                    |
| Tipo MAPI    | OBJECT                                                                 |
| Tipo di ADS     | STRINGA DN ADSTYPE \_ \_                                                    |
| Tipo variant | VT \_ BSTR                                                               |
| Tipo SDS     | [System.String](/dotnet/api/system.string) |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[System.String](/dotnet/api/system.string)
</dt> </dl>

 

 
