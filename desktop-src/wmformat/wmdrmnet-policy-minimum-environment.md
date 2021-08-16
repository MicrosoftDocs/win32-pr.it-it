---
title: WMDRMNET_POLICY_MINIMUM_ENVIRONMENT struttura (Wmdrmsdk.h)
description: La struttura MINIMUM ENVIRONMENT dei criteri WMDRMNET contiene i requisiti minimi di sicurezza per Windows \_ \_ Media \_ DRM per i dispositivi di rete.
ms.assetid: b1bc9a8d-197e-45fe-a152-0b81add977eb
keywords:
- WMDRMNET_POLICY_MINIMUM_ENVIRONMENT struttura windows Media Format
- struttura windows Media Format
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
ms.openlocfilehash: 26c11cf02d7cfcd2e3ab62c4e6b110e2c20b77cf6f79251a23f642b38d4df553
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118027462"
---
# <a name="wmdrmnet_policy_minimum_environment-structure"></a>Struttura DELL'AMBIENTE \_ \_ MINIMO DEI CRITERI WMDRMNET \_

La struttura MINIMUM ENVIRONMENT di **\_ CRITERI \_ \_ WMDRMNET** contiene i requisiti minimi di sicurezza per Windows DRM multimediale per i dispositivi di rete.

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

Livello minimo di sicurezza dell'applicazione richiesto.

</dd> <dt>

**dwMinimumAppRevocationListVersion**
</dt> <dd>

Versione minima dell'elenco di revoche di certificati dell'applicazione richiesta.

</dd> <dt>

**dwMinimumDeviceRevocationListVersion**
</dt> <dd>

È necessario un elenco minimo di revoche di certificati del dispositivo.

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

 

 





