---
description: Modifica un blocco condiviso in un blocco parziale.
ms.assetid: 82122671-b0bd-47ad-9a25-ee8ebd3779be
title: 'Metodo CShareLockNH:: SharedToPartial'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CShareLockNH.SharedToPartial
api_type:
- COM
api_location:
- Rwnh.dll
ms.openlocfilehash: a997c5a437063a4c55b74d837dc77fd506688158
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327351"
---
# <a name="csharelocknhsharedtopartial-method"></a>Metodo CShareLockNH:: SharedToPartial

Modifica un blocco condiviso in un blocco parziale.

## <a name="syntax"></a>Sintassi


```C++
BOOL SharedToPartial();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce **true** se viene ottenuto il blocco parziale. in caso contrario, restituisce **false** e il blocco rimane in modalità condivisa.

## <a name="remarks"></a>Commenti

A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|-------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Rwnh.dll</dt> </dl> |



 

 
