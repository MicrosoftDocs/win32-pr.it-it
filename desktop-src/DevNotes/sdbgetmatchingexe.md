---
description: Cerca il file eseguibile specificato.
ms.assetid: 32c6b054-7e47-4427-bdfe-6b5066db4ac3
title: SdbGetMatchingExe (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetMatchingExe
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 9d9c8c8c5e9ba0c55068558698b40c7274929364
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877694"
---
# <a name="sdbgetmatchingexe-function"></a>SdbGetMatchingExe (funzione)

Cerca il file eseguibile specificato.

## <a name="syntax"></a>Sintassi


```C++
BOOL WINAPI SdbGetMatchingExe(
  _In_opt_ HSDB            hSDB,
  _In_     LPCTSTR         szPath,
  _In_opt_ LPCTSTR         szModuleName,
  _In_opt_ LPCTSTR         pszEnvironment,
  _In_     DWORD           dwFlags,
  _Out_    PSDBQUERYRESULT pQueryResult
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hSDB* \[ in, facoltativo\]
</dt> <dd>

Handle per il database shim restituito dalla funzione [**SdbInitDatabase**](sdbinitdatabase.md) .

</dd> <dt>

*szPath* \[ in\]
</dt> <dd>

Percorso del file eseguibile.

</dd> <dt>

*szModuleName* \[ in, facoltativo\]
</dt> <dd>

Nome del modulo.

</dd> <dt>

*pszEnvironment* \[ in, facoltativo\]
</dt> <dd>

Variabili di ambiente da utilizzare come contesto di ricerca.

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Questo parametro può essere 0 o **SDBGMEF \_ Ignora \_ ambiente** (0x1).

</dd> <dt>

*pQueryResult* \[ out\]
</dt> <dd>

Struttura [**SDBQUERYRESULT**](sdbqueryresult.md) . Se non viene trovata alcuna corrispondenza, la struttura contiene **TAGREF \_ null**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

La funzione restituisce **true** in caso di esito positivo o **false** in caso di errore.

## <a name="remarks"></a>Commenti

Una volta completato il [**TAGREF**](tagref.md)restituito, liberarlo utilizzando la funzione [**SdbReleaseMatchingExe**](sdbreleasematchingexe.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                         |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SdbInitDatabase**](sdbinitdatabase.md)
</dt> <dt>

[**SdbReleaseMatchingExe**](sdbreleasematchingexe.md)
</dt> </dl>

 

 




