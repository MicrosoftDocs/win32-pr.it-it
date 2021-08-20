---
description: La proprietà Algorithm recupera l'oggetto OID che identifica l'algoritmo utilizzato dalla chiave pubblica. Si tratta della proprietà predefinita.
ms.assetid: f804ac4b-6a33-4f25-950b-6b6838bcc638
title: PublicKey.Algorithm - proprietà
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PublicKey.Algorithm
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 5dfe06e0454f54e33573696b716c7c8d709692cf9a5011b67bb85549535b9273
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117976159"
---
# <a name="publickeyalgorithm-property"></a>PublicKey.Algorithm - proprietà

\[La **proprietà Algorithm** è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Usare invece la [**proprietà X509Certificate2.PublicKey**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.publickey?view=netcore-3.1) nello spazio dei nomi [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

La **proprietà Algorithm** recupera l'oggetto [**OID**](oid.md) che identifica l'algoritmo utilizzato dalla chiave pubblica. Si tratta della proprietà predefinita.

## <a name="syntax"></a>Sintassi


```VB
PublicKey.Algorithm As OID
```



## <a name="property-value"></a>Valore proprietà

Oggetto [**OID**](oid.md) che identifica l'algoritmo utilizzato dalla chiave pubblica.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Publickey**](publickey.md)
</dt> </dl>

 

 
