---
title: Metodo IDeviceBroker OpenDeviceFromInterfacePath
description: Tenta di aprire un'istanza dell'interfaccia del dispositivo per conto di un client. IID 8604b268-34A6-4b1A-A59F-CDBD8379FD98.
ms.assetid: 5ADDB994-3AAB-49B2-8B83-F71883AFD854
keywords:
- Metodo OpenDeviceFromInterfacePath API gestore accesso dispositivo
- Metodo OpenDeviceFromInterfacePath API device access broker, interfaccia IDeviceBroker
- Interfaccia IDeviceBroker API Device Access Broker , metodo OpenDeviceFromInterfacePath
topic_type:
- apiref
api_name:
- IDeviceBroker.OpenDeviceFromInterfacePath
api_type:
- COM
ms.topic: article
ms.date: 02/11/2020
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4d9bd4e03b489a899e182c86207e11ae9ec0fb66cc6c917584d83dcc0aa97918
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119635331"
---
# <a name="idevicebrokeropendevicefrominterfacepath-method"></a>Metodo IDeviceBroker::OpenDeviceFromInterfacePath

> [!Important]  
> Queste interfacce non sono supportate e non devono essere usate. In alternativa, usare le API nella [API di accesso al dispositivo di programmazione C++.](device-access-api-c---programming-reference.md)

Tenta di aprire un'istanza dell'interfaccia del dispositivo per conto di un client. IID = 8604b268-34A6-4b1A-A59F-CDBD8379FD98.

## <a name="syntax"></a>Sintassi

```C++
HRESULT OpenDeviceFromInterfacePath(
  [in]  PCWSTR pszDeviceInterfacePath,
  [in]  DWORD  desiredAccess,
  [in]  DWORD  shareMode,
  [in]  DWORD  flagsAndAttributes,
  [out] Handle *phDevice
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*pszDeviceInterfacePath* \[ Pollici\]
</dt> <dd>

Istanza dell'interfaccia del dispositivo da aprire.

</dd> <dt>

*desiredAccess* \[ Pollici\]
</dt> <dd>

Accesso desiderato da passare all'apertura.

</dd> <dt>

*shareMode* \[ Pollici\]
</dt> <dd>

Modalità di condivisione da passare all'apertura.

</dd> <dt>

*flagsAndAttributes* \[ Pollici\]
</dt> <dd>

Flag e attributi da passare per l'apertura.

</dd> <dt>

*\* phDevice* \[ out\]
</dt> <dd>

Handle risultante se l'apertura ha avuto esito positivo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questa funzione ha esito positivo, restituisce S_OK. In caso contrario, restituisce un codice di errore HRESULT.
