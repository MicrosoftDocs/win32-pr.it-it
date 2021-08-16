---
title: Funzione DsBackupEnd (Ntdsbcli.h)
description: Chiamato per terminare un'operazione di backup.
ms.assetid: 872645bc-3dbe-4b12-af4f-778d54feb18f
ms.tgt_platform: multiple
keywords:
- Funzione DsBackupEnd active Directory
topic_type:
- apiref
api_name:
- DsBackupEnd
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 479a1641a6d347837733da7e7d26e67b2011654e638681ec774a6ec5d931e211
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118430251"
---
# <a name="dsbackupend-function"></a>Funzione DsBackupEnd

\[Questa funzione è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile. A partire da Windows Vista, [usare Servizio Copia Shadow del volume (VSS).](../vss/volume-shadow-copy-service-overview.md)\]

La **funzione DsBackupEnd** viene chiamata per terminare un'operazione di backup.

## <a name="syntax"></a>Sintassi


```C++
HRESULT DsBackupEnd(
  _In_ HBC hbc
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hbc* \[ Pollici\]
</dt> <dd>

Contiene l'handle del contesto di backup ottenuto con [**la funzione DsBackupPrepare.**](dsbackupprepare.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **S \_ OK se** la funzione ha esito positivo o un codice di errore Win32 o RPC in caso contrario. Nell'elenco seguente sono elencati altri possibili codici di errore.

<dl> <dt>

**ERRORE \_ PARAMETRO NON \_ VALIDO**
</dt> <dd>

*hbc* non è valido.

</dd> </dl>

## <a name="remarks"></a>Commenti

La **funzione DsBackupEnd** chiude gli handle di associazione in sospeso ed esegue una pulizia dopo un tentativo di backup riuscito o non riuscito.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Ntdsbcli.h</dt> </dl>   |
| Libreria<br/>                  | <dl> <dt>Ntdsbcli.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ntdsbcli.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**DsSetAuthIdentity**](dssetauthidentity.md)
</dt> <dt>

[Backup di un server Active Directory](backing-up-an-active-directory-server.md)
</dt> <dt>

[Funzioni di backup della directory](directory-backup-functions.md)
</dt> </dl>

 

