---
description: Ottiene un blocco condiviso.
ms.assetid: dff9a842-573a-4530-820d-6fd9001e502a
title: Metodo CShareLockNH::ShareLock
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CShareLockNH.ShareLock
api_type:
- COM
api_location:
- Rwnh.dll
ms.openlocfilehash: 7fd398228c6d0feb7e63133e8faeefd7a2fd3359bf62e80a8f398a3467424b90
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119654831"
---
# <a name="csharelocknhsharelock-method"></a>Metodo CShareLockNH::ShareLock

Ottiene un blocco condiviso.

## <a name="syntax"></a>Sintassi


```C++
void ShareLock();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Ogni chiamata **a ShareLock** deve essere associata esattamente a una chiamata a [**ShareUnlock.**](csharelocknh--shareunlock.md) Solo un thread che chiama **correttamente ShareLock** può chiamare **ShareUnlock**; In caso contrario, può verificarsi un deadlock.

A questa funzione non è associata alcuna libreria di importazione o file di intestazione. è necessario chiamarlo usando le [**funzioni LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**e GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|-------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Rwnh.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ShareUnlock**](csharelocknh--shareunlock.md)
</dt> </dl>

 

 
