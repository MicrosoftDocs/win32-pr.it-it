---
description: Ottiene informazioni sulla versione del sistema operativo.
ms.assetid: 1af2c320-6e0b-4692-858b-a2c921ed7ce7
title: _GetVersionEx funzione
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _GetVersionEx
api_type:
- DllExport
api_location:
- Msmdun80.dll
- Sqlunirl.dll
ms.openlocfilehash: 2e3047edfaf2dabe591172dd3ca292f41aeefa90774231b417f5405e3aeb18c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956290"
---
# <a name="_getversionex-function"></a>\_Funzione GetVersionEx

\[Questa funzione è un wrapper sulla **funzione GetVersionEx.** Questa funzione potrebbe essere modificata o non disponibile in futuro. Le applicazioni devono chiamare **direttamente GetVersionEx.**\]

Ottiene informazioni sulla versione del sistema operativo. Vedere [**GetVersionEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa).

## <a name="syntax"></a>Sintassi


```C++
BOOL _GetVersionEx(
    ...
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*...* 
</dt> <dd></dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Msmdun80.dll; </dt> <dt>Sqlunirl.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Getversionex**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa)
</dt> </dl>

 

 
