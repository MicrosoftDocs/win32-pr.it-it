---
description: Determina se al certificato è associata una chiave privata. Il metodo determina questa situazione controllando se la proprietà \_ CERT KEY \_ PROV \_ INFO PROP ID \_ è \_ presente.
ms.assetid: 80478956-1ed7-4c25-9ae3-d7176649e6d7
title: Metodo ICertificate2::HasPrivateKey
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.HasPrivateKey
- ICertificate2.HasPrivateKey
- ICertificate.HasPrivateKey
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: ac38a62e11d75e21de5fd61dffd821cb4384e4e9b59d2bf11f6e217589ab578b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117771538"
---
# <a name="icertificate2hasprivatekey-method"></a>Metodo ICertificate2::HasPrivateKey

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece la [**classe X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) nello spazio dei nomi [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

Il **metodo HasPrivateKey** determina se al [*certificato*](../secgloss/c-gly.md) è associata una [*chiave*](../secgloss/p-gly.md) privata. Il metodo determina questa situazione controllando se la proprietà \_ CERT KEY \_ PROV \_ INFO PROP ID \_ è \_ presente.

## <a name="syntax"></a>Sintassi


```VB
Certificate.HasPrivateKey()
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fine del supporto client<br/> | Windows Vista<br/>                                                               |
| Fine del supporto server<br/> | Windows Server 2008<br/>                                                         |
| Componente ridistribuibile<br/>       | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**PrivateKey.Open**](privatekey-open.md)
</dt> <dt>

[Oggetti di crittografia](cryptography-objects.md)
</dt> <dt>

[**Certificato**](certificate.md)
</dt> </dl>

 

 
