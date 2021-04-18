---
title: Struttura WMDRMNET_POLICY_MINIMUM_ENVIRONMENT (wmdrmsdk. h)
description: La \_ \_ struttura di ambiente minima dei criteri WMDRMNET \_ contiene i requisiti di sicurezza minimi per Windows Media DRM per i dispositivi di rete.
ms.assetid: b1bc9a8d-197e-45fe-a152-0b81add977eb
keywords:
- Formato di Windows Media per la struttura WMDRMNET_POLICY_MINIMUM_ENVIRONMENT
- struttura Windows Media Format
topic_type:
- apiref
api_name:
- WMDRMNET_POLICY_MINIMUM_ENVIRONMENT
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4bf53fdec186a44eff375dd2e9cf9badfe0ba715
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330879"
---
# <a name="wmdrmnet_policy_minimum_environment-structure"></a>\_Struttura di \_ ambiente minima dei criteri WMDRMNET \_

La struttura di **\_ \_ \_ ambiente minima dei criteri WMDRMNET** contiene i requisiti di sicurezza minimi per Windows Media DRM per i dispositivi di rete.

## <a name="syntax"></a>Sintassi


```C++
typedef struct WMDRMNET_POLICY_MINIMUM_ENVIRONMENT {
  WORD  wMinimumSecurityLevel;
  DWORD dwMinimumAppRevocationListVersion;
  DWORD dwMinimumDeviceRevocationListVersion;
} ;
```



## <a name="members"></a>Members

<dl> <dt>

**wMinimumSecurityLevel**
</dt> <dd>

È necessario un livello di sicurezza minimo per l'applicazione.

</dd> <dt>

**dwMinimumAppRevocationListVersion**
</dt> <dd>

È richiesta la versione minima dell'elenco di revoche di certificati dell'applicazione.

</dd> <dt>

**dwMinimumDeviceRevocationListVersion**
</dt> <dd>

È necessario un elenco di revoche di certificati minimo per il dispositivo.

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

 

 





