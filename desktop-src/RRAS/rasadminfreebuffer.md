---
title: Funzione RasAdminFreeBuffer (Rassapi.h)
description: La funzione RasAdminFreeBuffer libera la memoria allocata da RAS per conto del chiamante.
ms.assetid: 6dfbba22-3af1-4771-8c22-506996f30c6b
keywords:
- Funzione RasAdminFreeBuffer RAS
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
ms.openlocfilehash: 9550c072840fabf5d862e32f3bbdc6c26d3b32faf9cf6bf6dcfeae1be400e0a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117789096"
---
# <a name="rasadminfreebuffer-function"></a>Funzione RasAdminFreeBuffer

\[Questa funzione viene fornita solo per compatibilità con le versioni precedenti Windows NT Server 4.0. Restituisce ERROR \_ CALL NOT IMPLEMENTED in Windows Server \_ \_ 2003. Le applicazioni devono usare [**la funzione MprAdminBufferFree.**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminbufferfree)\]

La **funzione RasAdminFreeBuffer** libera la memoria allocata da RAS per conto del chiamante.

## <a name="syntax"></a>Sintassi


```C++
DWORD RasAdminFreeBuffer(
  _In_ PVOID Pointer
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Puntatore* \[ Pollici\]
</dt> <dd>

Puntatore al buffer da liberare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è ERROR \_ SUCCESS.

Se la funzione ha esito negativo, il valore restituito può essere il codice di errore seguente.



| Valore                                                                                                    | Significato                                        |
|----------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**ERRORE \_ PARAMETRO NON \_ VALIDO**</dt> </dl> | Il *parametro Pointer* non è valido.<br/> |



 

Non sono disponibili informazioni estese sugli errori per questa funzione. non chiamare [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Commenti

Usare la **funzione RasAdminFreeBuffer** per liberare i buffer allocati dalle funzioni [**RasAdminPortEnum**](rasadminportenum.md) [**e RasAdminPortGetInfo.**](rasadminportgetinfo.md)

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

[**RasAdminPortEnum**](rasadminportenum.md)
</dt> <dt>

[**RasAdminPortGetInfo**](rasadminportgetinfo.md)
</dt> </dl>

 

