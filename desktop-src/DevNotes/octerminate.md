---
description: Chiude il gestore OC.
ms.assetid: feba9954-03b2-4b57-b7ba-933e171751ff
title: Funzione OcTerminate
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OcTerminate
api_type:
- DllExport
api_location:
- OcManage.dll
ms.openlocfilehash: 399bdb936befb4f7ff45f9f5a3b132245b984bf2a5201ce054ee0fbeb50f5598
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119833351"
---
# <a name="octerminate-function"></a>Funzione OcTerminate

Chiude il gestore OC.

## <a name="syntax"></a>Sintassi


```C++
VOID OcTerminate(
  _Inout_ PVOID *OcManagerContext
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*OcManagerContext* \[ in, out\]
</dt> <dd>

In input contiene il puntatore di contesto del gestore OC restituito [**da OcInitialize.**](ocinitialize.md) Nell'output riceve **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

A questa funzione non è associata alcuna libreria di importazione o file di intestazione. è necessario chiamarlo usando le [**funzioni LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**e GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>OcManage.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**OcInitialize**](ocinitialize.md)
</dt> </dl>

 

 
