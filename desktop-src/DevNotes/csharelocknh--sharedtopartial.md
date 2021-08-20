---
description: Modifica un blocco condiviso in blocco parziale.
ms.assetid: 82122671-b0bd-47ad-9a25-ee8ebd3779be
title: Metodo CShareLockNH::SharedToPartial
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
ms.openlocfilehash: 8f2cc895786655754a3fcf56c6efe745467c12328867b1dc021a257ba1519652
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118162206"
---
# <a name="csharelocknhsharedtopartial-method"></a>Metodo CShareLockNH::SharedToPartial

Modifica un blocco condiviso in blocco parziale.

## <a name="syntax"></a>Sintassi


```C++
BOOL SharedToPartial();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE se** viene ottenuto il blocco parziale. In caso contrario, restituisce **FALSE** e il blocco rimane in modalità condivisa.

## <a name="remarks"></a>Commenti

A questa funzione non è associata alcuna libreria di importazione o file di intestazione. è necessario chiamarlo usando le [**funzioni LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**e GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|-------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Rwnh.dll</dt> </dl> |



 

 
