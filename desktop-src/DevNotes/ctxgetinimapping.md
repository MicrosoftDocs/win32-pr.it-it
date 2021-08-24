---
description: Determina se Terminal Server è in modalità INSTALL (solo in Terminale Windows Server 4.0).
ms.assetid: f6cb7971-d4f5-49ca-938a-9c280028764a
title: Funzione CtxGetIniMapping
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
ms.openlocfilehash: 7085e595b1f9c1fb8ea36e59aae4a90c816b508c92bcd33a99fe5051f2b722d9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119654211"
---
# <a name="ctxgetinimapping-function"></a>Funzione CtxGetIniMapping

\[Questa funzione non è supportata e non deve essere usata. Può cambiare o scomparire completamente senza preavviso. Usare invece **VerifyVersionInfo.**\]

Determina se Terminal Server è in modalità INSTALL (solo in Terminale Windows Server 4.0).

## <a name="syntax"></a>Sintassi


```C++
BOOLEAN CtxGetIniMapping(void);
```



## <a name="parameters"></a>Parametri

Questa funzione non ha parametri.

## <a name="return-value"></a>Valore restituito

Questa funzione restituisce **FALSE** se Terminal Server è in modalità INSTALL, **TRUE** se è in modalità EXECUTE.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Kernel32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**VerifyVersionInfo**](/windows/win32/api/winbase/nf-winbase-verifyversioninfoa)
</dt> </dl>

 

 
