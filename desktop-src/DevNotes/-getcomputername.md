---
description: Ottiene il nome del computer.
ms.assetid: 8b6fd61a-dd5a-46b8-920e-cc8a848732b6
title: Funzione _GetComputerName
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _GetComputerName
api_type:
- DllExport
api_location:
- Msmdun80.dll
- Sqlunirl.dll
ms.openlocfilehash: a8fc124e9a5b036e1be83e49e504d2a4d42ea27a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328097"
---
# <a name="_getcomputername-function"></a>\_GetComputerName (funzione)

\[Questa funzione è un wrapper della funzione **GetComputerName** . Questa funzione può essere modificata o non disponibile in futuro. Le applicazioni devono chiamare direttamente **GetComputerName** .\]

Ottiene il nome del computer. Vedere [**GetComputerName**](/windows/win32/api/winbase/nf-winbase-getcomputernamea).

## <a name="syntax"></a>Sintassi


```C++
BOOL _GetComputerName(
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

[**GetComputerName**](/windows/win32/api/winbase/nf-winbase-getcomputernamea)
</dt> </dl>

 

 
