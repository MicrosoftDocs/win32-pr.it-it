---
title: Struttura WINBIO_ANTI_SPOOF_POLICY ( \_ tipi WINBIO. h)
description: Rappresenta i criteri di antispoofing per un utente.
ms.assetid: 2B433AE8-21A0-4AF1-853C-9074527DB2E4
keywords:
- Struttura di WINBIO_ANTI_SPOOF_POLICY Windows Biometric Framework API
- API Windows Biometric Framework puntatore alla struttura PWINBIO_ANTI_SPOOF_POLICY
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
ms.openlocfilehash: 3da8b7811afb1de1ad464675125f125ef0ceab73
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477500"
---
# <a name="winbio_anti_spoof_policy-structure"></a>\_Struttura dei criteri anti- \_ spoofing WINBIO \_

Rappresenta i criteri di antispoofing per un utente.

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

Tipo di azione da eseguire per i criteri di antispoofing.

</dd> <dt>

**Origine**
</dt> <dd>

Origine per i criteri di antispoofing.

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
</dt> <dt>

[**\_risultato asincrono \_ WINBIO**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result)
</dt> <dt>

[**WinBioGetProperty**](/windows/desktop/api/Winbio/nf-winbio-winbiogetproperty)
</dt> <dt>

[**WinBioSetProperty**](/windows/desktop/api/winbio/nf-winbio-winbiosetproperty)
</dt> </dl>

 

 





