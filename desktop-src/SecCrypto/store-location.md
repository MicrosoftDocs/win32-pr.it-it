---
description: Recupera il percorso dell'archivio certificati rappresentato da questo oggetto.
ms.assetid: 756ee7cb-5f9f-4fb2-bf10-79b543895189
title: Proprietà Store. location
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Location
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 42afe40dffde5a0375928d355508ec75a4076f17
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333152"
---
# <a name="storelocation-property"></a>Proprietà Store. location

\[La proprietà **location** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Usare invece la [**classe X509Store**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

La proprietà **location** Recupera il percorso dell'archivio certificati rappresentato da questo oggetto.

## <a name="syntax"></a>Sintassi


```VB
Store.Location As CAPICOM_STORE_LOCATION
```



## <a name="property-value"></a>Valore proprietà

Il valore del [**\_ \_ percorso dell'archivio CAPICOM**](capicom-store-location.md) che rappresenta il percorso dell'archivio certificati.

## <a name="remarks"></a>Commenti

Il valore della proprietà **location** corrisponde al valore fornito per il parametro *StoreLocation* del metodo [**Open**](store-open.md) quando l'archivio è stato aperto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2,1 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Store**](store.md)
</dt> </dl>

 

 
