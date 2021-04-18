---
description: Elimina l'archivio certificati rappresentato dall'oggetto archivio corrente.
ms.assetid: 274914ee-27a0-4bd6-8510-af897aab3a2d
title: Store. Delete (metodo)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Delete
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 41c6417dae5006eb2ecaf64660fd0007cdf37fd2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333971"
---
# <a name="storedelete-method"></a>Store. Delete (metodo)

\[Il metodo **Delete** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Usare invece la [**classe X509Store**](/previous-versions/windows/embedded/hh424027(v=msdn.10)) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

Il metodo **Delete** Elimina l' [*archivio certificati*](../secgloss/c-gly.md) rappresentato dall'oggetto [**Archivio**](certificate.md) corrente. Questo metodo elimina solo gli archivi non di sistema.

## <a name="syntax"></a>Sintassi


```VB
Store.Delete()
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Gli archivi seguenti sono archivi di sistema e non possono essere eliminati:

-   My
-   Radice
-   Trust
-   CA
-   UserDS
-   TrustedPublisher
-   Non consentita
-   AuthRoot
-   TrustedPeople

Il metodo **Delete** restituisce un errore se chiamato da uno script Web.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2,1 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Store**](store.md)
</dt> <dt>

[**Oggetti Cryptography**](cryptography-objects.md)
</dt> </dl>

 

 
