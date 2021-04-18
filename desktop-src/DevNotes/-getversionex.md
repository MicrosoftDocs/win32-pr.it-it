---
description: Ottiene informazioni sulla versione del sistema operativo.
ms.assetid: 1af2c320-6e0b-4692-858b-a2c921ed7ce7
title: Funzione _GetVersionEx
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
ms.openlocfilehash: dd4b33bee4a5f1c2a72ef7494176fe2979b4a7cd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325693"
---
# <a name="_getversionex-function"></a>\_GetVersionEx (funzione)

\[Questa funzione è un wrapper per la funzione **GetVersionEx** . Questa funzione può essere modificata o non disponibile in futuro. Le applicazioni devono chiamare direttamente **GetVersionEx** .\]

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

[**GetVersionEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa)
</dt> </dl>

 

 
