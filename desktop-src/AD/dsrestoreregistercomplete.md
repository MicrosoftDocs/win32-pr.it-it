---
title: Funzione DsRestoreRegisterComplete (ntdsbcli. h)
description: Chiamata eseguita per sbloccare un server Active Directory al termine di un'operazione di ripristino.
ms.assetid: 781cd2ec-d2e2-4f3a-903d-feda4b871de5
ms.tgt_platform: multiple
keywords:
- Active Directory funzione DsRestoreRegisterComplete
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
ms.openlocfilehash: ff5e5e01b29281860dff59fbcd08a3b48ec66c4a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048482"
---
# <a name="dsrestoreregistercomplete-function"></a>DsRestoreRegisterComplete (funzione)

\[Questa funzione è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile. In alternativa, usare [servizio Copia Shadow del volume (VSS)](../vss/volume-shadow-copy-service-overview.md) .\]

La funzione **DsRestoreRegisterComplete** viene chiamata per sbloccare un server Active Directory al termine di un'operazione di ripristino. Questa funzione è controparte della funzione [**DsRestoreRegister**](dsrestoreregister.md) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT DsRestoreRegisterComplete(
  _In_ HBC     hbc,
  _In_ HRESULT hrRestoreState
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*HBC* \[ in\]
</dt> <dd>

Contiene l'handle del contesto di ripristino ottenuto con la funzione [**DsRestorePrepare**](dsrestoreprepare.md) .

</dd> <dt>

*hrRestoreState* \[ in\]
</dt> <dd>

Contiene lo stato finale dell'operazione di ripristino. Questo parametro deve contenere **S \_ OK** se l'operazione di ripristino è stata eseguita correttamente o un codice di errore in caso contrario.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **\_ OK** se la funzione ha esito positivo o un codice di errore Win32 o RPC in caso contrario. Nell'elenco seguente sono elencati i possibili codici di errore.

<dl> <dt>

**ERRORE di \_ accesso \_ negato**
</dt> <dd>

Il chiamante non dispone dei privilegi di accesso appropriati per chiamare questa funzione. La funzione [**DsSetAuthIdentity**](dssetauthidentity.md) può essere utilizzata per impostare le credenziali da utilizzare per le funzioni di backup e ripristino.

</dd> </dl>

## <a name="remarks"></a>Commenti

Prima di riavviare il controller di dominio, chiamare questa funzione per fornire lo stato dell'operazione di ripristino. Se lo stato ha esito negativo, il servizio directory non viene avviato fino a quando non viene ripristinato un database valido. Questa funzione completa l'operazione di ripristino e consente l'avvio Active Directory Domain Services.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                               |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                               |
| Fine del supporto client<br/>    | Nessuno supportato<br/>                                                               |
| Fine del supporto server<br/>    | Nessuno supportato<br/>                                                               |
| Intestazione<br/>                   | <dl> <dt>Ntdsbcli. h</dt> </dl>   |
| Libreria<br/>                  | <dl> <dt>Ntdsbcli. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ntdsbcli.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**DsRestoreRegister**](dsrestoreregister.md)
</dt> <dt>

[**DsRestorePrepare**](dsrestoreprepare.md)
</dt> <dt>

[**DsSetAuthIdentity**](dssetauthidentity.md)
</dt> <dt>

[Ripristino di un server di Active Directory](restoring-an-active-directory-server.md)
</dt> <dt>

[Funzioni di backup della directory](directory-backup-functions.md)
</dt> </dl>

 

