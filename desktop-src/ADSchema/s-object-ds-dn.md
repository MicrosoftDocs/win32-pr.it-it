---
title: Sintassi dell'oggetto (DS-DN)
description: Stringa che contiene un nome distinto (DN).
ms.assetid: 089104c4-ff82-49ea-a8db-a6dadc3a18bc
ms.tgt_platform: multiple
keywords:
- Oggetto (DS-DN) sintassi di AD schema
topic_type:
- apiref
api_name:
- Object(DS-DN)
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45154985fa7fbfc4d95d563196357d43eac2ea72
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104519350"
---
# <a name="objectds-dn-syntax"></a>Sintassi dell'oggetto (DS-DN)

Stringa che contiene un nome distinto (DN). Per gli attributi con questa sintassi, Active Directory gestisce i valori di attributo come riferimenti all'oggetto identificato dal DN e aggiorna automaticamente il valore se l'oggetto viene spostato o rinominato. Per le query che includono attributi della sintassi DN in un filtro, specificare nomi distinti completi. I caratteri jolly (ad esempio, CN = John \* ) non sono supportati.



| Voce | Valore |
|--------------|------------------------------------------------------------------------|
| Nome         | Object(DS-DN)                                                           |
| ID sintassi    | 2.5.5.1                                                                |
| ID OM        | 127                                                                    |
| Tipo MAPI    | OBJECT                                                                 |
| Tipo di annunci     | \_stringa DN \_ ADSTYPE                                                    |
| Tipo Variant | \_BSTR VT                                                               |
| Tipo SDS     | [System.String](/dotnet/api/system.string) |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[System.String](/dotnet/api/system.string)
</dt> </dl>

 

 
