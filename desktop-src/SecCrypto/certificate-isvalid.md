---
description: Compila una catena di verifica del certificato per un certificato e restituisce un oggetto CertificateStatus che contiene lo stato di validità del certificato.
ms.assetid: 4463e4ac-60a5-4845-93b3-35d2f83bd86e
title: 'Metodo ICertificate2:: IsValid'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.IsValid
- ICertificate2.IsValid
- ICertificate.IsValid
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 39fec7c1bd2b369ee512834ed1b58b59871d8ae5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325022"
---
# <a name="icertificate2isvalid-method"></a>Metodo ICertificate2:: IsValid

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece la [**classe X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

Il metodo **IsValid** compila una catena di verifica del certificato per un certificato e restituisce un oggetto [**CertificateStatus**](certificatestatus.md) che contiene lo stato di validità del certificato.

## <a name="syntax"></a>Sintassi


```VB
Certificate.IsValid()
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fine del supporto client<br/> | Windows Vista<br/>                                                               |
| Fine del supporto server<br/> | Windows Server 2008<br/>                                                         |
| Componente ridistribuibile<br/>       | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Oggetti Cryptography](cryptography-objects.md)
</dt> <dt>

[**Certificato**](certificate.md)
</dt> </dl>

 

 
