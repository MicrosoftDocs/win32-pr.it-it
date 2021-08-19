---
title: WMDRMNET_POLICY struttura (Wmdrmsdk.h)
description: La struttura DEI CRITERI WMDRMNET contiene i criteri da usare per Windows DRM multimediale \_ per le operazioni dei dispositivi di rete.
ms.assetid: 11eaaeb2-3470-4f58-ae1c-53ee0f60bdce
keywords:
- WMDRMNET_POLICY struttura windows Media Format
- Struttura windows Media Format
topic_type:
- apiref
api_name:
- WMDRMNET_POLICY
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf648ef5e300fa9fef1cf12fd4698f4ec196f62130bf75a02f263cd96931f0bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117653424"
---
# <a name="wmdrmnet_policy-structure"></a>Struttura DEI CRITERI \_ WMDRMNET

La **struttura DEI \_ CRITERI WMDRMNET** contiene i criteri da usare per Windows DRM multimediale per le operazioni dei dispositivi di rete.

## <a name="syntax"></a>Sintassi


```C++
typedef struct WMDRMNET_POLICY {
  WMDRMNET_POLICY_TYPE ePolicyType;
  BYTE                 *pbPolicy;
} ;
```



## <a name="members"></a>Members

<dl> <dt>

**ePolicyType**
</dt> <dd>

Membro [**dell'enumerazione WMDRMNET \_ POLICY \_ TYPE**](wmdrmnet-policy-type.md) che specifica il tipo di criteri.

</dd> <dt>

**pbPolicy**
</dt> <dd>

Buffer contenente i criteri. L'unico tipo di criterio attualmente supportato è **WMDRMNET \_ POLICY \_ TYPE \_ TRANSCRYPTPLAY.** Questo membro è un puntatore a una **struttura \_ \_ TRANSCRYPTPLAY di CRITERI WMDRMNET.**

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa struttura viene usata come parametro per il [**metodo IWMDRMNetTransmitter::GetLeafLicenseResponse.**](iwmdrmnettransmitter-getleaflicenseresponse.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Strutture**](drm-structures.md)
</dt> <dt>

[**REQUISITI GLOBALI DEI CRITERI WMDRMNET \_ \_ \_**](wmdrmnet-policy-global-requirements.md)
</dt> <dt>

[**AMBIENTE MINIMO DEI CRITERI WMDRMNET \_ \_ \_**](wmdrmnet-policy-minimum-environment.md)
</dt> <dt>

[**TRANSCRYPTPLAY \_ DEI CRITERI \_ WMDRMNET**](wmdrmnet-policy-transcryptplay.md)
</dt> <dt>

[**TIPO DI CRITERI WMDRMNET \_ \_**](wmdrmnet-policy-type.md)
</dt> </dl>

 

 





