---
description: Recupera TAGID e un handle per il database shim per il TAGREF specificato.
ms.assetid: 869c6af5-4c10-4358-9d6a-1a354be6f4e9
title: SdbTagRefToTagID (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbTagRefToTagID
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: faff00adc25a741342e586adea2f645a62eca36d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126387"
---
# <a name="sdbtagreftotagid-function"></a>SdbTagRefToTagID (funzione)

Recupera **TagId** e un handle per il database shim per il [**TAGREF**](tagref.md)specificato.

## <a name="syntax"></a>Sintassi


```C++
BOOL WINAPI SdbTagRefToTagID(
  _In_  HSDB   hSDB,
  _In_  TAGREF trWhich,
  _Out_ PDB    *ppdb,
  _Out_ TAGID  *ptiWhich
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hSDB* \[ in\]
</dt> <dd>

Handle per il database shim restituito dalla funzione [**SdbInitDatabase**](sdbinitdatabase.md) .

</dd> <dt>

*trWhich* \[ in\]
</dt> <dd>

[**TAGREF**](tagref.md).

</dd> <dt>

*PPDB* \[ out\]
</dt> <dd>

Handle risultante per il database shim.

</dd> <dt>

*ptiWhich* \[ out\]
</dt> <dd>

**TagId** risultante.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

La funzione restituisce **true** in caso di esito positivo o **false** in caso di errore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SdbInitDatabase**](sdbinitdatabase.md)
</dt> <dt>

[**TAGID**](tagid.md)
</dt> <dt>

[**TAGREF**](tagref.md)
</dt> </dl>

 

 




