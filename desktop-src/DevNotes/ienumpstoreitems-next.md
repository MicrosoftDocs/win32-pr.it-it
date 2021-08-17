---
description: Ottiene il successivo numero specificato di nomi di elementi di dati nella sequenza di enumerazione.
ms.assetid: 6f30bf64-bd63-43d7-ab7e-f64e372c723b
title: Metodo IEnumPStoreItems::Next (Pstore.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreItems.Next
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 0a70ac415c937b3fb3d5bf95901d2ae30f9d4b8fd5b5677c55465ccbadada4b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119432591"
---
# <a name="ienumpstoreitemsnext-method"></a>Metodo IEnumPStoreItems::Next

\[Protected Archiviazione (Pstore) è disponibile per l'uso in Windows Server 2003 e Windows XP. È disponibile solo per le operazioni di sola lettura in Windows Server 2008 e Windows Vista, ma potrebbe non essere disponibile nelle versioni successive. Pstore usa un'implementazione precedente della protezione dei dati. Gli sviluppatori sono fortemente invitati a sfruttare la protezione dei dati più avanzata fornita dalle funzioni [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData.**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata)\]

Ottiene il successivo numero specificato di nomi di elementi di dati nella sequenza di enumerazione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Next(
  [in]      DWORD  celt,
  [out]     LPWSTR *rgelt,
  [in, out] DWORD  *pceltFetched
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*celt* \[ Pollici\]
</dt> <dd>

Numero di elementi di dati richiesti.

</dd> <dt>

*rgelt* \[ Cambio\]
</dt> <dd>

Puntatore a una stringa in cui restituire il nome dell'elemento di dati.

</dd> <dt>

*pceltFetched* \[ in, out\]
</dt> <dd>

Puntatore al numero di nomi di elementi di dati effettivamente forniti.

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

[**IEnumPStoreItems**](ienumpstoreitems.md)
</dt> </dl>

 

 
