---
title: Metodo IDeviceBroker OpenDeviceFromInterfacePath
description: Tenta di aprire un'istanza dell'interfaccia del dispositivo per conto di un client. IID 8604b268-34A6-4b1A-A59F-CDBD8379FD98.
ms.assetid: 5ADDB994-3AAB-49B2-8B83-F71883AFD854
keywords:
- API broker Access Device Method OpenDeviceFromInterfacePath
- API gestore di accesso ai dispositivi del metodo OpenDeviceFromInterfacePath, interfaccia IDeviceBroker
- API del broker di accesso ai dispositivi dell'interfaccia IDeviceBroker, metodo OpenDeviceFromInterfacePath
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
ms.openlocfilehash: 5363600455ee1ba5c1c86cb12690afd242f68118
ms.sourcegitcommit: 01a4383738056cf3de4f45f36d98ef73d4dc694d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/11/2020
ms.locfileid: "104398522"
---
# <a name="idevicebrokeropendevicefrominterfacepath-method"></a>Metodo IDeviceBroker:: OpenDeviceFromInterfacePath

> [!Important]  
> Queste interfacce non sono supportate e non devono essere usate. Usare invece le API nella Guida di riferimento per la [programmazione di API di accesso ai dispositivi](device-access-api-c---programming-reference.md) .

Tenta di aprire un'istanza dell'interfaccia del dispositivo per conto di un client. IID = 8604b268-34A6-4b1A-A59F-CDBD8379FD98.

## <a name="syntax"></a>Sintassi

```C++
HRESULT OpenDeviceFromInterfacePath(
  [in]  PCWSTR pszDeviceInterfacePath,
  [in]  DWORD  desiredAccess,
  [in]  DWORD  shareMode,
  [in]  DWORD  flagsAndAttributes,
  [out] Handle *phDevice
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*pszDeviceInterfacePath* \[ in\]
</dt> <dd>

Istanza dell'interfaccia del dispositivo da aprire.

</dd> <dt>

*desiredAccess* \[ in\]
</dt> <dd>

Accesso desiderato da passare a Open.

</dd> <dt>

*shareMode* \[ in\]
</dt> <dd>

Modalità di condivisione da passare a Open.

</dd> <dt>

*flagsAndAttributes* \[ in\]
</dt> <dd>

Flag e attributi da passare a Open.

</dd> <dt>

*\* phDevice* \[\]
</dt> <dd>

Handle risultante se l'apertura è stata completata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questa funzione ha esito positivo, restituisce S_OK. In caso contrario, restituisce un codice di errore HRESULT.
