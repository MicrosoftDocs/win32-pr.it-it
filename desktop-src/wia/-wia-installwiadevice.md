---
description: La funzione InstallWiaDevice installa un dispositivo Windows Image Acquisition (WIA) come dispositivo con enumerazione radice. È possibile che venga visualizzato un avviso di sicurezza se un file di installazione o un coinstallatore non è firmato digitalmente e considerato attendibile.
ms.assetid: c7de27f5-5994-4fce-a6ec-6e7cfae2e591
title: Funzione InstallWiaDevice (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InstallWiaDevice
api_type:
- LibDef
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 62060d538b4b51fe22e10df09093f1f7f8c26a1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752863"
---
# <a name="installwiadevice-function"></a>InstallWiaDevice (funzione)

La funzione **InstallWiaDevice** installa un dispositivo Windows Image Acquisition (WIA) come dispositivo con enumerazione radice. È possibile che venga visualizzato un avviso di sicurezza se un file di installazione o un coinstallatore non è firmato digitalmente e considerato attendibile.

## <a name="syntax"></a>Sintassi


```C++
DWORD WINAPI InstallWiaDevice(
  _In_ PWIADEVICEINSTALL *pWiaDeviceInstall
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pWiaDeviceInstall* \[ in\]
</dt> <dd>

Tipo: **PWIADEVICEINSTALL \** _

Puntatore a una struttura WIADEVICEINSTALL. Il membro _szFriendlyName * della struttura deve essere impostato sull'effettivo dispositivo FriendlyName.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **DWORD**

Se la funzione ha esito positivo, il valore restituito è ERROR \_ Success.

Se la funzione ha esito negativo, restituisce un codice di errore Win32.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                         |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                   |
| Intestazione<br/>                   | <dl> <dt>WIA. h</dt> </dl>       |
| Libreria<br/>                  | <dl> <dt>Wiaguid. lib</dt> </dl> |



 

 




