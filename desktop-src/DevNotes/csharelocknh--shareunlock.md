---
description: Rilascia un blocco condiviso.
ms.assetid: c2e9eb68-aacb-4196-b09e-d2748efb7fd6
title: 'Metodo CShareLockNH:: ShareUnlock'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CShareLockNH.ShareUnlock
api_type:
- COM
api_location:
- Rwnh.dll
ms.openlocfilehash: 80c4311f4bf66000440dac38da6300888a8e5d59
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327350"
---
# <a name="csharelocknhshareunlock-method"></a>Metodo CShareLockNH:: ShareUnlock

Rilascia un blocco condiviso.

## <a name="syntax"></a>Sintassi


```C++
void ShareUnlock();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Ogni chiamata a [**ShareLock**](csharelocknh--sharelock.md) deve essere abbinata esattamente a una chiamata a **ShareUnlock**. Solo un thread che chiama correttamente **ShareLock** può chiamare **ShareUnlock**; in caso contrario, può verificarsi un deadlock.

A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|-------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Rwnh.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ShareLock**](csharelocknh--sharelock.md)
</dt> </dl>

 

 
