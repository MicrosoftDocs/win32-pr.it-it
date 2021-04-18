---
description: Recupera la raccolta di certificati associata all'oggetto SignedData. Dopo essere stati recuperati, è possibile enumerare i singoli oggetti certificato della raccolta.
ms.assetid: 94741fee-2462-4a18-bc14-c52e9cac374b
title: Proprietà SignedData. Certificates
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedData.Certificates
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 55c0fe432794289fabe67b37deeedfac43f7a7d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327894"
---
# <a name="signeddatacertificates-property"></a>Proprietà SignedData. Certificates

\[La proprietà **Certificates** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Usare invece la [**classe SignedCms**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) nello spazio dei nomi [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

La proprietà **Certificates** recupera la raccolta di [**certificati**](certificates.md) associata all'oggetto [**SignedData**](signeddata.md) . Dopo essere stati recuperati, è possibile enumerare i singoli oggetti [**certificato**](certificate.md) della raccolta.

## <a name="syntax"></a>Sintassi


```VB
SignedData.Certificates As Certificates
```



## <a name="property-value"></a>Valore proprietà

Raccolta di [**certificati**](certificates.md) associata all'oggetto [**SignedData**](signeddata.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SignedData**](signeddata.md)
</dt> </dl>

 

 
