---
description: Cerca la corrispondenza di TAG successiva all'interno dell'elemento padre specificato e restituisce il TAGID della corrispondenza.
ms.assetid: c96aa1c1-b0e6-49f5-9f74-7d0e050bee3b
title: SdbFindNextTag (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbFindNextTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 7a5baf728a75e4c02c20ed4207b7d6b9a968af1e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877537"
---
# <a name="sdbfindnexttag-function"></a>SdbFindNextTag (funzione)

Cerca la corrispondenza di TAG successiva all'interno dell'elemento padre specificato e restituisce il **TagId** della corrispondenza.

## <a name="syntax"></a>Sintassi


```C++
TAGID WINAPI SdbFindNextTag(
  _In_ PDB   pdb,
  _In_ TAGID tiParent,
  _In_ TAGID tiPrev
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

</dd> <dt>

*tiPrev* \[ in\]
</dt> <dd>

**TagId** della corrispondenza precedente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

**TagId** della corrispondenza.

## <a name="remarks"></a>Commenti

Prima di chiamare questa funzione, chiamare la funzione [**SdbFindFirstTag**](sdbfindfirsttag.md) .

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

[**SdbTagRefToTagID**](sdbtagreftotagid.md)
</dt> </dl>

 

 




