---
description: 'Libera gli identificatori di Plug and Play (PnP) recuperati dai metodi IPortableDeviceManager:: GetDevices o IPortableDeviceServiceManager:: GetDeviceServices.'
ms.assetid: b86f7733-81a3-4b60-bb7c-840c75f8d03f
title: Funzione FreePortableDevicePnPIDs (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FreePortableDevicePnPIDs
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 58bb5fa33007ed0e167226edf7078d08c2e5c3de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232703"
---
# <a name="freeportabledevicepnpids-function"></a>FreePortableDevicePnPIDs (funzione)

La funzione helper **FreePortableDevicePnPIDs** libera gli identificatori plug and Play (PNP) recuperati dai metodi [**IPortableDeviceManager:: GetDevices**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicemanager-getdevices) o [**IPortableDeviceServiceManager:: GetDeviceServices**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemanager-getdeviceservices) .

## <a name="syntax"></a>Sintassi


```C++
void FreePortableDevicePnPIDs(
   LPWSTR *pPnPIDs,
   DWORD  cPnPIDs
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pPnPIDs* 
</dt> <dd>

Matrice di identificatori di Plug and Play (PnP) da liberare.

</dd> <dt>

*cPnPIDs* 
</dt> <dd>

Il numero di identificatori nella matrice specificata dal parametro *pPnPIDs* .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

L'applicazione è responsabile di liberare la matrice di puntatori che alloca.

## <a name="examples"></a>Esempio


```C++
// Allocate an array of LPWSTR pointers.
    LPWSTR* pPnpDeviceIDs = new LPWSTR[cPnpDeviceIDs];
if (pPnpDeviceIDs != NULL)
{
    hr = pPortableDeviceManager->;GetDevices(pPnpDeviceIDs, &cPnpDeviceIDs);
    if (SUCCEEDED(hr))
    {
        // Free all returned PnPDeviceID strings allocated by IPortableDeviceManager::GetDevices.
     FreePortableDevicePnPIDs(pPnpDeviceIDs, cPnpDeviceIDs);
     // Application is responsible for deleting the array of LPWSTR pointers.
     delete [] pPnpDeviceIDs;
     pPnpDeviceIDs = NULL;      
 }
} 
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App desktop di Windows 7 \[ \| UWP\]<br/>                                           |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                   |
| Intestazione<br/>                   | <dl> <dt>PortableDevice. h</dt> </dl> |



 

 




