---
description: Rilascia le risorse usate dalla funzione SdbGetMatchingExe.
ms.assetid: 4a784f72-2108-4d5e-86e1-1960ac921c8f
title: SdbReleaseMatchingExe (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbReleaseMatchingExe
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: c98d9a79e8942f4bd3ea4c41119825d862de1418
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049143"
---
# <a name="sdbreleasematchingexe-function"></a>SdbReleaseMatchingExe (funzione)

Rilascia le risorse usate dalla funzione [**SdbGetMatchingExe**](sdbgetmatchingexe.md) .

## <a name="syntax"></a>Sintassi


```C++
void WINAPI SdbReleaseMatchingExe(
  _In_ HSDB   hSDB,
  _In_ TAGREF trExe
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hSDB* \[ in\]
</dt> <dd>

Handle per il database shim restituito dalla funzione [**SdbInitDatabase**](sdbinitdatabase.md) .

</dd> <dt>

*trExe* \[ in\]
</dt> <dd>

[**TAGREF**](tagref.md) restituito da [**SdbGetMatchingExe**](sdbgetmatchingexe.md).

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

[**SdbGetMatchingExe**](sdbgetmatchingexe.md)
</dt> <dt>

[**SdbInitDatabase**](sdbinitdatabase.md)
</dt> </dl>

 

 




