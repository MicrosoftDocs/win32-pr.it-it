---
title: WMDRMNET_POLICY_GLOBAL_REQUIREMENTS struttura (Wmdrmsdk.h)
description: La struttura DEI REQUISITI GLOBALI DEI CRITERI WMDRMNET include i requisiti globali per Windows \_ \_ \_ DRM multimediale per i dispositivi di rete.
ms.assetid: 140b3a6f-ccba-4735-b48a-2e990f5ec570
keywords:
- WMDRMNET_POLICY_GLOBAL_REQUIREMENTS struttura windows Media Format
- struttura windows Media Format
topic_type:
- apiref
api_name:
- WMDRMNET_POLICY_GLOBAL_REQUIREMENTS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e2a8dc7be95638e171126eb4a55c50744ee3e5126d3e0b49eb8f229ec0257e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117843972"
---
# <a name="wmdrmnet_policy_global_requirements-structure"></a>Struttura DEI REQUISITI GLOBALI DEI CRITERI WMDRMNET \_ \_ \_

La **struttura WMDRMNET \_ POLICY GLOBAL \_ \_ REQUIREMENTS** contiene i requisiti globali per Windows DRM multimediale per i dispositivi di rete.

## <a name="syntax"></a>Sintassi


```C++
typedef struct WMDRMNET_POLICY_GLOBAL_REQUIREMENTS {
  WMDRMNET_POLICY_MINIMUM_ENVIRONMENT MinimumEnvironment;
} ;
```



## <a name="members"></a>Members

<dl> <dt>

**MinimumEnvironment**
</dt> <dd>

[**WMDRMNET \_ Struttura \_ POLICY MINIMUM \_ ENVIRONMENT**](wmdrmnet-policy-minimum-environment.md) contenente i requisiti minimi di sicurezza per Windows Media DRM per i dispositivi di rete.

</dd> </dl>

## <a name="remarks"></a>Commenti

Nessuno.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Strutture**](drm-structures.md)
</dt> <dt>

[**CRITERI \_ WMDRMNET**](wmdrmnet-policy.md)
</dt> </dl>

 

 





