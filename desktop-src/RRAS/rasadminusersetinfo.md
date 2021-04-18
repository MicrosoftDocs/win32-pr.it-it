---
title: Funzione RasAdminUserSetInfo (rassapi. h)
description: La funzione RasAdminUserSetInfo imposta le autorizzazioni RAS e il numero di telefono di chiamata per un utente specificato.
ms.assetid: 5b049dfd-ecc8-47e4-82cc-71a875752714
keywords:
- RAS funzione RasAdminUserSetInfo
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
ms.openlocfilehash: 16d35f62713a3f4669db191891d2fb6b1694cabe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328059"
---
# <a name="rasadminusersetinfo-function"></a>RasAdminUserSetInfo (funzione)

\[Questa funzione viene fornita solo per compatibilità con le versioni precedenti di Windows NT Server 4,0. Restituisce la \_ chiamata \_ di errore non \_ implementata in Windows Server 2003. Le applicazioni devono utilizzare la funzione [**MprAdminUserSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusersetinfo) .\]

La funzione **RasAdminUserSetInfo** imposta le autorizzazioni RAS e il numero di telefono di chiamata per un utente specificato.

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

*lpszUserAccountServer* \[ in\]
</dt> <dd>

Puntatore a una stringa Unicode con terminazione null che specifica il nome del controller di dominio primario o di backup con il database degli account utente. Utilizzare la funzione [**RasAdminGetUserAccountServer**](rasadmingetuseraccountserver.md) per ottenere il nome del server.

</dd> <dt>

*lpszUser* \[ in\]
</dt> <dd>

Puntatore a una stringa Unicode con terminazione null che specifica il nome dell'utente per il quale devono essere impostate le informazioni RAS.

</dd> <dt>

*pRasUser0* \[ in\]
</dt> <dd>

Puntatore alla struttura [**\_ dell'utente RAS \_ 0**](ras-user-0-str.md) che specifica i nuovi dati RAS per l'utente specificato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è ERROR \_ Success.

Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti codici di errore.



| Valore                                                                                                           | Descrizione                                                                                     |
|-----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>**ERRORE \_ dati non validi \_**</dt> </dl>             | Il buffer *pRasUser0* contiene dati non validi.<br/>                                        |
| <dl> <dt>**ERRORE \_ \_ numero di callback non valido \_**</dt> </dl> | Il numero di callback specificato nel buffer *pRasUser0* contiene caratteri non validi.<br/> |
| <dl> <dt>**Nerr \_ BufTooSmall**</dt> </dl>               | Memoria insufficiente per eseguire questa funzione.<br/>                                        |



 

Non sono disponibili informazioni estese sull'errore per questa funzione. non chiamare [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Commenti

Quando si impostano le autorizzazioni RAS per un utente, è necessario che il membro **bfPrivilege** della struttura [**RAS \_ User \_ 0**](ras-user-0-str.md) specifichi almeno uno dei flag di chiamata. Ad esempio, per impostare i privilegi di un utente per consentire i privilegi di connessione remota senza privilegi di callback, impostare **bfPrivilege** su RASPRIV \_ DialinPrivilege \| RASPRIV \_ NoCallback.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fine del supporto client<br/> | Windows 2000 Professional<br/>                                                   |
| Fine del supporto server<br/> | Windows 2000 Server<br/>                                                         |
| Intestazione<br/>                | <dl> <dt>Rassapi. h</dt> </dl>   |
| Libreria<br/>               | <dl> <dt>Rassapi. lib</dt> </dl> |
| DLL<br/>                   | <dl> <dt>Rassapi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Panoramica del servizio di accesso remoto (RAS)](about-remote-access-service.md)
</dt> <dt>

[Funzioni di amministrazione del server RAS](ras-server-administration-functions.md)
</dt> <dt>

[**\_Utente RAS \_ 0**](ras-user-0-str.md)
</dt> <dt>

[**RasAdminGetUserAccountServer**](rasadmingetuseraccountserver.md)
</dt> <dt>

[**RasAdminUserGetInfo**](rasadminusergetinfo.md)
</dt> </dl>

 

