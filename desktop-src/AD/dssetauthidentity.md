---
title: Funzione DsSetAuthIdentity (Ntdsbcli.h)
description: Imposta il contesto di sicurezza in cui vengono chiamate le API di backup della directory.
ms.assetid: bfa2f847-6fe3-4f9b-bafa-acf6a7c861d9
ms.tgt_platform: multiple
keywords:
- Funzione DsSetAuthIdentity active Directory
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
ms.openlocfilehash: a8e4f990d1fa0c6a6a22b0068ea207be61b4aece441977b976f32f82b7b75c8b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118695506"
---
# <a name="dssetauthidentity-function"></a>Funzione DsSetAuthIdentity

\[Questa funzione è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile. A partire da Windows Vista, [usare Servizio Copia Shadow del volume (VSS).](../vss/volume-shadow-copy-service-overview.md)\]

La **funzione DsSetAuthIdentity** imposta il contesto di sicurezza in cui vengono chiamate le API di backup della directory.

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

*szUserName* \[ Pollici\]
</dt> <dd>

Stringa con terminazione Null che specifica il nome utente.

</dd> <dt>

*szDomainName* \[ Pollici\]
</dt> <dd>

Stringa con terminazione Null che specifica il nome del dominio a cui appartiene l'utente.

</dd> <dt>

*szPassword* \[ Pollici\]
</dt> <dd>

Stringa con terminazione Null che specifica la password dell'utente nel dominio specificato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se ha esito positivo, restituisce un **codice di esito positivo HRESULT** standard. In caso contrario, viene restituito un codice di errore.

## <a name="remarks"></a>Commenti

Se **DsSetAuthIdentity** non viene chiamato, si presuppone il contesto di sicurezza del processo corrente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Ntdsbcli.h</dt> </dl>   |
| Libreria<br/>                  | <dl> <dt>Ntdsbcli.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ntdsbcli.dll</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **DsSetAuthIdentityW** (Unicode) e **DsSetAuthIdentityA** (ANSI)<br/>           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Backup e ripristino di un server Active Directory](backing-up-and-restoring-an-active-directory-server.md)
</dt> <dt>

[Funzioni di backup della directory](directory-backup-functions.md)
</dt> </dl>

 

