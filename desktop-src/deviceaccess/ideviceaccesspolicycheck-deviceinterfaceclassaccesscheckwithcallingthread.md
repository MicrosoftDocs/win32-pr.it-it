---
title: Metodo IDeviceAccessPolicyCheck DeviceInterfaceClassAccessCheckWithCallingThread
description: Questa API determinerà se il token per il contesto corrente ha accesso alla classe di interfaccia del dispositivo specificata. IID 7D276FF2-CE90-4275-A2A8-9A48B10D3E0B.
ms.assetid: D7BFE1F3-4876-4BAB-A32D-46DB533140BB
keywords:
- API broker Access Device Method DeviceInterfaceClassAccessCheckWithCallingThread
- API gestore di accesso ai dispositivi del metodo DeviceInterfaceClassAccessCheckWithCallingThread, interfaccia IDeviceAccessPolicyCheck
- API del broker di accesso ai dispositivi dell'interfaccia IDeviceAccessPolicyCheck, metodo DeviceInterfaceClassAccessCheckWithCallingThread
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
ms.openlocfilehash: 44eb44a83175cf8f735abfeb8cfec4de83f46bd2
ms.sourcegitcommit: 01a4383738056cf3de4f45f36d98ef73d4dc694d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/11/2020
ms.locfileid: "106299369"
---
# <a name="ideviceaccesspolicycheckdeviceinterfaceclassaccesscheckwithcallingthread-method"></a>IDeviceAccessPolicyCheck::D Metodo eviceInterfaceClassAccessCheckWithCallingThread

> [!Important]  
> Queste interfacce non sono supportate e non devono essere usate. Usare invece le API nella Guida di riferimento per la [programmazione di API di accesso ai dispositivi](device-access-api-c---programming-reference.md) .

Questa API determinerà se il token per il contesto corrente ha accesso alla classe di interfaccia del dispositivo specificata. IID = 7D276FF2-CE90-4275-A2A8-9A48B10D3E0B.

## <a name="syntax"></a>Sintassi

```C++
HRESULT DeviceInterfaceClassAccessCheckWithCallingThread(
  [in] PCWSTR pszDeviceInterfaceClassGuid,
  [in] DWORD  dwClientThreadId
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*pszDeviceInterfaceClassGuid* \[ in\]
</dt> <dd>

GUID della classe dell'interfaccia del dispositivo per cui è necessario controllare l'accesso.

</dd> <dt>

*dwClientThreadId* \[ in\]
</dt> <dd>

ID thread del client in cui deve essere visualizzata un'interfaccia utente associata, se necessario.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questa funzione ha esito positivo, restituisce S_OK. In caso contrario, restituisce un codice di errore HRESULT.
