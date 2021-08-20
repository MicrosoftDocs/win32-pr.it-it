---
description: Trova il primo record DWORD nell'indice specificato che soddisfa i criteri specificati.
ms.assetid: 81302f84-497d-4fef-b348-eee2a53284c7
title: Funzione SdbFindFirstDWORDIndexedTag
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
ms.openlocfilehash: 40f54dfc109ec2f7f4807d57052b9c4e1f99d5b629e8028be2931d9b42081f43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118161572"
---
# <a name="sdbfindfirstdwordindexedtag-function"></a>Funzione SdbFindFirstDWORDIndexedTag

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

*pdb* \[ Pollici\]
</dt> <dd>

Handle per il database shim.

</dd> <dt>

*tWhich* \[ Pollici\]
</dt> <dd>

Tipo di indice. Per un elenco di valori, vedere [**TAG.**](tag.md)

</dd> <dt>

*tKey* \[ Pollici\]
</dt> <dd>

Tipo di chiave.

</dd> <dt>

*dwName* \[ Pollici\]
</dt> <dd>

Nome dei dati da trovare. Questo valore verrà convertito in una chiave.

</dd> <dt>

*pFindInfo* \[ Cambio\]
</dt> <dd>

Struttura [**FIND \_ INFO**](find-info.md) che riceve il record.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

**TAGID della** prima corrispondenza o **TAG \_ NULL** se non viene trovata alcuna corrispondenza.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                         |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SdbFindFirstTag**](sdbfindfirsttag.md)
</dt> </dl>

 

 




