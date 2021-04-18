---
description: Recupera la specifica della chiave.
ms.assetid: 93c909cb-b1d1-4c2b-a66c-9d3f6dd9b340
title: Proprietà PrivateKey. dataspec
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PrivateKey.KeySpec
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: f9d0ba55ca48d5257a038845f84374544b7615b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330603"
---
# <a name="privatekeykeyspec-property"></a>Proprietà PrivateKey. dataspec

\[La proprietà di una **specifica** di parametro è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Usare invece la [**Proprietà X509Certificate2. PrivateKey**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

La **proprietà chiave specifica recupera** la specifica della chiave.

## <a name="syntax"></a>Sintassi


```VB
PrivateKey.KeySpec As CAPICOM_KEY_SPEC
```



## <a name="property-value"></a>Valore proprietà

Valore dell'enumerazione delle [**\_ \_ specifiche della chiave capicot**](capicom-key-spec.md) che indica la specifica della chiave. Nella tabella seguente sono illustrati i possibili valori.



| Valore                                                                                                                                                                                                        | Significato                                                    |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <span id="CAPICOM_KEY_SPEC_KEYEXCHANGE"></span><span id="capicom_key_spec_keyexchange"></span><dl> <dt>**chiave per lo \_ scambio di chiavi di CAPICOM \_ \_**</dt> </dl> | La chiave può essere usata per la crittografia e la firma.<br/> |
| <span id="CAPICOM_KEY_SPEC_SIGNATURE"></span><span id="capicom_key_spec_signature"></span><dl> <dt>**firma della specifica della \_ chiave CAPICOM \_ \_**</dt> </dl>       | La chiave può essere usata solo per la firma.<br/>           |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**PrivateKey**](privatekey.md)
</dt> </dl>

 

 
