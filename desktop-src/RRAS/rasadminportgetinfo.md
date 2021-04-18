---
title: Funzione RasAdminPortGetInfo (rassapi. h)
description: La funzione RasAdminPortGetInfo recupera le informazioni su una porta specificata in un server specificato.
ms.assetid: 22837685-62a4-4e55-b88f-11019d5d4154
keywords:
- RAS funzione RasAdminPortGetInfo
topic_type:
- apiref
api_name:
- RasAdminPortGetInfo
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8d80c55b3182ec930732344cb7857f99c0dc411
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330765"
---
# <a name="rasadminportgetinfo-function"></a>RasAdminPortGetInfo (funzione)

\[Questa funzione viene fornita solo per compatibilità con le versioni precedenti di Windows NT Server 4,0. Restituisce la \_ chiamata \_ di errore non \_ implementata in Windows Server 2003. Le applicazioni devono utilizzare la funzione [**MprAdminPortGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportgetinfo) .\]

La funzione **RasAdminPortGetInfo** recupera le informazioni su una porta specificata in un server specificato.

## <a name="syntax"></a>Sintassi


```C++
DWORD RasAdminPortGetInfo(
  _In_  const WCHAR               *lpszServer,
  _In_  const WCHAR               *lpszPort,
  _Out_       RAS_PORT_1          *pRasPort1,
  _Out_       RAS_PORT_STATISTICS *pRasStats,
  _Out_       RAS_PARAMETERS      **ppRasParams
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lpszServer* \[ in\]
</dt> <dd>

Puntatore a una stringa Unicode con terminazione null che specifica il nome del server RAS. Specificare il nome con i \\ \\ caratteri "" iniziali nel formato: \\ \\ *ServerName*.

</dd> <dt>

*lpszPort* \[ in\]
</dt> <dd>

Puntatore a una stringa Unicode con terminazione null che specifica il nome della porta nel server.

</dd> <dt>

*pRasPort1* \[ out\]
</dt> <dd>

Puntatore alla struttura [**della \_ porta RAS \_ 1**](ras-port-1-str.md) che la funzione compila con informazioni sullo stato della porta.

</dd> <dt>

*pRasStats* \[ out\]
</dt> <dd>

Puntatore alla struttura [**delle \_ \_ statistiche della porta RAS**](ras-port-statistics-str.md) che la funzione compila con le statistiche sulla porta.

</dd> <dt>

*ppRasParams* \[ out\]
</dt> <dd>

Puntatore a una variabile puntatore che riceve l'indirizzo di una matrice di strutture di [**\_ parametri RAS**](ras-parameters-str.md) . Ogni struttura contiene il nome di una chiave specifica del supporto, ad esempio MAXCONNECTBPS, e il relativo valore associato. Al termine dell'applicazione, liberare la memoria chiamando la funzione [**RasAdminFreeBuffer**](rasadminfreebuffer.md) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è ERROR \_ Success.

Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti codici di errore.



| Valore                                                                                                     | Significato                                                                          |
|-----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <dt>**ERRORE \_ dev \_ non \_ esiste**</dt> </dl>     | La porta specificata non è valida.<br/>                                        |
| <dl> <dt>**ERRORE \_ di \_ memoria insufficiente \_**</dt> </dl> | Memoria insufficiente per allocare un buffer per la matrice *ppRasParams* .<br/> |



 

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

[**\_parametri RAS**](ras-parameters-str.md)
</dt> <dt>

[**\_Porta RAS \_ 1**](ras-port-1-str.md)
</dt> <dt>

[**\_statistiche porta \_ RAS**](ras-port-statistics-str.md)
</dt> <dt>

[**RasAdminFreeBuffer**](rasadminfreebuffer.md)
</dt> </dl>

 

