---
description: Ricarica le impostazioni dei colori dal registro di sistema.
ms.assetid: 1F2EE08A-4193-4F0C-BE4F-0551FA71CFA8
title: FRefreshStyle (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FRefreshStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: 098e79ab49373dc115189a2c47dc3604fba10ef9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327679"
---
# <a name="frefreshstyle-function"></a>FRefreshStyle (funzione)

Ricarica le impostazioni dei colori dal registro di sistema.

## <a name="syntax"></a>Sintassi


```C++
BOOL __cdecl FRefreshStyle(void);
```



## <a name="parameters"></a>Parametri

Questa funzione non ha parametri.

## <a name="return-value"></a>Valore restituito

Restituisce TRUE in caso di esito positivo; in caso contrario, FALSE.

## <a name="remarks"></a>Commenti

Questa funzione non è associata a una libreria di importazione o a un file di intestazione. deve essere chiamato usando le funzioni [**LoadLibrary**](-loadlibrary.md) e [**GetProcAddress**](-getprocaddress-.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Imeshare.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**GetProcAddress**](-getprocaddress-.md)
</dt> <dt>

[**LoadLibrary**](-loadlibrary.md)
</dt> </dl>

 

 




