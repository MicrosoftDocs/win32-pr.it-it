---
title: Enumerazione WMDRMNET_POLICY_TYPE (wmdrmsdk. h)
description: Il \_ \_ tipo di enumerazione tipo di criteri WMDRMNET elenca i tipi di criteri disponibili per le operazioni di Windows Media DRM per i dispositivi di rete.
ms.assetid: 83e9e247-3bd8-4857-97b6-95b3cd5ad25c
keywords:
- Formato Windows Media enumerazione WMDRMNET_POLICY_TYPE
- Enumerazione formato Windows Media
topic_type:
- apiref
api_name:
- WMDRMNET_POLICY_TYPE
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 964a3e938caa312f02f21074f046f3cf88d72de6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330878"
---
# <a name="wmdrmnet_policy_type-enumeration"></a>Enumerazione del tipo di \_ criteri WMDRMNET \_

Il tipo di enumerazione **\_ \_ tipo di criteri WMDRMNET** elenca i tipi di criteri disponibili per le operazioni di Windows Media DRM per i dispositivi di rete.

## <a name="syntax"></a>Sintassi


```C++
typedef enum WMDRMNET_POLICY_TYPE { 
  WMDRMNET_POLICY_TYPE_UNDEFINED       = 0x0000,
  WMDRMNET_POLICY_TYPE_TRANSCRYPTPLAY  = 0x0001
} ;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="WMDRMNET_POLICY_TYPE_UNDEFINED"></span><span id="wmdrmnet_policy_type_undefined"></span>**tipo di criteri WMDRMNET non \_ \_ \_ definito**
</dt> <dd>

I tipi di criteri non definiti non sono supportati.

</dd> <dt>

<span id="WMDRMNET_POLICY_TYPE_TRANSCRYPTPLAY"></span><span id="wmdrmnet_policy_type_transcryptplay"></span>**\_tipo di criteri WMDRMNET \_ \_ TRANSCRYPTPLAY**
</dt> <dd>

Il criterio regola la capacità di convertire il contenuto protetto da DRM di Windows Media in DRM Windows Media protetto per i dati dei dispositivi di rete e riprodurlo in un dispositivo di rete.

</dd> </dl>

## <a name="remarks"></a>Commenti

Nessuna.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Tipi di enumerazione**](drm-enumeration-types.md)
</dt> <dt>

[**criteri di WMDRMNET \_**](wmdrmnet-policy.md)
</dt> </dl>

 

 





