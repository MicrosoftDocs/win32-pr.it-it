---
description: Acquisisce un blocco in lettura/scrittura.
ms.assetid: fd212dd9-034b-4e0c-9111-e3460ea6f133
title: 'Metodo CShareLockNH:: ExclusiveLock'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CShareLockNH.ExclusiveLock
api_type:
- COM
api_location:
- Rwnh.dll
ms.openlocfilehash: 8b35b544c10e6dde2887e75971d747feade5517e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331682"
---
# <a name="csharelocknhexclusivelock-method"></a>Metodo CShareLockNH:: ExclusiveLock

Acquisisce un blocco in lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
void ExclusiveLock();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Ogni chiamata a **ExclusiveLock** deve essere abbinata esattamente a una chiamata a [**ExclusiveUnlock**](csharelocknh--exclusiveunlock.md) per evitare il rischio di un deadlock.

A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|-------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Rwnh.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ExclusiveUnlock**](csharelocknh--exclusiveunlock.md)
</dt> </dl>

 

 
