---
description: Chiude un archivio certificati aperto.
ms.assetid: 14db819a-b220-47d4-9030-72157e0e5019
title: Store. Close (metodo)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Close
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2e3deb127ec8b19d9ec5c625f07cfaa2685b776c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331703"
---
# <a name="storeclose-method"></a>Store. Close (metodo)

\[Il metodo **Close** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Usare invece la [**classe X509Store**](/previous-versions/windows/embedded/hh424027(v=msdn.10)) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

Il metodo **Close** chiude un [*archivio certificati*](../secgloss/c-gly.md)aperto.

## <a name="syntax"></a>Sintassi


```VB
Store.Close()
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Quando viene chiamato il metodo **Close** , l'oggetto [**Store**](store.md) viene eliminato definitivamente.

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
</dt> <dt>

[**Aprire**](store-open.md)
</dt> </dl>

 

 
