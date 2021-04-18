---
title: Funzione RasAdminFreeBuffer (rassapi. h)
description: La funzione RasAdminFreeBuffer libera la memoria allocata da RAS per conto del chiamante.
ms.assetid: 6dfbba22-3af1-4771-8c22-506996f30c6b
keywords:
- RAS funzione RasAdminFreeBuffer
topic_type:
- apiref
api_name:
- RasAdminFreeBuffer
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1bf86a3005a2b865b2096eddc5ffa9c0c33f848a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333973"
---
# <a name="rasadminfreebuffer-function"></a>RasAdminFreeBuffer (funzione)

\[Questa funzione viene fornita solo per compatibilità con le versioni precedenti di Windows NT Server 4,0. Restituisce la \_ chiamata \_ di errore non \_ implementata in Windows Server 2003. Le applicazioni devono utilizzare la funzione [**MprAdminBufferFree**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminbufferfree) .\]

La funzione **RasAdminFreeBuffer** libera la memoria allocata da RAS per conto del chiamante.

## <a name="syntax"></a>Sintassi


```C++
DWORD RasAdminFreeBuffer(
  _In_ PVOID Pointer
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Puntatore* \[ in\]
</dt> <dd>

Puntatore al buffer da liberare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è ERROR \_ Success.

Se la funzione ha esito negativo, il valore restituito può essere il codice di errore seguente.



| Valore                                                                                                    | Significato                                        |
|----------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**ERRORE \_ parametro non valido \_**</dt> </dl> | Il parametro del *puntatore* non è valido.<br/> |



 

Non sono disponibili informazioni estese sull'errore per questa funzione. non chiamare [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Commenti

Utilizzare la funzione **RasAdminFreeBuffer** per liberare i buffer allocati dalle funzioni [**RasAdminPortEnum**](rasadminportenum.md) e [**RasAdminPortGetInfo**](rasadminportgetinfo.md) .

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

[**RasAdminPortEnum**](rasadminportenum.md)
</dt> <dt>

[**RasAdminPortGetInfo**](rasadminportgetinfo.md)
</dt> </dl>

 

