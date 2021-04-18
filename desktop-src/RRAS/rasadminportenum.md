---
title: Funzione RasAdminPortEnum (rassapi. h)
description: La funzione RasAdminPortEnum enumera tutte le porte nel server RAS specificato. Per ogni porta sul server, la funzione restituisce la struttura della \_ porta RAS \_ 0 che contiene le informazioni sulla porta.
ms.assetid: ad23727c-8f54-4b10-9bc7-1425ac22bc88
keywords:
- RAS funzione RasAdminPortEnum
topic_type:
- apiref
api_name:
- RasAdminPortEnum
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5e4841627ce5df3feee3f885b399a070388ed55
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327901"
---
# <a name="rasadminportenum-function"></a>RasAdminPortEnum (funzione)

\[Questa funzione viene fornita solo per compatibilità con le versioni precedenti di Windows NT Server 4,0. Restituisce la \_ chiamata \_ di errore non \_ implementata in Windows Server 2003. Le applicazioni devono utilizzare la funzione [**MprAdminPortEnum**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportenum) .\]

La funzione **RasAdminPortEnum** enumera tutte le porte nel server RAS specificato. Per ogni porta sul server, la funzione restituisce la struttura [**della \_ porta RAS \_ 0**](ras-port-0-str.md) che contiene le informazioni sulla porta.

## <a name="syntax"></a>Sintassi


```C++
DWORD RasAdminPortEnum(
  _In_  const WCHAR       *lpszServer,
  _Out_       PRAS_PORT_0 *ppRasPort0,
  _Out_       WORD        *pcEntriesRead
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lpszServer* \[ in\]
</dt> <dd>

Puntatore a una stringa Unicode con terminazione null che specifica il nome del server RAS. Specificare il nome con i \\ \\ caratteri "" iniziali nel formato: \\ \\ *ServerName*.

</dd> <dt>

*ppRasPort0* \[ out\]
</dt> <dd>

Puntatore a una variabile che riceve un puntatore a un buffer che contiene una matrice di strutture della [**\_ porta RAS \_ 0**](ras-port-0-str.md) . Quando l'applicazione ha terminato con la memoria, liberarla chiamando la funzione [**RasAdminFreeBuffer**](rasadminfreebuffer.md) .

</dd> <dt>

*pcEntriesRead* \[ out\]
</dt> <dd>

Puntatore a una variabile a 16 bit che riceve il numero totale di strutture [**RAS della \_ porta \_ 0**](/windows/desktop/api/Mprapi/ns-mprapi-ras_port_0) restituite nella matrice *ppRasPort0* .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è ERROR \_ Success.

Se la funzione ha esito negativo, il valore restituito può essere il codice di errore seguente.



| Valore                                                                                             | Significato                                                                                                                                     |
|---------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_ITEMNOTFOUND Nerr**</dt> </dl> | Non è stato possibile enumerare le porte. Questo potrebbe essere dovuto al fatto che tutte le porte configurate nel server sono attualmente in uso per la connessione.<br/> |



 

Non sono disponibili informazioni estese sull'errore per questa funzione. non chiamare [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

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

[**\_Porta RAS \_ 0**](ras-port-0-str.md)
</dt> <dt>

[**RasAdminFreeBuffer**](rasadminfreebuffer.md)
</dt> </dl>

 

