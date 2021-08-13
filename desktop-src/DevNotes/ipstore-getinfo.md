---
description: Restituisce informazioni sul provider di archiviazione.
ms.assetid: bdacb5bb-a37a-4970-add7-57625bec1ce0
title: Metodo IPStore::GetInfo (Pstore.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.GetInfo
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 118f346acf550a8d4835931102a26d70f0c41fad7cc23ac706268b7778c31b56
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118667272"
---
# <a name="ipstoregetinfo-method"></a>Metodo IPStore::GetInfo

\[Protected Archiviazione (Pstore) è disponibile per l'uso in Windows Server 2003 e Windows XP. È disponibile solo per le operazioni di sola lettura in Windows Server 2008 e Windows Vista, ma potrebbe non essere disponibile nelle versioni successive. Pstore usa un'implementazione precedente della protezione dei dati. Gli sviluppatori sono fortemente invitati a sfruttare la protezione dei dati più avanzata fornita dalle funzioni [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData.**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata)\]

Restituisce informazioni sul provider di archiviazione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetInfo(
  [out] PPST_PROVIDERINFO *ppProperties
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppProperties* \[ Cambio\]
</dt> <dd>

Puntatore a una **struttura PPST \_ PROVIDERINFO** che contiene informazioni sul provider di archiviazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è un **valore HRESULT.** Il valore **PST \_ E \_ OK** indica che la funzione ha avuto esito positivo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Pstore.h</dt> </dl>    |
| DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Archivio IP**](ipstore.md)
</dt> </dl>

 

 
