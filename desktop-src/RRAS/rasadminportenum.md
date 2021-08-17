---
title: Funzione RasAdminPortEnum (Rassapi.h)
description: La funzione RasAdminPortEnum enumera tutte le porte nel server RAS specificato. Per ogni porta nel server, la funzione restituisce la struttura RAS \_ PORT \_ 0 che contiene informazioni sulla porta.
ms.assetid: ad23727c-8f54-4b10-9bc7-1425ac22bc88
keywords:
- RasAdminPortEnum ( funzione RAS)
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
ms.openlocfilehash: 989b86cbf78a47a62c8d98799ac18adf987cbe623dc92e703537c54b54bf892a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117788873"
---
# <a name="rasadminportenum-function"></a>Funzione RasAdminPortEnum

\[Questa funzione viene fornita solo per la compatibilità con Windows NT Server 4.0. Restituisce ERROR \_ CALL NOT IMPLEMENTED in Windows Server \_ \_ 2003. Le applicazioni devono usare [**la funzione MprAdminPortEnum.**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportenum)\]

La **funzione RasAdminPortEnum** enumera tutte le porte nel server RAS specificato. Per ogni porta nel server, la funzione restituisce la [**struttura RAS \_ PORT \_ 0**](ras-port-0-str.md) che contiene informazioni sulla porta.

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

*lpszServer* \[ Pollici\]
</dt> <dd>

Puntatore a una stringa Unicode con terminazione Null che specifica il nome del server RAS. Specificare il nome con caratteri \\ \\ " " iniziali, nel formato: \\ \\ *nomeserver*.

</dd> <dt>

*ppRasPort0* \[ Cambio\]
</dt> <dd>

Puntatore a una variabile che riceve un puntatore a un buffer che contiene una matrice di [**strutture RAS \_ PORT \_ 0.**](ras-port-0-str.md) Al termine dell'applicazione, liberare la memoria chiamando la [**funzione RasAdminFreeBuffer.**](rasadminfreebuffer.md)

</dd> <dt>

*pcEntriesRead* \[ Cambio\]
</dt> <dd>

Puntatore a una variabile a 16 bit che riceve il numero totale di strutture [**RAS \_ PORT \_ 0**](/windows/desktop/api/Mprapi/ns-mprapi-ras_port_0) restituite nella matrice *ppRasPort0.*

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è ERROR \_ SUCCESS.

Se la funzione ha esito negativo, il valore restituito può essere il codice di errore seguente.



| Valore                                                                                             | Significato                                                                                                                                     |
|---------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**Elemento \_ NERRNotFound**</dt> </dl> | Impossibile enumerare le porte. Ciò potrebbe essere dovuto al fatto che tutte le porte configurate nel server sono attualmente in uso per la connessione remota.<br/> |



 

Non sono disponibili informazioni sugli errori estesi per questa funzione. non chiamare [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

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

[**PORTA \_ RAS \_ 0**](ras-port-0-str.md)
</dt> <dt>

[**RasAdminFreeBuffer**](rasadminfreebuffer.md)
</dt> </dl>

 

