---
description: Importa un certificato codificato in precedenza da una stringa nell'oggetto Certificate.
ms.assetid: 8515e034-08aa-4575-9b96-34cdee3ccba8
title: Metodo ICertificate2::Import
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.Import
- ICertificate2.Import
- ICertificate.Import
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 1f47ebe884c8fb3a10a8ebdef89353e7549c916a7793075d0086d2f0cd2ce717
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127011"
---
# <a name="icertificate2import-method"></a>Metodo ICertificate2::Import

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece la [**classe X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) nello spazio dei [**nomi System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

Il **metodo Import** importa un certificato codificato in precedenza da una stringa nell'oggetto Certificate. [](certificate.md) La chiamata a questo metodo reimposta [*lo stato*](../secgloss/s-gly.md) di questo oggetto.

## <a name="syntax"></a>Sintassi


```VB
Certificate.Import( _
  ByVal EncodedCertificate _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*EncodedCertificate* \[ Pollici\]
</dt> <dd>

Stringa che contiene i dati del certificato codificati da importare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fine del supporto client<br/> | Windows Vista<br/>                                                               |
| Fine del supporto server<br/> | Windows Server 2008<br/>                                                         |
| Componente ridistribuibile<br/>       | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Oggetti di crittografia](cryptography-objects.md)
</dt> <dt>

[**Certificato**](certificate.md)
</dt> </dl>

 

 
