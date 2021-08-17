---
description: L'oggetto PublicKey rappresenta una chiave pubblica in un oggetto Certificate.
title: Oggetto PublicKey
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
ms.openlocfilehash: 5d27a89d51840e70563854b3cc7f9084b6bd42cb5707630755e771d610c64a91
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118901348"
---
# <a name="publickey-object"></a>Oggetto PublicKey

\[**L'oggetto PublicKey** è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Usare invece la [**proprietà X509Certificate2.PublicKey**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.publickey?view=netcore-3.1) nello spazio dei nomi [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

**L'oggetto PublicKey** rappresenta una chiave pubblica in un [**oggetto Certificate.**](certificate.md)

## <a name="when-to-use"></a>Utilizzo

**L'oggetto PublicKey** viene usato per recuperare i dati sulla chiave pubblica.

## <a name="members"></a>Membri

**L'oggetto PublicKey** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

**L'oggetto PublicKey** ha queste proprietà.



| Proprietà                                                            | Tipo di accesso          | Descrizione                                                                                                                            |
|:--------------------------------------------------------------------|:---------------------|:---------------------------------------------------------------------------------------------------------------------------------------|
| [**Algoritmo**](publickey-algorithm.md)<br/>                 | Sola lettura<br/> | Recupera [**l'oggetto OID**](oid.md) che identifica l'algoritmo usato dalla chiave pubblica. Si tratta della proprietà predefinita.<br/> |
| [**EncodedKey**](publickey-encodedkey.md)<br/>               | Sola lettura<br/> | Recupera un [**oggetto EncodedData**](encodeddata.md) che fornisce l'accesso al valore della chiave pubblica.<br/>                 |
| [**EncodedParameters**](publickey-encodedparameters.md)<br/> | Sola lettura<br/> | Recupera un oggetto [**EncodedData**](encodeddata.md) che fornisce l'accesso ai parametri dell'algoritmo a chiave pubblica.<br/>  |
| [**Length**](publickey-length.md)<br/>                       | Sola lettura<br/> | Recupera la lunghezza della chiave pubblica in bit.<br/>                                                                             |



 

## <a name="remarks"></a>Commenti

Impossibile **creare l'oggetto PublicKey.**

**L'oggetto PublicKey** viene usato dal [**metodo Certificate.PublicKey.**](certificate-publickey.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
