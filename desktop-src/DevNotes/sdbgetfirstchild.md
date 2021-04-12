---
description: Cerca un TAG figlio all'interno dell'elemento padre specificato e restituisce l'TAGID del primo elemento figlio.
ms.assetid: 67538c7e-6360-40fa-b50f-dcbc7a6a147d
title: SdbGetFirstChild (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetFirstChild
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: abc06ae0e4b5d842a968d0f3fbeb7a15702660b9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104522802"
---
# <a name="sdbgetfirstchild-function"></a>SdbGetFirstChild (funzione)

Cerca un TAG figlio all'interno dell'elemento padre specificato e restituisce l' **TagId** del primo elemento figlio.

## <a name="syntax"></a>Sintassi


```C++
TAGID WINAPI SdbGetFirstChild(
  _In_ PDB   pdb,
  _In_ TAGID tiParent
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PDB* \[ in\]
</dt> <dd>

Handle per il database shim.

</dd> <dt>

*tiParent* \[ in\]
</dt> <dd>

**TagId** di inizio della ricerca. Questo parametro può essere un **\_ \_ elenco di tipi di tag** o **\_ radice TagId** .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

**TagId** del primo **\_ valore null** figlio o TagId non è stato trovato alcun elemento figlio.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SdbFindFirstTag**](sdbfindfirsttag.md)
</dt> <dt>

[**SdbFindNextTag**](sdbfindnexttag.md)
</dt> <dt>

[**SdbGetNextChild**](sdbgetnextchild.md)
</dt> </dl>

 

 




