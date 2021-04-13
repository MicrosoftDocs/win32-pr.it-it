---
title: Enumerazione WINBIO_POLICY_SOURCE ( \_ tipi WINBIO. h)
description: Elenca le possibili origini delle informazioni sui criteri per il rilevamento dello spoofing per i fattori biometrici.
ms.assetid: 3DC3BB0B-1FD7-473C-8E0B-B7E0A4A44E9E
keywords:
- WINBIO_POLICY_SOURCE enumerazione Windows Biometric Framework API
- Puntatore di enumerazione PWINBIO_POLICY_SOURCE Windows Biometric Framework API
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
ms.openlocfilehash: 866d1d82d939f143c4385caa5d94c68ffe3758f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341263"
---
# <a name="winbio_policy_source-enumeration"></a>Enumerazione dell'origine dei \_ criteri WINBIO \_

Elenca le possibili origini delle informazioni sui criteri per il rilevamento dello spoofing per i fattori biometrici.

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

<span id="WINBIO_POLICY_UNKNOWN"></span><span id="winbio_policy_unknown"></span>**\_criterio WINBIO \_ sconosciuto**
</dt> <dd>

L'origine del criterio è sconosciuta.

</dd> <dt>

<span id="WINBIO_POLICY_DEFAULT"></span><span id="winbio_policy_default"></span>**\_impostazione predefinita dei criteri di WINBIO \_**
</dt> <dd>

Il criterio è il criterio predefinito fornito dal Windows Biometric Framework.

</dd> <dt>

<span id="WINBIO_POLICY_LOCAL"></span><span id="winbio_policy_local"></span>**\_criteri WINBIO \_ locale**
</dt> <dd>

Criteri impostati dall'utente singolo per il proprio account tramite l'app **Impostazioni** . Questo criterio sostituisce i criteri predefiniti.

</dd> <dt>

<span id="WINBIO_POLICY_ADMIN"></span><span id="winbio_policy_admin"></span>**\_amministrazione dei criteri di WINBIO \_**
</dt> <dd>

Criteri di gruppo impostati dall'amministratore IT per l'organizzazione. I singoli utenti non possono eseguire l'override di questo criterio.

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
</dt> </dl>

 

 





