---
description: Recupera lo stato della cache File offline.
ms.assetid: a8cc0dbb-0005-4e74-892e-898e2ebe0465
title: CSCQueryDatabaseStatus (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSCQueryDatabaseStatus
api_type:
- DllExport
api_location:
- Cscmig.dll
ms.openlocfilehash: badd869306290609ccadeba80e6ea67ca3479be8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331683"
---
# <a name="cscquerydatabasestatus-function"></a>CSCQueryDatabaseStatus (funzione)

\[Questa funzione non è supportata e non deve essere utilizzata.\]

Recupera lo stato della cache File offline.

## <a name="syntax"></a>Sintassi


```C++
BOOL WINAPI CSCQueryDatabaseStatus(
   ULONG *pulStatus,
   ULONG *pulErrors
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pulStatus* 
</dt> <dd>

Stato. Questo parametro può avere uno dei valori seguenti.



| Valore                                                                                                                                                                                                                                                                                                               | Significato                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span id="FLAG_DATABASESTATUS_ENCRYPTED"></span><span id="flag_databasestatus_encrypted"></span><dl> <dt>**Flag \_ di 0x00000002 \_ crittografato DATABASESTATUS**</dt> <dt></dt> </dl>                                      | La cache è contrassegnata per la crittografia e tutti i file nella cache sono crittografati.<br/>                |
| <span id="FLAG_DATABASESTATUS_PARTIALLY_ENCRYPTED"></span><span id="flag_databasestatus_partially_encrypted"></span><dl> <dt>**Flag \_ di DATABASESTATUS \_ parzialmente \_ crittografato**</dt> <dt>0x00000004</dt> </dl>       | La cache è contrassegnata per la crittografia, ma alcuni file nella cache non sono crittografati.<br/>          |
| <span id="FLAG_DATABASESTATUS_PARTIALLY_UNENCRYPTED"></span><span id="flag_databasestatus_partially_unencrypted"></span><dl> <dt>**Flag \_ di DATABASESTATUS \_ parzialmente non \_ crittografato**</dt> <dt>0x00000004</dt> </dl> | La cache non è contrassegnata per la crittografia, ma non tutti i file nella cache sono stati decrittografati.<br/> |
| <span id="FLAG_DATABASESTATUS_UNENCRYPTED"></span><span id="flag_databasestatus_unencrypted"></span><dl> <dt>**Flag \_ di 0x00000000 DATABASESTATUS non \_ crittografati**</dt> <dt></dt> </dl>                                | La cache non è contrassegnata per la crittografia e tutti i file nella cache sono stati decrittografati.<br/>      |



 

</dd> <dt>

*pulErrors* 
</dt> <dd>

Questo parametro è un valore diverso da zero se si verifica un errore interno del database o 0 in caso contrario.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione restituisce **true** se ha esito positivo; in caso contrario, restituisce **false**.

## <a name="remarks"></a>Commenti

A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|---------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Cscmig.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CSCIsCSCEnabled**](csciscscenabled.md)
</dt> </dl>

 

 
