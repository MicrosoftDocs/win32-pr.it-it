---
description: Divide i numeri interi estesi.
ms.assetid: d46f65f0-6c41-4cb2-9882-5b11f7aae3ca
title: RtlExtendedLargeIntegerDivide (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlExtendedLargeIntegerDivide
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: b17c89a744748214d74dc24abdaa8a12ac71e960
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330417"
---
# <a name="rtlextendedlargeintegerdivide-function"></a>RtlExtendedLargeIntegerDivide (funzione)

\[La funzione **RtlExtendedLargeIntegerDivide** viene esportata per supportare i binari dei driver esistenti ed è obsoleta. Per ottenere prestazioni migliori, usare il supporto del compilatore per le operazioni integer a 64 bit.\]

Divide i numeri interi estesi.

## <a name="syntax"></a>Sintassi


```C++
LARGE_INTEGER RtlExtendedLargeIntegerDivide(
  _In_    LARGE_INTEGER Dividend,
  _In_    ULONG         Divisor,
  _Inout_ PULONG        Remainder
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Dividendo* \[ in\]
</dt> <dd>

Dividendo.

</dd> <dt>

*Divisore* \[ in\]
</dt> <dd>

Divisore.

</dd> <dt>

*Resto* \[ in uscita\]
</dt> <dd>

Puntatore al resto della divisione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il risultato dell'operazione di divisione.

## <a name="remarks"></a>Commenti

A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|--------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



 

 
