---
title: Funzione DsRestoreRegisterComplete (Ntdsbcli.h)
description: Chiamato per sbloccare un server Active Directory dopo il completamento di un'operazione di ripristino.
ms.assetid: 781cd2ec-d2e2-4f3a-903d-feda4b871de5
ms.tgt_platform: multiple
keywords:
- Funzione DsRestoreRegisterComplete in Active Directory
topic_type:
- apiref
api_name:
- DsRestoreRegisterComplete
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b335f67ed4d392d189553f66655797e03121cbdee6ce19dffbd9803199f6c72
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118429929"
---
# <a name="dsrestoreregistercomplete-function"></a>Funzione DsRestoreRegisterComplete

\[Questa funzione è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile. Usare [Servizio Copia Shadow del volume (VSS).](../vss/volume-shadow-copy-service-overview.md)\]

La **funzione DsRestoreRegisterComplete** viene chiamata per sbloccare un server Active Directory dopo il completamento di un'operazione di ripristino. Questa funzione è la controparte [**della funzione DsRestoreRegister.**](dsrestoreregister.md)

## <a name="syntax"></a>Sintassi


```C++
HRESULT DsRestoreRegisterComplete(
  _In_ HBC     hbc,
  _In_ HRESULT hrRestoreState
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hbc* \[ Pollici\]
</dt> <dd>

Contiene l'handle del contesto di ripristino ottenuto [**con la funzione DsRestorePrepare.**](dsrestoreprepare.md)

</dd> <dt>

*hrRestoreState* \[ Pollici\]
</dt> <dd>

Contiene lo stato finale dell'operazione di ripristino. Questo parametro deve contenere **S \_ OK se** l'operazione di ripristino ha avuto esito positivo o un codice di errore in caso contrario.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **S \_ OK se** la funzione ha esito positivo oppure un codice di errore Win32 o RPC in caso contrario. Nell'elenco seguente sono elencati i codici di errore possibili.

<dl> <dt>

**ERRORE \_ DI \_ ACCESSO NEGATO**
</dt> <dd>

Il chiamante non dispone dei privilegi di accesso adeguati per chiamare questa funzione. La [**funzione DsSetAuthIdentity**](dssetauthidentity.md) può essere usata per impostare le credenziali da usare per le funzioni di backup e ripristino.

</dd> </dl>

## <a name="remarks"></a>Commenti

Prima di riavviare il controller di dominio, chiamare questa funzione per specificare lo stato dell'operazione di ripristino. Se lo stato non riesce, il servizio directory verrà avviato solo dopo il ripristino di un database valido. Questa funzione completa l'operazione di ripristino e consente Active Directory Domain Services'avvio.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                               |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                               |
| Fine del supporto client<br/>    | Nessuno supportato<br/>                                                               |
| Fine del supporto server<br/>    | Nessuno supportato<br/>                                                               |
| Intestazione<br/>                   | <dl> <dt>Ntdsbcli.h</dt> </dl>   |
| Libreria<br/>                  | <dl> <dt>Ntdsbcli.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ntdsbcli.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**DsRestoreRegister**](dsrestoreregister.md)
</dt> <dt>

[**DsRestorePrepare**](dsrestoreprepare.md)
</dt> <dt>

[**DsSetAuthIdentity**](dssetauthidentity.md)
</dt> <dt>

[Ripristino di un server Active Directory](restoring-an-active-directory-server.md)
</dt> <dt>

[Funzioni di backup della directory](directory-backup-functions.md)
</dt> </dl>

 

