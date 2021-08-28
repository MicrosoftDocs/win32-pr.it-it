---
description: Recupera il percorso dell'archivio certificati rappresentato da questo oggetto .
ms.assetid: 756ee7cb-5f9f-4fb2-bf10-79b543895189
title: Store.Location - proprietà
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
ms.openlocfilehash: b03fd93196eba3c0b3592d89ff3dfb3f5e8236f481296bfd9369beedc44fea91
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117972551"
---
# <a name="storelocation-property"></a>Store.Location - proprietà

\[La **proprietà Location** è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Usare invece la [**classe X509Store**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) nello spazio dei [**nomi System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

La **proprietà Location** recupera il percorso dell'archivio certificati rappresentato da questo oggetto.

## <a name="syntax"></a>Sintassi


```VB
Store.Location As CAPICOM_STORE_LOCATION
```



## <a name="property-value"></a>Valore proprietà

Valore [**CAPICOM \_ STORE \_ LOCATION**](capicom-store-location.md) che rappresenta il percorso dell'archivio certificati.

## <a name="remarks"></a>Commenti

Il valore della **proprietà Location** è uguale al valore fornito per il parametro *StoreLocation* del metodo [**Open**](store-open.md) quando l'archivio è stato aperto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2.1 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Archiviazione**](store.md)
</dt> </dl>

 

 
