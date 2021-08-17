---
title: WINBIO_CREDENTIAL_FORMAT enumerazione \_ (Types.h Winbio)
description: Definisce i flag che possono essere utilizzati per specificare il formato delle credenziali dell'utente finale.
ms.assetid: f107e000-98a2-44f0-aa5e-d13b5d9c8d43
keywords:
- WINBIO_CREDENTIAL_FORMAT'enumerazione Windows'API Biometric Framework
topic_type:
- apiref
api_name:
- WINBIO_CREDENTIAL_FORMAT
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82185bdb9d8170abbdba04e758010443dc8be6a37e198edb27a137024dacf9af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118910824"
---
# <a name="winbio_credential_format-enumeration"></a>Enumerazione CREDENTIAL FORMAT WINBIO \_ \_

Definisce i flag che possono essere utilizzati per specificare il formato delle credenziali dell'utente finale. Questa enumerazione viene usata dalla [**funzione WinBioSetCredential.**](/windows/desktop/api/Winbio/nf-winbio-winbiosetcredential)

## <a name="syntax"></a>Sintassi


```C++
typedef enum _WINBIO_CREDENTIAL_FORMAT { 
  WINBIO_PASSWORD_GENERIC    = 0x00000001,
  WINBIO_PASSWORD_PACKED     = 0x00000002,
  WINBIO_PASSWORD_PROTECTED  = 0x00000003
} WINBIO_CREDENTIAL_FORMAT;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="WINBIO_PASSWORD_GENERIC"></span><span id="winbio_password_generic"></span>**WINBIO \_ PASSWORD \_ GENERICA**
</dt> <dd>

La password è in un formato generico.

</dd> <dt>

<span id="WINBIO_PASSWORD_PACKED"></span><span id="winbio_password_packed"></span>**PASSWORD WINBIO \_ \_ IN PACCHETTO**
</dt> <dd>

La password è in un formato compresso.

</dd> <dt>

<span id="WINBIO_PASSWORD_PROTECTED"></span><span id="winbio_password_protected"></span>**WINBIO \_ PASSWORD \_ PROTECTED**
</dt> <dd>

La credenziale della password è stata incapsulata [**con CredProtect**](/windows/desktop/api/wincred/nf-wincred-credprotecta).

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8.1 solo app desktop\]<br/>                                                                  |
| Server minimo supportato<br/> | Windows Server 2012 Solo \[ app desktop R2\]<br/>                                                       |
| Intestazione<br/>                   | <dl> <dt>Winbio \_ types.h (include Winbio.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni di applicazioni client](client-application-enumerations.md)
</dt> <dt>

[**WinBioSetCredential**](/windows/desktop/api/Winbio/nf-winbio-winbiosetcredential)
</dt> </dl>

 

