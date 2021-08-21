---
description: Impedisce a più thread di completare l'acquisizione di un blocco.
ms.assetid: 9cdcc6d5-b2f1-4c88-b859-1c15a80e70a9
title: Metodo CShareLockNH::P artialLock
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CShareLockNH.PartialLock
api_type:
- COM
api_location:
- Rwnh.dll
ms.openlocfilehash: 7eae3f0eb57d534ea352b7d1c1e0834ef54dfb42460dfe7b2edc4f6fc07fa013
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118162345"
---
# <a name="csharelocknhpartiallock-method"></a>Metodo CShareLockNH::P artialLock

Impedisce a più thread di completare l'acquisizione di un blocco.

## <a name="syntax"></a>Sintassi


```C++
void PartialLock();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Mentre **PartialLock** è attivo, altri thread che chiamano [**ShareLock**](csharelocknh--sharelock.md) possono accedere al blocco.

A questa funzione non è associata alcuna libreria di importazione o file di intestazione. è necessario chiamarlo usando le [**funzioni LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**e GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|-------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Rwnh.dll</dt> </dl> |



 

 
