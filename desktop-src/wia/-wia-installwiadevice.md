---
description: La funzione InstallWiaDevice installa un Windows di acquisizione di immagini (WIA) come dispositivo enumerato nella radice. Potrebbe essere visualizzato un avviso di sicurezza se un file o un coinstallatore di installazione non è firmato digitalmente e considerato attendibile.
ms.assetid: c7de27f5-5994-4fce-a6ec-6e7cfae2e591
title: Funzione InstallWiaDevice (Wia.h)
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
ms.openlocfilehash: 10006e234c9a76054a77fb64f89a31d9a21e394066bcc98813912bad9f804e1e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965840"
---
# <a name="installwiadevice-function"></a>Funzione InstallWiaDevice

La **funzione InstallWiaDevice** installa un Windows di acquisizione di immagini (WIA) come dispositivo enumerato nella radice. Potrebbe essere visualizzato un avviso di sicurezza se un file o un coinstallatore di installazione non è firmato digitalmente e considerato attendibile.

## <a name="syntax"></a>Sintassi


```C++
DWORD WINAPI InstallWiaDevice(
  _In_ PWIADEVICEINSTALL *pWiaDeviceInstall
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pWiaDeviceInstall* \[ Pollici\]
</dt> <dd>

Tipo: **PWIADEVICEINSTALL \***

Puntatore a una struttura WIADEVICEINSTALL. Il *membro szFriendlyName* della struttura deve essere impostato sul valore friendlyName effettivo del dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **DWORD**

Se la funzione ha esito positivo, il valore restituito è ERROR \_ SUCCESS.

Se la funzione ha esito negativo, restituisce un codice di errore Win32.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                         |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                   |
| Intestazione<br/>                   | <dl> <dt>Wia.h</dt> </dl>       |
| Libreria<br/>                  | <dl> <dt>Wiaguid.lib</dt> </dl> |



 

 




