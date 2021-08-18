---
title: WINBIO_ANTI_SPOOF_POLICY_ACTION enumerazione (Winbio \_ types.h)
description: Specifica i tipi di azioni eseguite per i criteri di antispoofing di un utente.
ms.assetid: 846C0725-1796-49E4-883C-44AC7D618317
keywords:
- WINBIO_ANTI_SPOOF_POLICY_ACTION di enumerazione Windows'API Biometric Framework
- PWINBIO_ANTI_SPOOF_POLICY puntatore di enumerazione Windows'API Biometric Framework
topic_type:
- apiref
api_name:
- WINBIO_ANTI_SPOOF_POLICY_ACTION
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f65fec198a0784bf076eb90224318bd36a88ba3ed96258ffd2014a27da5c8f8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118911270"
---
# <a name="winbio_anti_spoof_policy_action-enumeration"></a>Enumerazione DELLE AZIONI DEI CRITERI \_ ANTI \_ SPOOF \_ \_ DI WINBIO

Specifica i tipi di azioni eseguite per i criteri di antispoofing di un utente.

## <a name="syntax"></a>Sintassi


```C++
typedef enum _WINBIO_ANTI_SPOOF_POLICY_ACTION { 
  WINBIO_ANTI_SPOOF_DISABLE  = 0x00000000,
  WINBIO_ANTI_SPOOF_ENABLE   = 0x00000001,
  WINBIO_ANTI_SPOOF_REMOVE   = 0x00000002
} WINBIO_ANTI_SPOOF_POLICY_ACTION, *PWINBIO_ANTI_SPOOF_POLICY;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="WINBIO_ANTI_SPOOF_DISABLE"></span><span id="winbio_anti_spoof_disable"></span>**WINBIO \_ ANTI \_ SPOOF \_ DISABLE**
</dt> <dd>

Disattiva il rilevamento dello spoofing per un fattore biometrico.

</dd> <dt>

<span id="WINBIO_ANTI_SPOOF_ENABLE"></span><span id="winbio_anti_spoof_enable"></span>**WINBIO \_ ANTI \_ SPOOF \_ ENABLE**
</dt> <dd>

Attiva il rilevamento dello spoofing per un fattore biometrico.

</dd> <dt>

<span id="WINBIO_ANTI_SPOOF_REMOVE"></span><span id="winbio_anti_spoof_remove"></span>**RIMOZIONE DI WINBIO \_ ANTI \_ SPOOF \_**
</dt> <dd>

Rimuove dall'account l'intero criterio antispoofing per il fattore biometrico.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 10 solo app desktop\]<br/>                                                                                                                              |
| Server minimo supportato<br/> | \[Windows Server 2016 solo app desktop\]<br/>                                                                                                                     |
| Intestazione<br/>                   | <dl> <dt>Winbio \_ types.h (includere Winbio.h per le applicazioni client o Adapters.h Winbio \_ per gli adapter)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**AZIONE DEI CRITERI \_ ANTI \_ \_ SPOOFING WINBIO \_**](winbio-anti-spoof-policy-action.md)
</dt> <dt>

[**ORIGINE DEI CRITERI WINBIO \_ \_**](winbio-policy-source.md)
</dt> </dl>

 

 





