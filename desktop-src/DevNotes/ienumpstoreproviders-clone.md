---
description: 'Metodo IEnumPStoreProviders::Clone: crea un altro enumeratore che contiene lo stesso stato di enumerazione di quello corrente.'
ms.assetid: c9a53005-4bb2-4a07-8f58-28d51f22c9e8
title: Metodo IEnumPStoreProviders::Clone (Pstore.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreProviders.Clone
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 2eb5f5788c903c854d9cf1551d6cf5a1bd2b51f6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096799"
---
# <a name="ienumpstoreprovidersclone-method"></a>Metodo IEnumPStoreProviders::Clone

\[L'archiviazione protetta (Pstore) è disponibile per l'uso in Windows Server 2003 e Windows XP. È disponibile solo per le operazioni di sola lettura in Windows Server 2008 e Windows Vista, ma potrebbe non essere disponibile nelle versioni successive. Pstore usa un'implementazione precedente della protezione dei dati. Gli sviluppatori sono fortemente invitati a sfruttare la protezione dei dati più avanzata fornita dalle funzioni [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData.**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata)\]

Crea un altro enumeratore che contiene lo stesso stato di enumerazione di quello corrente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Clone(
  [out] IEnumPStoreProviders **ppenum
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppenum* \[ Cambio\]
</dt> <dd>

Puntatore a un [**puntatore IEnumPStoreProviders.**](ienumpstoreproviders.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è un **valore HRESULT.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Pstore.h</dt> </dl>    |
| DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IEnumPStoreProviders**](ienumpstoreproviders.md)
</dt> </dl>

 

 
