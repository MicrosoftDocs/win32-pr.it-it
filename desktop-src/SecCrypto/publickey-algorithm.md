---
description: La proprietà Algorithm recupera l'oggetto OID che identifica l'algoritmo utilizzato dalla chiave pubblica. Si tratta della proprietà predefinita.
ms.assetid: f804ac4b-6a33-4f25-950b-6b6838bcc638
title: Proprietà PublicKey. Algorithm
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
ms.openlocfilehash: 98e955279646306b1484dcd0674cf735680d44e8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329331"
---
# <a name="publickeyalgorithm-property"></a>Proprietà PublicKey. Algorithm

\[La proprietà **algoritmo** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Usare invece la [**Proprietà X509Certificate2. PublicKey**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.publickey?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

La proprietà **Algorithm** recupera l'oggetto [**OID**](oid.md) che identifica l'algoritmo utilizzato dalla chiave pubblica. Si tratta della proprietà predefinita.

## <a name="syntax"></a>Sintassi


```VB
PublicKey.Algorithm As OID
```



## <a name="property-value"></a>Valore proprietà

Oggetto [**OID**](oid.md) che identifica l'algoritmo utilizzato dalla chiave pubblica.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**PublicKey**](publickey.md)
</dt> </dl>

 

 
