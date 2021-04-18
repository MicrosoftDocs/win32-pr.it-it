---
title: Struttura WMDRMNET_POLICY_GLOBAL_REQUIREMENTS (wmdrmsdk. h)
description: La \_ struttura dei \_ requisiti globali del criterio WMDRMNET include i \_ requisiti globali per Windows Media DRM per i dispositivi di rete.
ms.assetid: 140b3a6f-ccba-4735-b48a-2e990f5ec570
keywords:
- Formato di Windows Media per la struttura WMDRMNET_POLICY_GLOBAL_REQUIREMENTS
- struttura Windows Media Format
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
ms.openlocfilehash: 0ccf13c881c9696d970a00ac902f3f8d08f13c58
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325531"
---
# <a name="wmdrmnet_policy_global_requirements-structure"></a>\_Struttura dei \_ requisiti globali dei criteri WMDRMNET \_

La struttura dei **\_ \_ \_ requisiti globali del criterio WMDRMNET** include i requisiti globali per Windows Media DRM per i dispositivi di rete.

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

[**WMDRMNET \_ Struttura \_ di \_ ambiente minima dei criteri**](wmdrmnet-policy-minimum-environment.md) contenente i requisiti minimi di sicurezza per Windows Media DRM per i dispositivi di rete.

</dd> </dl>

## <a name="remarks"></a>Commenti

Nessuna.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Strutture**](drm-structures.md)
</dt> <dt>

[**criteri di WMDRMNET \_**](wmdrmnet-policy.md)
</dt> </dl>

 

 





