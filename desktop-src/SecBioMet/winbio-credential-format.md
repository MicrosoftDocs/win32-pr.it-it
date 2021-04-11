---
title: Enumerazione WINBIO_CREDENTIAL_FORMAT ( \_ tipi WINBIO. h)
description: Definisce i flag che possono essere utilizzati per specificare il formato delle credenziali dell'utente finale.
ms.assetid: f107e000-98a2-44f0-aa5e-d13b5d9c8d43
keywords:
- WINBIO_CREDENTIAL_FORMAT enumerazione Windows Biometric Framework API
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
ms.openlocfilehash: fa28ea56c7af9f78947e64587740300a70f763ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119782"
---
# <a name="winbio_credential_format-enumeration"></a>Enumerazione del formato delle \_ credenziali WINBIO \_

Definisce i flag che possono essere utilizzati per specificare il formato delle credenziali dell'utente finale. Questa enumerazione viene utilizzata dalla funzione [**WinBioSetCredential**](/windows/desktop/api/Winbio/nf-winbio-winbiosetcredential) .

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

<span id="WINBIO_PASSWORD_GENERIC"></span><span id="winbio_password_generic"></span>**WINBIO \_ password \_ generico**
</dt> <dd>

Il formato della password è generico.

</dd> <dt>

<span id="WINBIO_PASSWORD_PACKED"></span><span id="winbio_password_packed"></span>**\_password \_ compressa WINBIO**
</dt> <dd>

La password è in un formato compresso.

</dd> <dt>

<span id="WINBIO_PASSWORD_PROTECTED"></span><span id="winbio_password_protected"></span>**WINBIO \_ password \_ protetta**
</dt> <dd>

La credenziale della password è stata incapsulata con [**CredProtect**](/windows/desktop/api/wincred/nf-wincred-credprotecta).

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8.1 \[ solo app desktop\]<br/>                                                                  |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2012 R2 \[\]<br/>                                                       |
| Intestazione<br/>                   | <dl> <dt>\_Tipi WinBio. h (includere WinBio. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni delle applicazioni client](client-application-enumerations.md)
</dt> <dt>

[**WinBioSetCredential**](/windows/desktop/api/Winbio/nf-winbio-winbiosetcredential)
</dt> </dl>

 

