---
description: Recupera i dati dalle voci specificate appartenenti a una voce EXE.
ms.assetid: 355eecd6-a0c9-4448-9aed-a9c3eb3b2071
title: Funzione SdbQueryDataExTagID
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
ms.openlocfilehash: 19477385fb70f65c560d1a13d479fc4c2ce1853220aff6ac32a75f3634a40d71
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119815381"
---
# <a name="sdbquerydataextagid-function"></a>Funzione SdbQueryDataExTagID

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

*pdb* \[ Pollici\]
</dt> <dd>

Handle per il database shim.

</dd> <dt>

*tiExe* \[ Pollici\]
</dt> <dd>

[**TAGID della**](tagid.md) voce EXE.

</dd> <dt>

*lpszDataName* \[ in, facoltativo\]
</dt> <dd>

Nome della voce di dati da recuperare. Per specificare più voci, separare i nomi con il carattere barra rovesciata (" \\ "). Se questo parametro è **NULL,** la funzione tenta di restituire tutte le voci di dati.

</dd> <dt>

*lpdwDataType* \[ out, facoltativo\]
</dt> <dd>

Tipo di dati delle voci restituite. Questo parametro può essere uno dei valori seguenti:

<dl><span id="REG_BINARY"></span><span id="reg_binary"></span><dt>

**REG \_ BINARY**
</dt><span id="REG_DWORD"></span><span id="reg_dword"></span><dt>

**REG \_ DWORD**
</dt><span id="REG_MULTI_SZ"></span><span id="reg_multi_sz"></span><dt>

**REG \_ MULTI \_ SZ**
</dt><span id="REG_NONE"></span><span id="reg_none"></span><dt>

**REG \_ NONE**
</dt><span id="REG_QWORD"></span><span id="reg_qword"></span><dt>

**REG \_ QWORD**
</dt><span id="REG_SZ"></span><span id="reg_sz"></span><dt>

**REG \_ SZ**
</dt> </dl> </dd> <dt>

*lpBuffer* \[ Cambio\]
</dt> <dd>

Buffer che riceve i dati. Se le dimensioni del buffer non sono sufficienti per contenere i dati, la funzione ha esito negativo e restituisce **ERROR \_ INSUFFICIENT \_ BUFFER**.

</dd> <dt>

*lpcbBufferSize* \[ in, out, facoltativo\]
</dt> <dd>

Dimensioni del buffer *lpBuffer,* in byte.

</dd> <dt>

*ptiData* \[ Cambio\]
</dt> <dd>

[**TAGID della**](tagid.md) voce di dati.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione restituisce uno dei valori seguenti.



| Codice restituito                                                                                                    | Descrizione                                                            |
|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <dt>**ERRORE \_ PARAMETRO NON \_ VALIDO**</dt> </dl>       | Uno o più parametri di input non sono corretti.<br/>                  |
| <dl> <dt>**ERRORE \_ INTERNO \_ DEL \_ DATABASE**</dt> </dl> | Non sono state trovate voci di dati per la voce EXE.<br/>               |
| <dl> <dt>**ERRORE \_ BUFFER \_ INSUFFICIENTE**</dt> </dl>     | Le dimensioni del buffer non sono sufficienti per contenere le voci di dati.<br/> |
| <dl> <dt>**ERRORE \_ MEMORIA \_ \_ INSUFFICIENTE**</dt> </dl>      | Allocazione di memoria non riuscita.<br/>                               |
| <dl> <dt>**ERRORE \_ NON \_ TROVATO**</dt> </dl>               | Non è stata trovata una voce di dati con il nome *lpszDataName.*<br/>    |
| <dl> <dt>**ERRORE \_ RIUSCITO**</dt> </dl>                  | La funzione è stata completata correttamente.<br/>                        |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                         |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



 

 




