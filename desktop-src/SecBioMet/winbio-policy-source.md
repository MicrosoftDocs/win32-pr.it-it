---
title: WINBIO_POLICY_SOURCE enumerazione (Winbio \_ types.h)
description: Elenca le possibili origini di informazioni sui criteri per il rilevamento dello spoofing per i fattori biometrici.
ms.assetid: 3DC3BB0B-1FD7-473C-8E0B-B7E0A4A44E9E
keywords:
- WINBIO_POLICY_SOURCE'Windows API Biometric Framework
- PWINBIO_POLICY_SOURCE puntatore di enumerazione Windows'API Biometric Framework
topic_type:
- apiref
api_name:
- WINBIO_POLICY_SOURCE
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 962d4bc3e8cffb778df56d78a9ddaf0641f57f8f96c8f7b024745a4b879f2f81
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118909935"
---
# <a name="winbio_policy_source-enumeration"></a>Enumerazione WINBIO \_ POLICY \_ SOURCE

Elenca le possibili origini di informazioni sui criteri per il rilevamento dello spoofing per i fattori biometrici.

## <a name="syntax"></a>Sintassi


```C++
typedef enum _WINBIO_POLICY_SOURCE { 
  WINBIO_POLICY_UNKNOWN  = 0x00000000,
  WINBIO_POLICY_DEFAULT  = 0x00000001,
  WINBIO_POLICY_LOCAL    = 0x00000002,
  WINBIO_POLICY_ADMIN    = 0x00000003
} WINBIO_POLICY_SOURCE, *PWINBIO_POLICY_SOURCE;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="WINBIO_POLICY_UNKNOWN"></span><span id="winbio_policy_unknown"></span>**CRITERI WINBIO \_ \_ SCONOSCIUTI**
</dt> <dd>

L'origine dei criteri è sconosciuta.

</dd> <dt>

<span id="WINBIO_POLICY_DEFAULT"></span><span id="winbio_policy_default"></span>**IMPOSTAZIONE PREDEFINITA DEI CRITERI WINBIO \_ \_**
</dt> <dd>

I criteri sono i criteri predefiniti forniti dall'Windows Biometric Framework.

</dd> <dt>

<span id="WINBIO_POLICY_LOCAL"></span><span id="winbio_policy_local"></span>**CRITERI WINBIO \_ \_ LOCALI**
</dt> <dd>

Criteri impostati dal singolo utente per il proprio account usando l'app **Impostazioni** app. Questo criterio esegue l'override dei criteri predefiniti.

</dd> <dt>

<span id="WINBIO_POLICY_ADMIN"></span><span id="winbio_policy_admin"></span>**AMMINISTRATORE DEI CRITERI WINBIO \_ \_**
</dt> <dd>

Criteri di gruppo impostati dall'amministratore IT per l'organizzazione. I singoli utenti non possono eseguire l'override di questo criterio.

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
</dt> </dl>

 

 





