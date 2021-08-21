---
description: Rilascia un blocco acquisito utilizzando ExclusiveLock in modalità condivisa.
ms.assetid: d38354f0-2eb3-4924-99b5-1331e587ce32
title: Metodo CShareLockNH::ExclusiveUnlock
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
ms.openlocfilehash: 20d614f733b1668e3dea7619629cf2833f1d6af40384e679aea79a7a48279724
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118667837"
---
# <a name="csharelocknhexclusiveunlock-method"></a>Metodo CShareLockNH::ExclusiveUnlock

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

Ogni chiamata [**a ExclusiveLock**](csharelocknh--exclusivelock.md) deve essere abbinata esattamente a una chiamata a **ExclusiveUnlock** per evitare il rischio di deadlock.

A questa funzione non è associata alcuna libreria di importazione o file di intestazione. è necessario chiamarlo usando le [**funzioni LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**e GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|-------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Rwnh.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ExclusiveLock**](csharelocknh--exclusivelock.md)
</dt> </dl>

 

 
