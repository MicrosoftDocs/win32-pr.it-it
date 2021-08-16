---
description: Carica una libreria.
ms.assetid: 191fcbd8-4542-4cad-955e-6951f3005fc5
title: _LoadLibrary funzione
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _LoadLibrary
api_type:
- DllExport
api_location:
- Msmdun80.dll
- Sqlunirl.dll
ms.openlocfilehash: 67755d96d87530f450627714de7c1526750967b87bdf51901b788662c4534045
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117827982"
---
# <a name="_loadlibrary-function"></a>\_Funzione LoadLibrary

\[Questa funzione è un wrapper sulla **funzione LoadLibrary.** Questa funzione potrebbe essere modificata o non disponibile in futuro. Le applicazioni devono chiamare **direttamente LoadLibrary.**\]

Carica una libreria. Vedere [**LoadLibrary.**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)

## <a name="syntax"></a>Sintassi


```C++
HMODULE _LoadLibrary(
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

[**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)
</dt> </dl>

 

 
