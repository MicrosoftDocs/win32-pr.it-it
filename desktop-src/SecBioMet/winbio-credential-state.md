---
title: WINBIO_CREDENTIAL_STATE enumerazione (Winbio \_ types.h)
description: Definisce i valori che specificano se una credenziale è stata associata ai dati biometrici per un utente finale.
ms.assetid: c24f1771-7a1f-403e-8100-dfb3f4cd77a1
keywords:
- WINBIO_CREDENTIAL_STATE enumerazione Windows'API Biometric Framework
- PWINBIO_CREDENTIAL_STATE puntatore di enumerazione Windows'API Biometric Framework
topic_type:
- apiref
api_name:
- WINBIO_CREDENTIAL_STATE
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce0e176479a68d39b017e852e17a73691b8349d7c6faa6be62130007a09dcef0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119868061"
---
# <a name="winbio_credential_state-enumeration"></a>Enumerazione CREDENTIAL STATE WINBIO \_ \_

Definisce i valori che specificano se una credenziale è stata associata ai dati biometrici per un utente finale. Questa enumerazione viene usata dalla [**funzione WinBioGetCredentialState.**](/windows/desktop/api/Winbio/nf-winbio-winbiogetcredentialstate)

## <a name="syntax"></a>Sintassi


```C++
typedef enum _WINBIO_CREDENTIAL_STATE { 
  WINBIO_CREDENTIAL_NOT_SET  = 0x00000001,
  WINBIO_CREDENTIAL_SET      = 0x00000002
} WINBIO_CREDENTIAL_STATE, *PWINBIO_CREDENTIAL_STATE;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="WINBIO_CREDENTIAL_NOT_SET"></span><span id="winbio_credential_not_set"></span>**CREDENZIALI WINBIO \_ \_ NON \_ IMPOSTATE**
</dt> <dd>

All'utente finale è stata associata una credenziale.

</dd> <dt>

<span id="WINBIO_CREDENTIAL_SET"></span><span id="winbio_credential_set"></span>**SET DI CREDENZIALI WINBIO \_ \_**
</dt> <dd>

All'utente finale non è stata associata una credenziale.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                                    |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/>                                                       |
| Intestazione<br/>                   | <dl> <dt>Winbio \_ types.h (include Winbio.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni di applicazioni client](client-application-enumerations.md)
</dt> <dt>

[**WinBioGetCredentialState**](/windows/desktop/api/Winbio/nf-winbio-winbiogetcredentialstate)
</dt> </dl>

 

 





