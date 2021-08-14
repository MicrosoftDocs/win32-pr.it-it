---
title: WMDRMNET_POLICY_TRANSCRYPTPLAY struttura (Wmdrmsdk.h)
description: La struttura TRANSCRYPTPLAY di WMDRMNET POLICY contiene le informazioni sui criteri per la riproduzione del contenuto \_ \_ Windows DRM multimediale per i dispositivi di rete.
ms.assetid: 95671c58-a593-40bb-856e-28ad1cba340e
keywords:
- WMDRMNET_POLICY_TRANSCRYPTPLAY struttura windows Media Format
- Struttura windows Media Format
topic_type:
- apiref
api_name:
- WMDRMNET_POLICY_TRANSCRYPTPLAY
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8fe64c796a1f2f15e4733e7dd3d82e918306fb95d78c61fb85ad2d813d946d60
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118195506"
---
# <a name="wmdrmnet_policy_transcryptplay-structure"></a>Struttura \_ TRANSCRYPTPLAY di CRITERI \_ WMDRMNET

La **struttura \_ \_ TRANSCRYPTPLAY di WMDRMNET POLICY** contiene le informazioni sui criteri per la riproduzione del contenuto Windows DRM multimediale per dispositivi di rete.

## <a name="syntax"></a>Sintassi


```C++
typedef struct WMDRMNET_POLICY_TRANSCRYPTPLAY {
  WMDRMNET_POLICY_GLOBAL_REQUIREMENTS globals;
  WMDRMNET_POLICY_PLAY_OPL            playOPLs;
} ;
```



## <a name="members"></a>Members

<dl> <dt>

**Globals**
</dt> <dd>

Struttura dei criteri globali.

</dd> <dt>

**playOPLs**
</dt> <dd>

Livelli di protezione dell'output per la riproduzione. **WMDRMNET \_ POLICY \_ PLAY \_ OPL** è un tipo definito [**come DRM PLAY \_ \_ OPL \_ EX.**](drm-play-opl-ex.md)

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

[**CRITERI WMDRMNET \_**](wmdrmnet-policy.md)
</dt> </dl>

 

 





