---
description: Installa un nuovo dispositivo. All'utente viene richiesto di selezionare il dispositivo.
ms.assetid: 9bdee82c-1d0a-41ea-8b42-7ad96ac37663
title: InstallNewDevice (funzione)
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
ms.openlocfilehash: 76a458ae071c61b9f1030aad535c4d4c6a31078c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127290"
---
# <a name="installnewdevice-function"></a>InstallNewDevice (funzione)

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

*hwndParent* \[ in\]
</dt> <dd>

Handle per la finestra di primo livello da utilizzare per qualsiasi interfaccia utente richiesta.

</dd> <dt>

*ClassGuid* \[ in\]
</dt> <dd>

Puntatore a un **GUID** di classe. Questo parametro è facoltativo. Se questo parametro è **null**, l'utente inizia dalla pagina scelta del rilevamento. Se questo parametro è **GUID \_ null** o **GUID \_ devclass \_ Unknown**, l'utente inizia dalla pagina di selezione della classe.

</dd> <dt>

*preavvio* \[ out\]
</dt> <dd>

Puntatore a una variabile che riceve lo stato di riavvio. Questo parametro può essere **di \_ NEEDRESTART** o **di \_ NEEDREBOOT**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è diverso da zero.

Se la funzione ha esito negativo, il valore restituito è zero. Per informazioni dettagliate sull'errore, chiamare [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Osservazioni

A questa funzione non è associata alcuna libreria di importazione. È necessario utilizzare le funzioni [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) per collegare dinamicamente a NewDev.dll.

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

 

