---
description: Cerca una corrispondenza di TAG all'interno dell'elemento padre specificato e restituisce il TAGID della prima corrispondenza.
ms.assetid: ecbe216c-1e46-4472-b1d1-e2ac7ace82ab
title: SdbFindFirstTag (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbFindFirstTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: dc8b752d536be83d90ded55474166d14521f0f7a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103965873"
---
# <a name="sdbfindfirsttag-function"></a>SdbFindFirstTag (funzione)

Cerca una corrispondenza di TAG all'interno dell'elemento padre specificato e restituisce il **TagId** della prima corrispondenza.

## <a name="syntax"></a>Sintassi


```C++
TAGID WINAPI SdbFindFirstTag(
  _In_ PDB   pdb,
  _In_ TAGID tiParent,
  _In_ TAG   tTag
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

*tTag* \[ in\]
</dt> <dd>

TAG per cui trovare una corrispondenza. Per un elenco di valori possibili, vedere [tag](tag.md) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

**TagId** della prima corrispondenza.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SdbFindNextTag**](sdbfindnexttag.md)
</dt> <dt>

[**SdbTagRefToTagID**](sdbtagreftotagid.md)
</dt> </dl>

 

 




