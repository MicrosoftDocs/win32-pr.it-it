---
title: Funzione DsIsNTDSOnline (Ntdsbcli.h)
description: Determina se Active Directory Domain Services sono online nel server specificato.
ms.assetid: 8f46e4d8-6d05-402c-a5b4-291fd2d6609b
ms.tgt_platform: multiple
keywords:
- Funzione DsIsNTDSOnline Active Directory
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
ms.openlocfilehash: 0bf65109b4c72e1d403ece18d82b189039d74d58043271e0f5bf317f5272f84d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118430023"
---
# <a name="dsisntdsonline-function"></a>Funzione DsIsNTDSOnline

\[Questa funzione è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile. A partire da Windows Vista, [usare Servizio Copia Shadow del volume (VSS).](../vss/volume-shadow-copy-service-overview.md)\]

La **funzione DsIsNTDSOnline** determina se Active Directory Domain Services online nel server specificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT DsIsNTDSOnline(
  _In_  LPCTSTR szServerName,
  _Out_ BOOL    *pfNTDSOnline
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*szServerName* \[ Pollici\]
</dt> <dd>

Puntatore a una stringa con terminazione Null contenente il nome del server da testare. Le barre rovesciate precedenti sono facoltative. Il server deve essere lo stesso computer da cui viene chiamata questa funzione. Il nome del server non può contenere caratteri di sottolineatura ( \_ ). Un esempio di nome server è \\ \\ "server1".

</dd> <dt>

*pfNTDSOnline* \[ Cambio\]
</dt> <dd>

Puntatore **al valore BOOL** che riceve il risultato. Riceve **TRUE se** il servizio directory è online o **FALSE** se il servizio directory è offline.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **S \_ OK se** la funzione ha esito positivo o un codice di errore in caso contrario. Nell'elenco seguente sono elencati i possibili codici di errore.

<dl> <dt>

**ERRORE \_ DI ACCESSO \_ NEGATO**
</dt> <dd>

Il chiamante non dispone dei privilegi di accesso adeguati per chiamare questa funzione. La [**funzione DsSetAuthIdentity**](dssetauthidentity.md) può essere usata per impostare le credenziali da usare per le funzioni di backup e ripristino.

</dd> <dt>

**hrCouldNotConnect**
</dt> <dd>

Impossibile trovare il server in *szServerName,* non è un controller di dominio o *szServerName* non è formattato correttamente. Questo valore è definito in Ntdsbmsg.h.

</dd> <dt>

**ASSOCIAZIONE \_ RPC S NON \_ \_ VALIDA**
</dt> <dd>

La [**funzione DsIsNTDSOnline**](dsisntdsonline.md) viene chiamata in modalità remota o il server in *szServerName* non è un controller di dominio.

</dd> </dl>

## <a name="remarks"></a>Commenti

Chiamare questa funzione prima di chiamare una delle funzioni di backup o ripristino della directory. Per eseguire un backup, la directory deve essere online. La directory deve essere offline per eseguire un ripristino.

Questa funzione può essere chiamata solo da un controller di dominio che è anche il server di destinazione specificato in *szServerName*. Questa funzione non può essere chiamata in modalità remota.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Ntdsbcli.h</dt> </dl>   |
| Libreria<br/>                  | <dl> <dt>Ntdsbcli.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ntdsbcli.dll</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **DsIsNTDSOnlineW** (Unicode) e **DsIsNTDSOnlineA** (ANSI)<br/>                 |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**DsSetAuthIdentity**](dssetauthidentity.md)
</dt> <dt>

[Funzioni di backup della directory](directory-backup-functions.md)
</dt> <dt>

[Backup e ripristino di un server Active Directory](backing-up-and-restoring-an-active-directory-server.md)
</dt> </dl>

 

