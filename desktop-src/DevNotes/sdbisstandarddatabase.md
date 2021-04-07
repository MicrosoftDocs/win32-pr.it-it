---
description: Determina se il database specificato è uno dei database standard (SysMain, AppHelp, Drvmain o Msimain).
ms.assetid: 7d7e3ca7-535e-40b3-b635-299eff8abea5
title: SdbIsStandardDatabase (funzione)
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
ms.openlocfilehash: 9e9e445162c2bfc171ccf975981876f81a8bb804
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049081"
---
# <a name="sdbisstandarddatabase-function"></a>SdbIsStandardDatabase (funzione)

Determina se il database specificato è uno dei database standard (SysMain, AppHelp, Drvmain o Msimain).

## <a name="syntax"></a>Sintassi


```C++
BOOL WINAPI SdbIsStandardDatabase(
  _In_ GUID GuidDB
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*GuidDB* \[ in\]
</dt> <dd>

GUID del database.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

La funzione restituisce **true** se il GUID rappresenta un database standard o **false** in caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                         |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



 

 




