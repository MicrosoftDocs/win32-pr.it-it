---
description: Libera i dati dell'attributo di file specificato.
ms.assetid: c1a4dcf8-614f-49a5-a923-8d7d610e6406
title: Funzione SdbFreeFileAttributes
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbFreeFileAttributes
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 7e99180198f8f23ba6b6872502710b2af28aaff3999a9f315c33ef2d1874d987
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120103671"
---
# <a name="sdbfreefileattributes-function"></a>Funzione SdbFreeFileAttributes

Libera i dati dell'attributo di file specificato.

## <a name="syntax"></a>Sintassi


```C++
BOOL WINAPI SdbFreeFileAttributes(
  _In_ PATTRINFO pFileAttributes
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pFileAttributes* \[ Pollici\]
</dt> <dd>

Struttura [**ATTRINFO**](attrinfo.md) restituita dalla [**funzione SdbGetFileAttributes.**](sdbgetfileattributes.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

La funzione restituisce **TRUE in caso** di esito positivo o FALSE **in** caso di esito negativo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                         |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SdbGetFileAttributes**](sdbgetfileattributes.md)
</dt> </dl>

 

 




