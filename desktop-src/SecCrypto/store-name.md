---
description: Recupera il nome dell'archivio certificati rappresentato da questo oggetto.
ms.assetid: db61b464-0e8e-4b19-be12-04e00d6bba53
title: Proprietà Store.Name
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Name
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 85679bb594bdb59c41773b7f956deea95021381f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333870"
---
# <a name="storename-property"></a>Proprietà Store.Name

\[La proprietà [**Name**](store-location.md) è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Usare invece la [**classe X509Store**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

La proprietà [**Name**](store-location.md) Recupera il nome dell'archivio certificati rappresentato da questo oggetto.

## <a name="syntax"></a>Sintassi


```VB
Store.Name As String
```



## <a name="property-value"></a>Valore proprietà

Valore **stringa** che rappresenta il nome dell'archivio certificati.

## <a name="remarks"></a>Commenti

Esempi di nomi di archivio certificati includono My e root.

Il valore della proprietà [**Name**](store-location.md) corrisponde al valore fornito per il parametro *StoreName* del metodo [**Open**](store-open.md) quando l'archivio è stato aperto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2,1 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Store**](store.md)
</dt> </dl>

 

 
