---
title: Funzione DsSetCurrentBackupLog (ntdsbcli. h)
description: Imposta il numero di log di backup corrente dopo un ripristino riuscito.
ms.assetid: 903bddea-c5a7-4b3f-819c-0467a9c5ae1b
ms.tgt_platform: multiple
keywords:
- Active Directory funzione DsSetCurrentBackupLog
topic_type:
- apiref
api_name:
- DsSetCurrentBackupLog
- DsSetCurrentBackupLogA
- DsSetCurrentBackupLogW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f50fc41317ae22ae89c47f63bb19f981563e5c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874057"
---
# <a name="dssetcurrentbackuplog-function"></a>DsSetCurrentBackupLog (funzione)

\[Questa funzione è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile. A partire da Windows Vista, usare invece [servizio Copia Shadow del volume (VSS)](../vss/volume-shadow-copy-service-overview.md) .\]

La funzione **DsSetCurrentBackupLog** imposta il numero di log di backup corrente dopo un ripristino riuscito. Poiché Active Directory Domain Services supporta solo la registrazione circolare, questa funzione non viene in genere utilizzata.

## <a name="syntax"></a>Sintassi


```C++
HRESULT DsSetCurrentBackupLog(
  _In_ LPCWSTR szServerName,
  _In_ DWORD   dwCurrentLog
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*szServerName* \[ in\]
</dt> <dd>

Puntatore a una stringa con terminazione null che contiene il nome del server per il quale impostare il numero di log di backup. Le barre rovesciate precedenti sono facoltative. Il server deve essere lo stesso computer da cui viene chiamata la funzione. Il nome del server non può contenere caratteri di sottolineatura ( \_ ). Un esempio di nome di server è " \\ \\ Server1".

</dd> <dt>

*dwCurrentLog* \[ in\]
</dt> <dd>

Contiene il numero di log di backup da impostare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **\_ OK** se la funzione ha esito positivo o un codice di errore Win32 o RPC in caso contrario. Nell'elenco seguente sono elencati i possibili codici di errore.

<dl> <dt>

**ERRORE \_ parametro non valido \_**
</dt> <dd>

Uno o più parametri non sono validi.

</dd> <dt>

**ERRORE \_ di \_ memoria insufficiente \_**
</dt> <dd>

Si è verificato un errore di allocazione della memoria.

</dd> </dl>

## <a name="remarks"></a>Commenti

In genere non è necessario chiamare la funzione **DsSetCurrentBackupLog** . Le funzioni di backup determinano e impostano automaticamente il backup dell'ultimo numero di log. Usare **DsSetCurrentBackupLog** per evitare che un altro backup incrementale riesca fino a quando non viene eseguito un backup completo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Ntdsbcli. h</dt> </dl>   |
| Libreria<br/>                  | <dl> <dt>Ntdsbcli. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ntdsbcli.dll</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **DsSetCurrentBackupLogW** (Unicode) e **DsSetCurrentBackupLogA** (ANSI)<br/>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Backup e ripristino di un server di Active Directory](backing-up-and-restoring-an-active-directory-server.md)
</dt> <dt>

[Funzioni di backup della directory](directory-backup-functions.md)
</dt> </dl>

 

