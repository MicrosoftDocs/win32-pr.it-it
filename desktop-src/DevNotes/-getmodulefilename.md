---
description: Ottiene il percorso del modulo.
ms.assetid: ff632357-8d4a-4de4-a69a-0be9e380639d
title: Funzione _GetModuleFileName
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _GetModuleFileName
api_type:
- DllExport
api_location:
- Msmdun80.dll
- Sqlunirl.dll
ms.openlocfilehash: 5bf18e8baac62de6474f4ce1e48a0ae115ced778
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331976"
---
# <a name="_getmodulefilename-function"></a>\_GetModuleFileName (funzione)

\[Questa funzione è un wrapper per la funzione **GetModuleFileName** . Questa funzione può essere modificata o non disponibile in futuro. Le applicazioni devono chiamare direttamente **GetModuleFileName** .\]

Ottiene il percorso del modulo. Vedere [**GetModuleFileName**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulefilenamea).

## <a name="syntax"></a>Sintassi


```C++
DWORD _GetModuleFileName(
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

[**GetModuleFileName**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulefilenamea)
</dt> </dl>

 

 
