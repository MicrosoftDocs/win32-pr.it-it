---
description: Moltiplica numeri interi estesi.
ms.assetid: 6a59d211-4baf-4c7c-af2a-ffb0c5773445
title: Funzione RtlExtendedIntegerMultiply
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
ms.openlocfilehash: 0048da80026029274a89d089f5c232311a481a6010c0aad32d8b1a6ae6cc6786
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119571471"
---
# <a name="rtlextendedintegermultiply-function"></a>Funzione RtlExtendedIntegerMultiply

\[La **funzione RtlExtendedIntegerMultiply** viene esportata per supportare i file binari del driver esistenti ed è obsoleta. Per prestazioni migliori, usare il supporto del compilatore per le operazioni integer a 64 bit.\]

Moltiplica numeri interi estesi.

## <a name="syntax"></a>Sintassi


```C++
LARGE_INTEGER RtlExtendedIntegerMultiply(
  _In_ LARGE_INTEGER Multiplicand,
  _In_ LONG          Multiplier
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Moltiplicazione* \[ Pollici\]
</dt> <dd>

Moltiplicato.

</dd> <dt>

*Moltiplicatore* \[ Pollici\]
</dt> <dd>

Moltiplicatore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il risultato della moltiplicazione.

## <a name="remarks"></a>Commenti

A questa funzione non è associata alcuna libreria di importazione o file di intestazione. è necessario chiamarlo usando le [**funzioni LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**e GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|--------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



 

 
