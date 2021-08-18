---
description: Determina se il database specificato è uno dei database standard (Sysmain, Apphelp, Drvmain o Msimain).
ms.assetid: 7d7e3ca7-535e-40b3-b635-299eff8abea5
title: Funzione SdbIsStandardDatabase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbIsStandardDatabase
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 7ef30f54b4d8eb4df4d8f136de6357a072cdb0183f462cb3af8a9340ce68b0c6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120045191"
---
# <a name="sdbisstandarddatabase-function"></a>Funzione SdbIsStandardDatabase

Determina se il database specificato è uno dei database standard (Sysmain, Apphelp, Drvmain o Msimain).

## <a name="syntax"></a>Sintassi


```C++
BOOL WINAPI SdbIsStandardDatabase(
  _In_ GUID GuidDB
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*GuidDB* \[ Pollici\]
</dt> <dd>

GUID per il database.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

La funzione restituisce **TRUE se** il GUID rappresenta un database standard o FALSE in **caso contrario.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                         |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



 

 




