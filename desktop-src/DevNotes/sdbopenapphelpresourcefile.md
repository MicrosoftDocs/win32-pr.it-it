---
description: Carica il file di risorse Apphelp.
ms.assetid: fca50e00-9324-410a-a572-69441f332593
title: Funzione SdbOpenApphelpResourceFile
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
ms.openlocfilehash: ab865a29e0879119ca50cf4177aa7649bd82a83e70c07e1b7068a5d8fcd2cc30
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120044991"
---
# <a name="sdbopenapphelpresourcefile-function"></a>Funzione SdbOpenApphelpResourceFile

Carica il file di risorse Apphelp.

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

Percorso del file di risorse. Se questo parametro è **NULL,** viene aperta la DLL della risorsa locale.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

La funzione restituisce un handle per il file di risorse aperto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                         |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



 

 




