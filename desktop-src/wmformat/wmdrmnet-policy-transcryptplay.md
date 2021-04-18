---
title: Struttura WMDRMNET_POLICY_TRANSCRYPTPLAY (wmdrmsdk. h)
description: La \_ struttura WMDRMNET Policy \_ TRANSCRYPTPLAY include le informazioni sui criteri per la riproduzione di contenuto con Windows Media DRM per i dispositivi di rete.
ms.assetid: 95671c58-a593-40bb-856e-28ad1cba340e
keywords:
- Formato di Windows Media per la struttura WMDRMNET_POLICY_TRANSCRYPTPLAY
- struttura Windows Media Format
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
ms.openlocfilehash: 0681251428b87b323c9ad3e73277ec8cdd2b95f0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324815"
---
# <a name="wmdrmnet_policy_transcryptplay-structure"></a>\_Struttura TRANSCRYPTPLAY del criterio WMDRMNET \_

La struttura **WMDRMNET \_ policy \_ TRANSCRYPTPLAY** include le informazioni sui criteri per la riproduzione di contenuto con Windows Media DRM per i dispositivi di rete.

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

Livelli di protezione dell'output per la riproduzione. **WMDRMNET \_ POLICY \_ Play \_ OPL** è un tipo definito come [**DRM \_ Play \_ OPL \_ ex**](drm-play-opl-ex.md).

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

 

 





