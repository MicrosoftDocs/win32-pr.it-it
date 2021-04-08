---
description: Cerca il TAG figlio successivo all'interno dell'elemento padre specificato e restituisce il TAGID dell'elemento figlio successivo.
ms.assetid: c7311f20-15ca-4b2d-a08d-8bb992a3a0cd
title: SdbGetNextChild (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetNextChild
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 4f2943eaf0baec84a9473b679743b9eafad3b7fb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877693"
---
# <a name="sdbgetnextchild-function"></a>SdbGetNextChild (funzione)

Cerca il TAG figlio successivo all'interno dell'elemento padre specificato e restituisce il **TagId** dell'elemento figlio successivo.

## <a name="syntax"></a>Sintassi


```C++
TAGID WINAPI SdbGetNextChild(
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

**TagId** del figlio precedente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

**TagId** dell'elemento figlio o **TagId \_ null** se non viene trovato alcun elemento figlio.

## <a name="remarks"></a>Commenti

Prima di chiamare questa funzione, chiamare la funzione [**SdbGetFirstChild**](sdbgetfirstchild.md) .

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

[**SdbGetFirstChild**](sdbgetfirstchild.md)
</dt> </dl>

 

 




