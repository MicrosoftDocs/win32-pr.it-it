---
title: Funzione DsIsNTDSOnline (ntdsbcli. h)
description: Determina se Active Directory Domain Services sono online nel server specificato.
ms.assetid: 8f46e4d8-6d05-402c-a5b4-291fd2d6609b
ms.tgt_platform: multiple
keywords:
- Active Directory funzione DsIsNTDSOnline
topic_type:
- apiref
api_name:
- DsIsNTDSOnline
- DsIsNTDSOnlineA
- DsIsNTDSOnlineW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57f6728f4481eb8820055b48f10cfa0f94c7aaa1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119850"
---
# <a name="dsisntdsonline-function"></a>DsIsNTDSOnline (funzione)

\[Questa funzione è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile. A partire da Windows Vista, usare invece [servizio Copia Shadow del volume (VSS)](../vss/volume-shadow-copy-service-overview.md) .\]

La funzione **DsIsNTDSOnline** determina se Active Directory Domain Services sono online nel server specificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT DsIsNTDSOnline(
  _In_  LPCTSTR szServerName,
  _Out_ BOOL    *pfNTDSOnline
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*szServerName* \[ in\]
</dt> <dd>

Puntatore a una stringa con terminazione null che contiene il nome del server da testare. Le barre rovesciate precedenti sono facoltative. Il server deve essere lo stesso computer da cui viene chiamata la funzione. Il nome del server non può contenere caratteri di sottolineatura ( \_ ). Un esempio di nome di server è " \\ \\ Server1".

</dd> <dt>

*pfNTDSOnline* \[ out\]
</dt> <dd>

Puntatore al valore **bool** che riceve il risultato. Riceve **true** se il servizio directory è online o **false** se il servizio directory è offline.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **\_ OK** se la funzione ha esito positivo o un codice di errore. Nell'elenco seguente sono elencati i possibili codici di errore.

<dl> <dt>

**ERRORE di \_ accesso \_ negato**
</dt> <dd>

Il chiamante non dispone dei privilegi di accesso appropriati per chiamare questa funzione. La funzione [**DsSetAuthIdentity**](dssetauthidentity.md) può essere utilizzata per impostare le credenziali da utilizzare per le funzioni di backup e ripristino.

</dd> <dt>

**hrCouldNotConnect**
</dt> <dd>

Il server in *szServerName* non è stato trovato, non è un controller di dominio oppure *szServerName* non è formattato correttamente. Questo valore è definito in ntdsbmsg. h.

</dd> <dt>

**\_binding RPC S \_ non valido \_**
</dt> <dd>

La funzione [**DsIsNTDSOnline**](dsisntdsonline.md) viene chiamata in modalità remota o il server in *szServerName* non è un controller di dominio.

</dd> </dl>

## <a name="remarks"></a>Commenti

Chiamare questa funzione prima di chiamare una delle funzioni di backup o ripristino della directory. Per eseguire un backup, la directory deve essere online. Per eseguire un ripristino è necessario che la directory sia offline.

Questa funzione può essere chiamata solo da un controller di dominio che è anche il server di destinazione specificato in *szServerName*. Questa funzione non può essere chiamata in modalità remota.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Ntdsbcli. h</dt> </dl>   |
| Libreria<br/>                  | <dl> <dt>Ntdsbcli. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ntdsbcli.dll</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **DsIsNTDSOnlineW** (Unicode) e **DsIsNTDSOnlineA** (ANSI)<br/>                 |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**DsSetAuthIdentity**](dssetauthidentity.md)
</dt> <dt>

[Funzioni di backup della directory](directory-backup-functions.md)
</dt> <dt>

[Backup e ripristino di un server di Active Directory](backing-up-and-restoring-an-active-directory-server.md)
</dt> </dl>

 

