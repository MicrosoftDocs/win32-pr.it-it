---
description: Chiude un archivio certificati aperto.
ms.assetid: 14db819a-b220-47d4-9030-72157e0e5019
title: Metodo Store.Close
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
ms.openlocfilehash: e0310db88b29fea18756ecaf7a2dc142097c3a6e53dfff5892acdaf4030b9b00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118897926"
---
# <a name="storeclose-method"></a>Metodo Store.Close

\[Il **metodo** Close è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Usare invece la [**classe X509Store**](/previous-versions/windows/embedded/hh424027(v=msdn.10)) nello spazio dei nomi [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

Il **metodo Close** chiude un archivio certificati [*aperto.*](../secgloss/c-gly.md)

## <a name="syntax"></a>Sintassi


```VB
Store.Close()
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Dopo la chiamata al metodo **Close,** l'oggetto [**Store**](store.md) viene eliminato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2.1 o versioni successive Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Archiviazione**](store.md)
</dt> <dt>

[**Oggetti di crittografia**](cryptography-objects.md)
</dt> <dt>

[**Aperto**](store-open.md)
</dt> </dl>

 

 
