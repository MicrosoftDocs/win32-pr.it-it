---
description: Moltiplica gli Integer estesi.
ms.assetid: 6a59d211-4baf-4c7c-af2a-ffb0c5773445
title: RtlExtendedIntegerMultiply (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlExtendedIntegerMultiply
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 8b824080c28da3265be6dc0333f236b8c9a4cbaf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326832"
---
# <a name="rtlextendedintegermultiply-function"></a>RtlExtendedIntegerMultiply (funzione)

\[La funzione **RtlExtendedIntegerMultiply** viene esportata per supportare i binari dei driver esistenti ed è obsoleta. Per ottenere prestazioni migliori, usare il supporto del compilatore per le operazioni integer a 64 bit.\]

Moltiplica gli Integer estesi.

## <a name="syntax"></a>Sintassi


```C++
LARGE_INTEGER RtlExtendedIntegerMultiply(
  _In_ LARGE_INTEGER Multiplicand,
  _In_ LONG          Multiplier
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Multiplicand* \[ in\]
</dt> <dd>

Multiplicand.

</dd> <dt>

*Moltiplicatore* \[ in\]
</dt> <dd>

Moltiplicatore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il risultato della moltiplicazione.

## <a name="remarks"></a>Commenti

A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|--------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



 

 
