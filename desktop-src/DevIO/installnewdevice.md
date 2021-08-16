---
description: Installa un nuovo dispositivo. All'utente viene richiesto di selezionare il dispositivo.
ms.assetid: 9bdee82c-1d0a-41ea-8b42-7ad96ac37663
title: Funzione InstallNewDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InstallNewDevice
api_type:
- DllExport
api_location:
- NewDev.dll
ms.openlocfilehash: cb12e87ceee4812ffc8c0e39d961ce631e26c4ab8ca7ae555785c8ad8381ca01
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118405308"
---
# <a name="installnewdevice-function"></a>Funzione InstallNewDevice

Installa un nuovo dispositivo. All'utente viene richiesto di selezionare il dispositivo.

## <a name="syntax"></a>Sintassi


```C++
BOOL WINAPI InstallNewDevice(
  _In_  HWND   hwndParent,
  _In_  LPGUID ClassGuid,
  _Out_ PDWORD pReboot
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hwndParent* \[ Pollici\]
</dt> <dd>

Handle per la finestra di primo livello da usare per qualsiasi interfaccia utente richiesta.

</dd> <dt>

*ClassGuid* \[ Pollici\]
</dt> <dd>

Puntatore a un **GUID di classe.** Questo parametro è facoltativo. Se questo parametro è **NULL,** l'utente inizia dalla pagina di scelta del rilevamento. Se questo parametro è **GUID \_ NULL** o **GUID \_ DEVCLASS \_ UNKNOWN,** l'utente inizia dalla pagina di selezione della classe.

</dd> <dt>

*pReboot* \[ Cambio\]
</dt> <dd>

Puntatore a una variabile che riceve lo stato di riavvio. Questo parametro può essere **DI \_ NEEDRESTART** o **DI \_ NEEDREBOOT.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è diverso da zero.

Se la funzione ha esito negativo, il valore restituito è zero. Per informazioni dettagliate sull'errore, chiamare [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Osservazioni

A questa funzione non è associata alcuna libreria di importazione. È necessario usare le [**funzioni LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) per collegarsi dinamicamente NewDev.dll.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP<br/>                                                                 |
| Server minimo supportato<br/> | Windows Server 2003<br/>                                                        |
| DLL<br/>                      | <dl> <dt>NewDev.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni di gestione dei dispositivi](device-management-functions.md)
</dt> </dl>

 

