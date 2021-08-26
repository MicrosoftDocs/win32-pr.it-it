---
title: Funzione RasAdminUserSetInfo (Rassapi.h)
description: La funzione RasAdminUserSetInfo imposta le autorizzazioni RAS e il numero di telefono di chiamata per un utente specificato.
ms.assetid: 5b049dfd-ecc8-47e4-82cc-71a875752714
keywords:
- RasAdminUserSetInfo (funzione RAS)
topic_type:
- apiref
api_name:
- RasAdminUserSetInfo
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51bc4b56b9aa606892002fbef0eda8036c45442c06ce06b8561afba57620b7a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120028431"
---
# <a name="rasadminusersetinfo-function"></a>Funzione RasAdminUserSetInfo

\[Questa funzione viene fornita solo per la compatibilità con Windows NT Server 4.0. Restituisce ERROR \_ CALL NOT IMPLEMENTED in Windows Server \_ \_ 2003. Le applicazioni devono usare [**la funzione MprAdminUserSetInfo.**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusersetinfo)\]

La **funzione RasAdminUserSetInfo** imposta le autorizzazioni RAS e il numero di telefono di chiamata per un utente specificato.

## <a name="syntax"></a>Sintassi


```C++
DWORD RasAdminUserSetInfo(
  _In_ const WCHAR       *lpszUserAccountServer,
  _In_ const WCHAR       *lpszUser,
  _In_ const PRAS_USER_0 pRasUser0
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lpszUserAccountServer* \[ Pollici\]
</dt> <dd>

Puntatore a una stringa Unicode con terminazione Null che specifica il nome del controller di dominio primario o di backup con il database dell'account utente. Usare la [**funzione RasAdminGetUserAccountServer**](rasadmingetuseraccountserver.md) per ottenere il nome del server.

</dd> <dt>

*lpszUser* \[ Pollici\]
</dt> <dd>

Puntatore a una stringa Unicode con terminazione Null che specifica il nome dell'utente per cui devono essere impostate le informazioni RAS.

</dd> <dt>

*pRasUser0* \[ Pollici\]
</dt> <dd>

Puntatore alla [**struttura RAS \_ USER \_ 0**](ras-user-0-str.md) che specifica i nuovi dati RAS per l'utente specificato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è ERROR \_ SUCCESS.

Se la funzione ha esito negativo, il valore restituito può essere uno dei codici di errore seguenti.



| Valore                                                                                                           | Descrizione                                                                                     |
|-----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>**ERRORE \_ DATI NON \_ VALIDI**</dt> </dl>             | Il *buffer pRasUser0* contiene dati non validi.<br/>                                        |
| <dl> <dt>**ERRORE \_ NUMERO DI CALLBACK NON \_ \_ VALIDO**</dt> </dl> | Il numero di callback specificato nel buffer *pRasUser0* contiene caratteri non validi.<br/> |
| <dl> <dt>**NERR \_ BufTooSmall**</dt> </dl>               | Memoria insufficiente per eseguire questa funzione.<br/>                                        |



 

Non sono disponibili informazioni sugli errori estesi per questa funzione. non chiamare [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Commenti

Quando si impostano le autorizzazioni RAS per un utente, il membro **bfPrivilege** della struttura [**RAS USER \_ \_ 0**](ras-user-0-str.md) deve specificare almeno uno dei flag di richiamo. Ad esempio, per impostare i privilegi di un utente per consentire i privilegi di accesso remoto ma nessun privilegio di richiamata, impostare **bfPrivilege** su RASPRIV \_ DialinPrivilege \| RASPRIV \_ NoCallback.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fine del supporto client<br/> | Windows 2000 Professional<br/>                                                   |
| Fine del supporto server<br/> | Windows 2000 Server<br/>                                                         |
| Intestazione<br/>                | <dl> <dt>Rassapi.h</dt> </dl>   |
| Libreria<br/>               | <dl> <dt>Rassapi.lib</dt> </dl> |
| DLL<br/>                   | <dl> <dt>Rassapi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Panoramica del servizio di accesso remoto (RAS)](about-remote-access-service.md)
</dt> <dt>

[Funzioni di amministrazione del server RAS](ras-server-administration-functions.md)
</dt> <dt>

[**UTENTE \_ RAS \_ 0**](ras-user-0-str.md)
</dt> <dt>

[**RasAdminGetUserAccountServer**](rasadmingetuseraccountserver.md)
</dt> <dt>

[**RasAdminUserGetInfo**](rasadminusergetinfo.md)
</dt> </dl>

 

