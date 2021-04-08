---
description: Libera i dati dell'attributo di file specificati.
ms.assetid: c1a4dcf8-614f-49a5-a923-8d7d610e6406
title: SdbFreeFileAttributes (funzione)
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
ms.openlocfilehash: 6f28812fbbec83dd1a41c8a21cb4c9544dbefea5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103747687"
---
# <a name="sdbfreefileattributes-function"></a>SdbFreeFileAttributes (funzione)

Libera i dati dell'attributo di file specificati.

## <a name="syntax"></a>Sintassi


```C++
BOOL WINAPI SdbFreeFileAttributes(
  _In_ PATTRINFO pFileAttributes
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pFileAttributes* \[ in\]
</dt> <dd>

Struttura [**ATTRINFO**](attrinfo.md) restituita dalla funzione [**SdbGetFileAttributes**](sdbgetfileattributes.md) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

La funzione restituisce **true** in caso di esito positivo o **false** in caso di errore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                         |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SdbGetFileAttributes**](sdbgetfileattributes.md)
</dt> </dl>

 

 




