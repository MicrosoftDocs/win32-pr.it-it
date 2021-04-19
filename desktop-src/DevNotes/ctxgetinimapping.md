---
description: Determina se l'Terminal Server è in modalità di installazione (solo in Windows Terminal Server 4,0).
ms.assetid: f6cb7971-d4f5-49ca-938a-9c280028764a
title: CtxGetIniMapping (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CtxGetIniMapping
api_type:
- DllExport
api_location:
- Kernel32.dll
ms.openlocfilehash: 17093303cf0ea74e7efc6a3070c48660083bc491
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331821"
---
# <a name="ctxgetinimapping-function"></a>CtxGetIniMapping (funzione)

\[Questa funzione non è supportata e non deve essere utilizzata. Potrebbe cambiare o scomparire completamente senza preavviso. Usare invece **VerifyVersionInfo**.\]

Determina se l'Terminal Server è in modalità di installazione (solo in Windows Terminal Server 4,0).

## <a name="syntax"></a>Sintassi


```C++
BOOLEAN CtxGetIniMapping(void);
```



## <a name="parameters"></a>Parametri

Questa funzione non ha parametri.

## <a name="return-value"></a>Valore restituito

Questa funzione restituisce **false** se il Terminal Server è in modalità di installazione, **true** se è in modalità di esecuzione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Kernel32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**VerifyVersionInfo**](/windows/win32/api/winbase/nf-winbase-verifyversioninfoa)
</dt> </dl>

 

 
