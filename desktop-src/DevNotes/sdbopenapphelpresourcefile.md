---
description: Carica il file di risorse apphelp.
ms.assetid: fca50e00-9324-410a-a572-69441f332593
title: SdbOpenApphelpResourceFile (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbOpenApphelpResourceFile
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 2f1dfb1695e25bfb82e01ffa4f9eac4e245a6ffa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401437"
---
# <a name="sdbopenapphelpresourcefile-function"></a>SdbOpenApphelpResourceFile (funzione)

Carica il file di risorse apphelp.

## <a name="syntax"></a>Sintassi


```C++
HMODULE WINAPI SdbOpenApphelpResourceFile(
  _In_opt_ LPCWSTR pwszACResourceFile
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pwszACResourceFile* \[ in, facoltativo\]
</dt> <dd>

Percorso del file di risorse. Se questo parametro è **null**, viene aperta la dll della risorsa locale.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

La funzione restituisce un handle per il file di risorse aperto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                         |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



 

 




