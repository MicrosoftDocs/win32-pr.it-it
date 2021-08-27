---
description: Ricarica le impostazioni dei colori dal Registro di sistema.
ms.assetid: 1F2EE08A-4193-4F0C-BE4F-0551FA71CFA8
title: Funzione FRefreshStyle
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
ms.openlocfilehash: 5c071d76712877650bba8ecf502687538bb6ac354e62a0285dc08e2f22f25873
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120103691"
---
# <a name="frefreshstyle-function"></a>Funzione FRefreshStyle

Ricarica le impostazioni dei colori dal Registro di sistema.

## <a name="syntax"></a>Sintassi


```C++
BOOL __cdecl FRefreshStyle(void);
```



## <a name="parameters"></a>Parametri

Questa funzione non ha parametri.

## <a name="return-value"></a>Valore restituito

Restituisce TRUE in caso di esito positivo. in caso contrario, FALSE.

## <a name="remarks"></a>Commenti

Questa funzione non è associata a una libreria di importazione o a un file di intestazione. deve essere chiamato usando le [**funzioni LoadLibrary**](-loadlibrary.md) e [**GetProcAddress.**](-getprocaddress-.md)

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

 

 




