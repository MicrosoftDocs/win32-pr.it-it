---
title: Metodo IDeviceAccessPolicyCheck DeviceInterfaceClassAccessCheckWithCallingThread
description: Questa API determinerà se il token per il contesto corrente ha accesso alla classe di interfaccia del dispositivo specificata. IID 7D276FF2-CE90-4275-A2A8-9A48B10D3E0B.
ms.assetid: D7BFE1F3-4876-4BAB-A32D-46DB533140BB
keywords:
- Metodo DeviceInterfaceClassAccessCheckWithCallingThread API device access broker
- Metodo DeviceInterfaceClassAccessCheckWithCallingThread API device access broker, interfaccia IDeviceAccessPolicyCheck
- Metodo DeviceInterfaceClassAccessCheckWithCallingThread dell'interfaccia IDeviceAccessPolicyCheck
topic_type:
- apiref
api_name:
- IDeviceAccessPolicyCheck.DeviceInterfaceClassAccessCheckWithCallingThread
api_type:
- COM
ms.topic: article
ms.date: 02/11/2020
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f279972c3b716f111fa37fc2dd01ef9184b2f804f07106f6b971358daf290c44
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119635351"
---
# <a name="ideviceaccesspolicycheckdeviceinterfaceclassaccesscheckwithcallingthread-method"></a>Metodo IDeviceAccessPolicyCheck::D eviceInterfaceClassAccessCheckWithCallingThread

> [!Important]  
> Queste interfacce non sono supportate e non devono essere usate. Usare invece le API nel API di accesso al dispositivo [di programmazione C++.](device-access-api-c---programming-reference.md)

Questa API determinerà se il token per il contesto corrente ha accesso alla classe di interfaccia del dispositivo specificata. IID = 7D276FF2-CE90-4275-A2A8-9A48B10D3E0B.

## <a name="syntax"></a>Sintassi

```C++
HRESULT DeviceInterfaceClassAccessCheckWithCallingThread(
  [in] PCWSTR pszDeviceInterfaceClassGuid,
  [in] DWORD  dwClientThreadId
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*pszDeviceInterfaceClassGuid* \[ Pollici\]
</dt> <dd>

GUID della classe di interfaccia del dispositivo per cui verificare l'accesso.

</dd> <dt>

*dwClientThreadId* \[ Pollici\]
</dt> <dd>

ID thread client in cui deve essere visualizzata qualsiasi interfaccia utente associata, se necessario.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questa funzione ha esito positivo, restituisce S_OK. In caso contrario, restituisce un codice di errore HRESULT.
