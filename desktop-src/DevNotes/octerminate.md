---
description: Chiude il gestore OC.
ms.assetid: feba9954-03b2-4b57-b7ba-933e171751ff
title: OcTerminate (funzione)
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
ms.openlocfilehash: 2e747c19db5e5a79e2827dc3bcfb88b97fae2ba6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326286"
---
# <a name="octerminate-function"></a>OcTerminate (funzione)

Chiude il gestore OC.

## <a name="syntax"></a>Sintassi


```C++
VOID OcTerminate(
  _Inout_ PVOID *OcManagerContext
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*OcManagerContext* \[ in uscita\]
</dt> <dd>

In input, contiene il puntatore di contesto del gestore OC restituito da [**OcInitialize**](ocinitialize.md). Nell'output, riceve **null**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>OcManage.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**OcInitialize**](ocinitialize.md)
</dt> </dl>

 

 
