---
title: Funzione DsSetAuthIdentity (ntdsbcli. h)
description: Imposta il contesto di sicurezza in cui vengono chiamate le API di backup della directory.
ms.assetid: bfa2f847-6fe3-4f9b-bafa-acf6a7c861d9
ms.tgt_platform: multiple
keywords:
- Active Directory funzione DsSetAuthIdentity
topic_type:
- apiref
api_name:
- DsSetAuthIdentity
- DsSetAuthIdentityA
- DsSetAuthIdentityW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40d973d5f818b4bd81278a1466487ae89ebf888f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477344"
---
# <a name="dssetauthidentity-function"></a>DsSetAuthIdentity (funzione)

\[Questa funzione è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile. A partire da Windows Vista, usare invece [servizio Copia Shadow del volume (VSS)](../vss/volume-shadow-copy-service-overview.md) .\]

La funzione **DsSetAuthIdentity** imposta il contesto di sicurezza in cui vengono chiamate le API di backup della directory.

## <a name="syntax"></a>Sintassi


```C++
HRESULT DsSetAuthIdentity(
  _In_ LPCTSTR szUserName,
  _In_ LPCTSTR szDomainName,
  _In_ LPCTSTR szPassword
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*szUserName* \[ in\]
</dt> <dd>

Stringa con terminazione null che specifica il nome utente.

</dd> <dt>

*szDomainName* \[ in\]
</dt> <dd>

Stringa con terminazione null che specifica il nome del dominio a cui appartiene l'utente.

</dd> <dt>

*szPassword* \[ in\]
</dt> <dd>

Stringa con terminazione null che specifica la password dell'utente nel dominio specificato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se l'operazione riesce, restituisce un codice di esito positivo **HRESULT** standard; in caso contrario, viene restituito un codice di errore.

## <a name="remarks"></a>Commenti

Se **DsSetAuthIdentity** non viene chiamato, viene utilizzato il contesto di sicurezza del processo corrente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Ntdsbcli. h</dt> </dl>   |
| Libreria<br/>                  | <dl> <dt>Ntdsbcli. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ntdsbcli.dll</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **DsSetAuthIdentityW** (Unicode) e **DsSetAuthIdentityA** (ANSI)<br/>           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Backup e ripristino di un server di Active Directory](backing-up-and-restoring-an-active-directory-server.md)
</dt> <dt>

[Funzioni di backup della directory](directory-backup-functions.md)
</dt> </dl>

 

