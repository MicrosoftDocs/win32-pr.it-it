---
title: Sintassi String(Generalized-Time)
description: Formato di stringa temporale definito dagli standard ASN.1. | Sintassi String(Generalized-Time)
ms.assetid: c69ab29b-5877-47d4-b58d-4f103758dfac
ms.tgt_platform: multiple
keywords:
- Schema AD della sintassi String(Generalized-Time)
topic_type:
- apiref
api_name:
- String(Generalized-Time)
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19bf7d965b03b75f4186b807098a5262c402d0c19104a4c09357958b38a77a73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119580211"
---
# <a name="stringgeneralized-time-syntax"></a>Sintassi String(Generalized-Time)

Formato di stringa temporale definito dagli standard ASN.1. Usare questa sintassi per archiviare i valori di ora Generalized-Time formato.

Il formato della sintassi Generalized-Time è "AAAAMMGGHHMMSS.0Z". Un esempio di valore accettabile è "20010928060000.0Z". La "Z" non indica differenze di tempo. Active Directory archivia data/ora come ora di Greenwich (GMT). Se non viene specificato alcun differenziale di ora, GMT è l'impostazione predefinita.

Se l'ora viene specificata in un fuso orario diverso da GMT, il differenziale tra il fuso orario e GMT viene aggiunto alla stringa anziché "Z" nel formato "YYYYMMDDHHMMSS.0 \[ +/- \] HHMM". Un esempio di valore accettabile è "20010928060000.0+0200". Il differenziale si basa sulla formula GMT=Local+differenziale.

Per altre informazioni, vedere ISO 8601 e X680.



| Voce | Valore |
|--------------|----------------------------------------------------------------------------|
| Nome         | String(Generalized-Time)                                                   |
| ID sintassi    | 2.5.5.11                                                                   |
| OM ID        | 24                                                                         |
| Tipo MAPI    | SYSTIME                                                                    |
| Tipo di ADS     | ORA UTC ADSTYPE \_ \_                                                         |
| Tipo variant | DATA \_ VT                                                                   |
| Tipo SDS     | [System.DateTime](/dotnet/api/system.datetime) |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[System.DateTime](/dotnet/api/system.datetime)
</dt> </dl>

 

 
