---
title: Struttura WMDRMNET_POLICY (wmdrmsdk. h)
description: La \_ struttura dei criteri WMDRMNET contiene i criteri da usare per le operazioni di Windows Media DRM per i dispositivi di rete.
ms.assetid: 11eaaeb2-3470-4f58-ae1c-53ee0f60bdce
keywords:
- Formato di Windows Media per la struttura WMDRMNET_POLICY
- struttura Windows Media Format
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
ms.openlocfilehash: 574e37a8c5ee7f68291012b86cda3a89e25949ab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324810"
---
# <a name="wmdrmnet_policy-structure"></a>\_Struttura dei criteri WMDRMNET

La struttura dei **\_ criteri WMDRMNET** contiene i criteri da usare per le operazioni di Windows Media DRM per i dispositivi di rete.

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

Membro dell'enumerazione [**del \_ \_ tipo di criteri WMDRMNET**](wmdrmnet-policy-type.md) che specifica il tipo di criteri.

</dd> <dt>

**pbPolicy**
</dt> <dd>

Buffer contenente i criteri. L'unico tipo di criteri attualmente supportato è **il \_ tipo di criteri WMDRMNET \_ \_ TRANSCRYPTPLAY**. Questo membro è un puntatore a una **struttura \_ \_ TRANSCRYPTPLAY dei criteri WMDRMNET** .

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa struttura viene utilizzata come parametro per il metodo [**IWMDRMNetTransmitter:: GetLeafLicenseResponse**](iwmdrmnettransmitter-getleaflicenseresponse.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Strutture**](drm-structures.md)
</dt> <dt>

[**\_ \_ requisiti globali del criterio WMDRMNET \_**](wmdrmnet-policy-global-requirements.md)
</dt> <dt>

[**\_ \_ ambiente minimo per i criteri WMDRMNET \_**](wmdrmnet-policy-minimum-environment.md)
</dt> <dt>

[**\_criteri WMDRMNET \_ TRANSCRYPTPLAY**](wmdrmnet-policy-transcryptplay.md)
</dt> <dt>

[**\_tipo di criteri WMDRMNET \_**](wmdrmnet-policy-type.md)
</dt> </dl>

 

 





