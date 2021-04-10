---
description: Recupera la directory AppPatch di sistema.
ms.assetid: 1c79411f-1f90-4b90-84c7-24a34cf0d91d
title: SdbGetAppPatchDir (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetAppPatchDir
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 60a3b14bcca1be3ecb8d33b0d3f344f08bc11b28
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104125634"
---
# <a name="sdbgetapppatchdir-function"></a>SdbGetAppPatchDir (funzione)

Recupera la directory AppPatch di sistema.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI SdbGetAppPatchDir(
  _In_opt_ HSDB   hSDB,
  _Out_    LPTSTR szAppPatchPath,
  _In_     DWORD  cchSize
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hSDB* \[ in, facoltativo\]
</dt> <dd>

Handle per il database shim restituito dalla funzione [**SdbInitDatabase**](sdbinitdatabase.md) .

</dd> <dt>

*szAppPatchPath* \[ out\]
</dt> <dd>

Percorso risultante.

</dd> <dt>

*cchSize* \[ in\]
</dt> <dd>

Dimensioni del buffer *szAppPatchPath* , in caratteri. Se la funzione ha esito negativo, questo parametro viene impostato sulla stringa vuota ("").

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                         |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SdbInitDatabase**](sdbinitdatabase.md)
</dt> </dl>

 

 




