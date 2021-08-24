---
title: Funzione RasAdminPortGetInfo (Rassapi.h)
description: La funzione RasAdminPortGetInfo recupera informazioni su una porta specificata in un server specificato.
ms.assetid: 22837685-62a4-4e55-b88f-11019d5d4154
keywords:
- RasAdminPortGetInfo (funzione RAS)
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
ms.openlocfilehash: e633b663e9c4b35810585a2ac738c79ae2d39be06d7b91be0df75fd0455a5213
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120028511"
---
# <a name="rasadminportgetinfo-function"></a>Funzione RasAdminPortGetInfo

\[Questa funzione viene fornita solo per la compatibilità con Windows NT Server 4.0. Restituisce ERROR \_ CALL NOT IMPLEMENTED in Windows Server \_ \_ 2003. Le applicazioni devono usare [**la funzione MprAdminPortGetInfo.**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportgetinfo)\]

La **funzione RasAdminPortGetInfo** recupera informazioni su una porta specificata in un server specificato.

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

*lpszServer* \[ Pollici\]
</dt> <dd>

Puntatore a una stringa Unicode con terminazione Null che specifica il nome del server RAS. Specificare il nome con caratteri \\ \\ " " iniziali, nel formato: \\ \\ *nomeserver*.

</dd> <dt>

*lpszPort* \[ Pollici\]
</dt> <dd>

Puntatore a una stringa Unicode con terminazione Null che specifica il nome della porta nel server.

</dd> <dt>

*pRasPort1* \[ Cambio\]
</dt> <dd>

Puntatore alla [**struttura RAS \_ PORT \_ 1**](ras-port-1-str.md) compilata dalla funzione con informazioni sullo stato della porta.

</dd> <dt>

*pRasStats* \[ Cambio\]
</dt> <dd>

Puntatore alla [**struttura RAS \_ PORT \_ STATISTICS**](ras-port-statistics-str.md) compilata dalla funzione con statistiche sulla porta.

</dd> <dt>

*ppRasParams* \[ Cambio\]
</dt> <dd>

Puntatore a una variabile puntatore che riceve l'indirizzo di una matrice di [**strutture \_ PARAMETERS RAS.**](ras-parameters-str.md) Ogni struttura contiene il nome di una chiave specifica del supporto, ad esempio MAXCONNECTBPS, e il relativo valore associato. Al termine dell'applicazione, liberare la memoria chiamando la [**funzione RasAdminFreeBuffer.**](rasadminfreebuffer.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è ERROR \_ SUCCESS.

Se la funzione ha esito negativo, il valore restituito può essere uno dei codici di errore seguenti.



| Valore                                                                                                     | Significato                                                                          |
|-----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <dt>**ERRORE \_ DEV \_ \_ INESISTENTE**</dt> </dl>     | La porta specificata non è valida.<br/>                                        |
| <dl> <dt>**MEMORIA \_ INSUFFICIENTE \_ PER \_ L'ERRORE**</dt> </dl> | Memoria insufficiente per allocare un buffer per *la matrice ppRasParams.*<br/> |



 

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

[**PARAMETRI \_ RAS**](ras-parameters-str.md)
</dt> <dt>

[**PORTA \_ RAS \_ 1**](ras-port-1-str.md)
</dt> <dt>

[**STATISTICHE \_ PORTA \_ RAS**](ras-port-statistics-str.md)
</dt> <dt>

[**RasAdminFreeBuffer**](rasadminfreebuffer.md)
</dt> </dl>

 

