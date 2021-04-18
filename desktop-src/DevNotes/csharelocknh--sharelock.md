---
description: Ottiene un blocco condiviso.
ms.assetid: dff9a842-573a-4530-820d-6fd9001e502a
title: 'Metodo CShareLockNH:: ShareLock'
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
ms.openlocfilehash: d0c77564deceab29a8bee0cbffbd477559117cbd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327352"
---
# <a name="csharelocknhsharelock-method"></a>Metodo CShareLockNH:: ShareLock

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

Ogni chiamata a **ShareLock** deve essere abbinata esattamente a una chiamata a [**ShareUnlock**](csharelocknh--shareunlock.md). Solo un thread che chiama correttamente **ShareLock** può chiamare **ShareUnlock**; in caso contrario, può verificarsi un deadlock.

A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|-------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Rwnh.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ShareUnlock**](csharelocknh--shareunlock.md)
</dt> </dl>

 

 
