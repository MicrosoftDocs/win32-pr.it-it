---
description: Indica se l'utente corrente è un amministratore.
ms.assetid: e759a6b9-19c3-4a2e-b8cf-1398037f88ee
title: pSetupIsUserAdmin (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pSetupIsUserAdmin
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 1c40a69fd682c22e2625a3ba362d11d719cf9cce
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330861"
---
# <a name="psetupisuseradmin-function"></a>pSetupIsUserAdmin (funzione)

\[Questa funzione non è disponibile in Windows Vista o Windows Server 2008.\]

Indica se l'utente corrente è un amministratore.

## <a name="syntax"></a>Sintassi


```C++
BOOL pSetupIsUserAdmin(void);
```



## <a name="parameters"></a>Parametri

Questa funzione non ha parametri.

## <a name="return-value"></a>Valore restituito

**True** se l'utente corrente è un amministratore; in caso contrario, **false**.

## <a name="remarks"></a>Commenti

A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Setupapi.dll</dt> </dl> |



 

 
