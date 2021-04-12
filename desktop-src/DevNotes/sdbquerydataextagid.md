---
description: Recupera i dati dalle voci specificate appartenenti a una voce EXE.
ms.assetid: 355eecd6-a0c9-4448-9aed-a9c3eb3b2071
title: SdbQueryDataExTagID (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbQueryDataExTagID
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 8db16463d2923ce3c888de4f202e1ebc36584e99
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401368"
---
# <a name="sdbquerydataextagid-function"></a>SdbQueryDataExTagID (funzione)

Recupera i dati dalle voci specificate appartenenti a una voce EXE.

## <a name="syntax"></a>Sintassi


```C++
DWORD WINAPI SdbQueryDataExTagID(
  _In_        PDB     pdb,
  _In_        TAGID   tiExe,
  _In_opt_    LPCTSTR lpszDataName,
  _Out_opt_   LPDWORD lpdwDataType,
  _Out_       LPVOID  lpBuffer,
  _Inout_opt_ LPDWORD lpcbBufferSize,
  _Out_       TAGID   *ptiData
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PDB* \[ in\]
</dt> <dd>

Handle per il database shim.

</dd> <dt>

*tiExe* \[ in\]
</dt> <dd>

[**TagId**](tagid.md) della voce exe.

</dd> <dt>

*lpszDataName* \[ in, facoltativo\]
</dt> <dd>

Nome della voce di dati da recuperare. Per specificare più voci, separare i nomi con il carattere barra rovesciata (" \\ "). Se questo parametro è **null**, la funzione tenta di restituire tutte le voci di dati.

</dd> <dt>

*lpdwDataType* \[ out, facoltativo\]
</dt> <dd>

Tipo di dati delle voci restituite. Questo parametro può essere uno dei valori seguenti:

<dl><span id="REG_BINARY"></span><span id="reg_binary"></span><dt>

**REG \_ binario**
</dt><span id="REG_DWORD"></span><span id="reg_dword"></span><dt>

**REG \_ DWORD**
</dt><span id="REG_MULTI_SZ"></span><span id="reg_multi_sz"></span><dt>

**REG \_ - \_ SZ**
</dt><span id="REG_NONE"></span><span id="reg_none"></span><dt>

**REG \_ None**
</dt><span id="REG_QWORD"></span><span id="reg_qword"></span><dt>

**REG \_ QWORD**
</dt><span id="REG_SZ"></span><span id="reg_sz"></span><dt>

**REG \_ SZ**
</dt> </dl> </dd> <dt>

*lpBuffer* \[ out\]
</dt> <dd>

Buffer che riceve i dati. Se il buffer non è sufficientemente grande da contenere i dati, la funzione ha esito negativo e restituisce l' **errore \_ \_ buffer insufficiente**.

</dd> <dt>

*lpcbBufferSize* \[ in, out, facoltativo\]
</dt> <dd>

Dimensioni in byte del buffer *lpBuffer* .

</dd> <dt>

*ptiData* \[ out\]
</dt> <dd>

[**TagId**](tagid.md) della voce di dati.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione restituisce uno dei valori seguenti.



| Codice restituito                                                                                                    | Descrizione                                                            |
|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <dt>**ERRORE \_ parametro non valido \_**</dt> </dl>       | Uno o più parametri di input non sono corretti.<br/>                  |
| <dl> <dt>**ERRORE \_ di \_ danneggiamento interno del database \_**</dt> </dl> | Non sono state trovate voci di dati per la voce EXE.<br/>               |
| <dl> <dt>**ERRORE \_ buffer insufficiente \_**</dt> </dl>     | Il buffer non è sufficientemente grande da contenere le voci di dati.<br/> |
| <dl> <dt>**ERRORE \_ di \_ memoria insufficiente \_**</dt> </dl>      | Allocazione di memoria non riuscita.<br/>                               |
| <dl> <dt>**ERRORE \_ non \_ trovato**</dt> </dl>               | Impossibile trovare una voce di dati con il nome *lpszDataName* .<br/>    |
| <dl> <dt>**ERRORE \_ riuscito**</dt> </dl>                  | La funzione è stata completata correttamente.<br/>                        |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                         |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



 

 




