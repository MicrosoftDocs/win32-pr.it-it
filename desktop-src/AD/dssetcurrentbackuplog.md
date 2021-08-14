---
title: Funzione DsSetCurrentBackupLog (Ntdsbcli.h)
description: Imposta il numero di log di backup corrente dopo un ripristino riuscito.
ms.assetid: 903bddea-c5a7-4b3f-819c-0467a9c5ae1b
ms.tgt_platform: multiple
keywords:
- Funzione DsSetCurrentBackupLog active Directory
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
ms.openlocfilehash: ab10ac21d1a3cb2501a809b938252414c756bdfbd62f1e142ba3b902cde8c291
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118191780"
---
# <a name="dssetcurrentbackuplog-function"></a>Funzione DsSetCurrentBackupLog

\[Questa funzione è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile. A partire da Windows Vista, [usare Servizio Copia Shadow del volume (VSS).](../vss/volume-shadow-copy-service-overview.md)\]

La **funzione DsSetCurrentBackupLog** imposta il numero di log di backup corrente dopo un ripristino riuscito. Poiché Active Directory Domain Services solo la registrazione circolare, questa funzione non viene in genere usata.

## <a name="syntax"></a>Sintassi


```C++
HRESULT DsSetCurrentBackupLog(
  _In_ LPCWSTR szServerName,
  _In_ DWORD   dwCurrentLog
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*szServerName* \[ Pollici\]
</dt> <dd>

Puntatore a una stringa con terminazione Null contenente il nome del server per cui impostare il numero di log di backup. Le barre rovesciate precedenti sono facoltative. Il server deve essere lo stesso computer da cui viene chiamata questa funzione. Il nome del server non può contenere caratteri di sottolineatura ( \_ ). Un esempio di nome server è \\ \\ "server1".

</dd> <dt>

*dwCurrentLog* \[ Pollici\]
</dt> <dd>

Contiene il numero del log di backup da impostare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **S \_ OK se** la funzione ha esito positivo o un codice di errore Win32 o RPC in caso contrario. Nell'elenco seguente sono elencati i possibili codici di errore.

<dl> <dt>

**ERRORE \_ PARAMETRO NON \_ VALIDO**
</dt> <dd>

Uno o più parametri non sono validi.

</dd> <dt>

**MEMORIA \_ INSUFFICIENTE \_ PER \_ L'ERRORE**
</dt> <dd>

Si è verificato un errore di allocazione della memoria.

</dd> </dl>

## <a name="remarks"></a>Commenti

In genere non è necessario chiamare la **funzione DsSetCurrentBackupLog.** Le funzioni di backup determinano e impostano automaticamente l'ultimo numero di log di cui è stato eseguito il backup. Usare **DsSetCurrentBackupLog** per impedire il completamento di un altro backup incrementale fino a quando non viene eseguito un backup completo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Ntdsbcli.h</dt> </dl>   |
| Libreria<br/>                  | <dl> <dt>Ntdsbcli.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ntdsbcli.dll</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **DsSetCurrentBackupLogW** (Unicode) e **DsSetCurrentBackupLogA** (ANSI)<br/>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Backup e ripristino di un server Active Directory](backing-up-and-restoring-an-active-directory-server.md)
</dt> <dt>

[Funzioni di backup della directory](directory-backup-functions.md)
</dt> </dl>

 

