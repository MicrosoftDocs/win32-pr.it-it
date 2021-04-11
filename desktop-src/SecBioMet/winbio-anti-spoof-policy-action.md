---
title: Enumerazione WINBIO_ANTI_SPOOF_POLICY_ACTION ( \_ tipi WINBIO. h)
description: Specifica i tipi di azioni da eseguire per i criteri di antispoofing di un utente.
ms.assetid: 846C0725-1796-49E4-883C-44AC7D618317
keywords:
- WINBIO_ANTI_SPOOF_POLICY_ACTION enumerazione Windows Biometric Framework API
- Puntatore di enumerazione PWINBIO_ANTI_SPOOF_POLICY Windows Biometric Framework API
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
ms.openlocfilehash: 5905624bad252475cdde12c003f31a734e64dd2e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964443"
---
# <a name="winbio_anti_spoof_policy_action-enumeration"></a>\_ \_ \_ Enumerazione azione criterio anti spoofing WINBIO \_

Specifica i tipi di azioni da eseguire per i criteri di antispoofing di un utente.

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

<span id="WINBIO_ANTI_SPOOF_DISABLE"></span><span id="winbio_anti_spoof_disable"></span>**WINBIO \_ anti \_ spoofing \_ disabilitato**
</dt> <dd>

Disattiva il rilevamento dello spoofing per un fattore biometrico.

</dd> <dt>

<span id="WINBIO_ANTI_SPOOF_ENABLE"></span><span id="winbio_anti_spoof_enable"></span>**WINBIO \_ anti \_ spoofing \_ abilitato**
</dt> <dd>

Attiva il rilevamento dello spoofing per un fattore biometrico.

</dd> <dt>

<span id="WINBIO_ANTI_SPOOF_REMOVE"></span><span id="winbio_anti_spoof_remove"></span>**rimozione di WINBIO \_ anti \_ spoofing \_**
</dt> <dd>

Rimuove l'intero criterio di antispoofing per il fattore biometrico dall'account.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows 10\]<br/>                                                                                                                              |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2016\]<br/>                                                                                                                     |
| Intestazione<br/>                   | <dl> <dt>WinBio \_ types. h (includere WinBio. h per le applicazioni client o WinBio \_ Adapters. h per gli adapter)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_ \_ \_ Azione criterio anti-spoofing WINBIO \_**](winbio-anti-spoof-policy-action.md)
</dt> <dt>

[**\_origine criteri \_ WINBIO**](winbio-policy-source.md)
</dt> </dl>

 

 





