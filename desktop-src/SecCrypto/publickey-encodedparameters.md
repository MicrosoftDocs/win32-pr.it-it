---
description: Recupera i parametri dell'algoritmo a chiave pubblica.
ms.assetid: 1d12f72e-0144-4b7b-b468-d2f35bf253d3
title: Proprietà PublicKey. EncodedParameters
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PublicKey.EncodedParameters
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 316e9737633bccea46cb644da24e4cc98fd118bf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329329"
---
# <a name="publickeyencodedparameters-property"></a>Proprietà PublicKey. EncodedParameters

\[La proprietà **EncodedParameters** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Usare invece la [**Proprietà X509Certificate2. PublicKey**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.publickey?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

La proprietà **EncodedParameters** recupera i parametri dell'algoritmo a chiave pubblica.

## <a name="syntax"></a>Sintassi


```VB
PublicKey.EncodedParameters As EncodedData
```



## <a name="property-value"></a>Valore proprietà

Oggetto [**EncodedData**](encodeddata.md) che fornisce l'accesso ai parametri dell'algoritmo a chiave pubblica.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**PublicKey**](publickey.md)
</dt> </dl>

 

 
