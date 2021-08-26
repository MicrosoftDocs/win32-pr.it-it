---
description: Rilascia le risorse usate dalla funzione SdbGetMatchingExe.
ms.assetid: 4a784f72-2108-4d5e-86e1-1960ac921c8f
title: Funzione SdbReleaseMatchingExe
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
ms.openlocfilehash: 710874fc0e57775eb6ad1c9c6681a5b74dc66d133b22ce23d2ac0d27270ef7f1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120044921"
---
# <a name="sdbreleasematchingexe-function"></a>Funzione SdbReleaseMatchingExe

Rilascia le risorse usate dalla [**funzione SdbGetMatchingExe.**](sdbgetmatchingexe.md)

## <a name="syntax"></a>Sintassi


```C++
void WINAPI SdbReleaseMatchingExe(
  _In_ HSDB   hSDB,
  _In_ TAGREF trExe
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hSDB* \[ Pollici\]
</dt> <dd>

Handle per il database shim restituito dalla [**funzione SdbInitDatabase.**](sdbinitdatabase.md)

</dd> <dt>

*trExe* \[ Pollici\]
</dt> <dd>

TAGREF [**restituito**](tagref.md) da [**SdbGetMatchingExe.**](sdbgetmatchingexe.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                         |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SdbGetMatchingExe**](sdbgetmatchingexe.md)
</dt> <dt>

[**SdbInitDatabase**](sdbinitdatabase.md)
</dt> </dl>

 

 




