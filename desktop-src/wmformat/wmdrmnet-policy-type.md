---
title: WMDRMNET_POLICY_TYPE enumerazione (Wmdrmsdk.h)
description: Il tipo di enumerazione WMDRMNET POLICY TYPE elenca i tipi di criteri disponibili per le Windows \_ \_ media DRM per le operazioni dei dispositivi di rete.
ms.assetid: 83e9e247-3bd8-4857-97b6-95b3cd5ad25c
keywords:
- WMDRMNET_POLICY_TYPE enumerazione Windows Media Format
- enumeration windows Media Format
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
ms.openlocfilehash: 8aec574717abb51117b142b8450ad7548d84766b4138f76a4296982422462fbc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118697813"
---
# <a name="wmdrmnet_policy_type-enumeration"></a>Enumerazione WMDRMNET \_ POLICY \_ TYPE

Il **tipo di enumerazione WMDRMNET \_ POLICY \_ TYPE** elenca i tipi di criteri disponibili per le Windows DRM multimediale per le operazioni dei dispositivi di rete.

## <a name="syntax"></a>Sintassi


```C++
typedef enum WMDRMNET_POLICY_TYPE { 
  WMDRMNET_POLICY_TYPE_UNDEFINED       = 0x0000,
  WMDRMNET_POLICY_TYPE_TRANSCRYPTPLAY  = 0x0001
} ;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="WMDRMNET_POLICY_TYPE_UNDEFINED"></span><span id="wmdrmnet_policy_type_undefined"></span>**TIPO DI CRITERI WMDRMNET \_ \_ NON \_ DEFINITO**
</dt> <dd>

I tipi di criteri non definiti non sono supportati.

</dd> <dt>

<span id="WMDRMNET_POLICY_TYPE_TRANSCRYPTPLAY"></span><span id="wmdrmnet_policy_type_transcryptplay"></span>**TIPO DI CRITERI WMDRMNET \_ \_ \_ TRANSCRYPTPLAY**
</dt> <dd>

I criteri regolano la possibilità di convertire il contenuto protetto da Windows Media DRM in dati Windows Media DRM per dispositivi di rete e riprodurli in un dispositivo di rete.

</dd> </dl>

## <a name="remarks"></a>Commenti

Nessuno.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Tipi di enumerazione**](drm-enumeration-types.md)
</dt> <dt>

[**CRITERI \_ WMDRMNET**](wmdrmnet-policy.md)
</dt> </dl>

 

 





