---
description: Trova il primo record DWORD nell'indice specificato che soddisfa i criteri specificati.
ms.assetid: 81302f84-497d-4fef-b348-eee2a53284c7
title: SdbFindFirstDWORDIndexedTag (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbFindFirstDWORDIndexedTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 4f3c9290f98fb24d856561114bc654da0315c5a7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104522817"
---
# <a name="sdbfindfirstdwordindexedtag-function"></a>SdbFindFirstDWORDIndexedTag (funzione)

Trova il primo record **DWORD** nell'indice specificato che soddisfa i criteri specificati.

## <a name="syntax"></a>Sintassi


```C++
TAGID WINAPI SdbFindFirstDWORDIndexedTag(
  _In_  PDB       pdb,
  _In_  TAG       tWhich,
  _In_  TAG       tKey,
  _In_  DWORD     dwName,
  _Out_ FIND_INFO *pFindInfo
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PDB* \[ in\]
</dt> <dd>

Handle per il database shim.

</dd> <dt>

*tWhich* \[ in\]
</dt> <dd>

Tipo di indice. Per un elenco di valori, vedere [**tag**](tag.md) .

</dd> <dt>

*tKey* \[ in\]
</dt> <dd>

Tipo di chiave.

</dd> <dt>

*dwName* \[ in\]
</dt> <dd>

Nome dei dati da trovare. Questo valore verrà convertito in una chiave.

</dd> <dt>

*pFindInfo* \[ out\]
</dt> <dd>

Struttura [**di \_ informazioni di ricerca**](find-info.md) che riceve il record.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

**TagId** della prima corrispondenza o **tag \_ null** se non viene trovata alcuna corrispondenza.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                         |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SdbFindFirstTag**](sdbfindfirsttag.md)
</dt> </dl>

 

 




