---
description: L'oggetto PublicKey rappresenta una chiave pubblica in un oggetto Certificate.
title: PublicKey (oggetto)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PublicKey
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 12ab8fcf61d30b47fc809fb05e1ffa524bb2488e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333285"
---
# <a name="publickey-object"></a>PublicKey (oggetto)

\[L'oggetto **publicKey** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Usare invece la [**Proprietà X509Certificate2. PublicKey**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.publickey?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

L'oggetto **publicKey** rappresenta una chiave pubblica in un oggetto [**Certificate**](certificate.md) .

## <a name="when-to-use"></a>Utilizzo

L'oggetto **publicKey** viene utilizzato per recuperare i dati relativi alla chiave pubblica.

## <a name="members"></a>Membri

L'oggetto **publicKey** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

L'oggetto **publicKey** presenta queste proprietà.



| Proprietà                                                            | Tipo di accesso          | Descrizione                                                                                                                            |
|:--------------------------------------------------------------------|:---------------------|:---------------------------------------------------------------------------------------------------------------------------------------|
| [**Algoritmo**](publickey-algorithm.md)<br/>                 | Sola lettura<br/> | Recupera l'oggetto [**OID**](oid.md) che identifica l'algoritmo utilizzato dalla chiave pubblica. Si tratta della proprietà predefinita.<br/> |
| [**EncodedKey**](publickey-encodedkey.md)<br/>               | Sola lettura<br/> | Recupera un oggetto [**EncodedData**](encodeddata.md) che fornisce l'accesso al valore della chiave pubblica.<br/>                 |
| [**EncodedParameters**](publickey-encodedparameters.md)<br/> | Sola lettura<br/> | Recupera un oggetto [**EncodedData**](encodeddata.md) che fornisce l'accesso ai parametri dell'algoritmo a chiave pubblica.<br/>  |
| [**Lunghezza**](publickey-length.md)<br/>                       | Sola lettura<br/> | Recupera la lunghezza della chiave pubblica in bit.<br/>                                                                             |



 

## <a name="remarks"></a>Commenti

Impossibile creare l'oggetto **publicKey** .

L'oggetto **publicKey** viene utilizzato dal metodo [**Certificate. PublicKey**](certificate-publickey.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
