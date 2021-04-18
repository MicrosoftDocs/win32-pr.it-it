---
description: Rilascia un blocco acquisito utilizzando ExclusiveLock in modalità condivisa.
ms.assetid: d38354f0-2eb3-4924-99b5-1331e587ce32
title: 'Metodo CShareLockNH:: ExclusiveUnlock'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CShareLockNH.ExclusiveUnlock
api_type:
- COM
api_location:
- Rwnh.dll
ms.openlocfilehash: f5fae5d6131bfcb386d52880b530f3def9464442
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331678"
---
# <a name="csharelocknhexclusiveunlock-method"></a>Metodo CShareLockNH:: ExclusiveUnlock

Rilascia un blocco acquisito utilizzando [**ExclusiveLock**](csharelocknh--exclusivelock.md) in modalità condivisa.

## <a name="syntax"></a>Sintassi


```C++
void ExclusiveUnlock();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Ogni chiamata a [**ExclusiveLock**](csharelocknh--exclusivelock.md) deve essere abbinata esattamente a una chiamata a **ExclusiveUnlock** per evitare il rischio di un deadlock.

A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|-------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Rwnh.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ExclusiveLock**](csharelocknh--exclusivelock.md)
</dt> </dl>

 

 
