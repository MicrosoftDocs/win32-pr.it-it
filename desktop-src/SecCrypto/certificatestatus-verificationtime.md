---
description: Imposta o recupera l'ora in cui il certificato è stato verificato.
ms.assetid: 1bd17df3-2fa1-4b99-ab00-659b4ad5fcd9
title: Proprietà CertificateStatus. VerificationTime
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificateStatus.VerificationTime
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 178402861c9830efbea78a31081ae7e8b31800b0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324132"
---
# <a name="certificatestatusverificationtime-property"></a>Proprietà CertificateStatus. VerificationTime

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece la [**struttura X509ChainStatus**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

La proprietà **VerificationTime** imposta o recupera l'ora in cui il certificato è stato verificato.

## <a name="syntax"></a>Sintassi


```VB
CertificateStatus.VerificationTime As Date
```



## <a name="property-value"></a>Valore proprietà

Ora di verifica del certificato.

## <a name="remarks"></a>Commenti

Se questa proprietà non è impostata, viene utilizzata l'ora corrente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fine del supporto client<br/> | Windows Vista<br/>                                                               |
| Fine del supporto server<br/> | Windows Server 2008<br/>                                                         |
| Componente ridistribuibile<br/>       | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
