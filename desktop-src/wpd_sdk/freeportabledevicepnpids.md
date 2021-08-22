---
description: Libera gli identificatori Plug and Play (PnP) recuperati dai metodi IPortableDeviceManager::GetDevices o IPortableDeviceServiceManager::GetDeviceServices.
ms.assetid: b86f7733-81a3-4b60-bb7c-840c75f8d03f
title: Funzione FreePortableDevicePnPIDs (PortableDevice.h)
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
ms.openlocfilehash: 150796912d2796a2697d3c088963c20e1523288f5a1301e9467a6859845db68c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119590316"
---
# <a name="freeportabledevicepnpids-function"></a>Funzione FreePortableDevicePnPIDs

La funzione helper **FreePortableDevicePnPIDs** libera gli identificatori Plug and Play (PnP) recuperati dai metodi [**IPortableDeviceManager::GetDevices**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicemanager-getdevices) o [**IPortableDeviceServiceManager::GetDeviceServices.**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemanager-getdeviceservices)

## <a name="syntax"></a>Sintassi


```C++
void FreePortableDevicePnPIDs(
   LPWSTR *pPnPIDs,
   DWORD  cPnPIDs
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pPnPID* 
</dt> <dd>

Matrice di Plug and Play (PnP) da liberare.

</dd> <dt>

*cPnPID* 
</dt> <dd>

Numero di identificatori nella matrice specificata dal *parametro pPnPIDs.*

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

L'applicazione è responsabile della liberatura della matrice di puntatori allocata.

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
| Client minimo supportato<br/> | Windows 7 \[ app desktop app \| UWP\]<br/>                                           |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                   |
| Intestazione<br/>                   | <dl> <dt>PortableDevice.h</dt> </dl> |



 

 




