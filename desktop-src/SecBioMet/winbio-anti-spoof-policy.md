---
title: WINBIO_ANTI_SPOOF_POLICY struttura (Winbio \_ types.h)
description: Rappresenta i criteri antispoofing per un utente.
ms.assetid: 2B433AE8-21A0-4AF1-853C-9074527DB2E4
keywords:
- WINBIO_ANTI_SPOOF_POLICY struttura Windows'API Biometric Framework
- PWINBIO_ANTI_SPOOF_POLICY puntatore alla struttura Windows'API Biometric Framework
topic_type:
- apiref
api_name:
- WINBIO_ANTI_SPOOF_POLICY
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28ade20749b105cc3c7f8a92e0904aff1cea860f9175c8b3c6adb113f273f0fd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073251"
---
# <a name="winbio_anti_spoof_policy-structure"></a>Struttura DEI CRITERI \_ DI \_ SPOOFING DI WINBIO \_

Rappresenta i criteri antispoofing per un utente.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _WINBIO_ANTI_SPOOF_POLICY {
  WINBIO_ANTI_SPOOF_POLICY_ACTION Action;
  WINBIO_POLICY_SOURCE            Source;
} WINBIO_ANTI_SPOOF_POLICY, *PWINBIO_ANTI_SPOOF_POLICY;
```



## <a name="members"></a>Members

<dl> <dt>

**Azione**
</dt> <dd>

Tipo di azione da eseguire per i criteri antispoofing.

</dd> <dt>

**Origine**
</dt> <dd>

Origine per i criteri antispoofing.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 10 solo app desktop\]<br/>                                                                                                                              |
| Server minimo supportato<br/> | \[Windows Server 2016 solo app desktop\]<br/>                                                                                                                     |
| Intestazione<br/>                   | <dl> <dt>Winbio \_ types.h (includere Winbio.h per le applicazioni client o Winbio \_ adapters.h per gli adapter)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**AZIONE DEI CRITERI \_ DI \_ SPOOFING DI \_ WINBIO \_**](winbio-anti-spoof-policy-action.md)
</dt> <dt>

[**ORIGINE CRITERI \_ WINBIO \_**](winbio-policy-source.md)
</dt> <dt>

[**RISULTATO \_ ASINCRONO \_ WINBIO**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result)
</dt> <dt>

[**WinBioGetProperty**](/windows/desktop/api/Winbio/nf-winbio-winbiogetproperty)
</dt> <dt>

[**WinBioSetProperty**](/windows/desktop/api/winbio/nf-winbio-winbiosetproperty)
</dt> </dl>

 

 





