---
title: Funzione GetPhysicalMonitors
description: Ottiene i monitor fisici associati a un dispositivo di visualizzazione.
ms.assetid: 8bbbad0a-2e45-439c-9312-f922a920c7fd
keywords:
- Configurazione del monitoraggio della funzione GetPhysicalMonitors
topic_type:
- apiref
api_name:
- GetPhysicalMonitors
api_location:
- gdi32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f94cef0352aae75f95b1ff7ee9e65937f82c7b598a19cdce768028173dc97331
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146154"
---
# <a name="getphysicalmonitors-function"></a>Funzione GetPhysicalMonitors

> [!IMPORTANT]
> Questa funzione viene usata dall'API di configurazione del monitoraggio per accedere alle funzionalità nel driver video. Le applicazioni non devono chiamare questa funzione.

 

Ottiene i monitor fisici associati a un dispositivo di visualizzazione.

## <a name="syntax"></a>Sintassi


```C++
NTSTATUS WINAPI GetPhysicalMonitors(
  _In_  UNICODE_STRING *pstrDeviceName,
  _In_  DWORD          dwPhysicalMonitorArraySize,
  _Out_ DWORD          *pdwNumPhysicalMonitorHandlesInArray,
  _Out_ HANDLE         *phPhysicalMonitorArray
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pstrDeviceName* \[ Pollici\]
</dt> <dd>

Puntatore a una [**struttura \_ STRING UNICODE**](/windows/desktop/api/subauth/ns-subauth-unicode_string) contenente il nome del dispositivo di visualizzazione, come restituito dalla [**funzione GetMonitorInfo.**](/windows/desktop/api/winuser/nf-winuser-getmonitorinfoa)

</dd> <dt>

*dwPhysicalMonitorArraySize* \[ Pollici\]
</dt> <dd>

Numero di elementi nella matrice *pdwNumPhysicalMonitorHandlesInArray.* Per ottenere le dimensioni richieste della matrice, chiamare [**GetNumberOfPhysicalMonitors**](getnumberofphysicalmonitors.md).

</dd> <dt>

*pdwNumPhysicalMonitorHandlesInArray* \[ Cambio\]
</dt> <dd>

Riceve il numero di elementi copiati dalla funzione nella matrice *phPhysicalMonitorArray.*

</dd> <dt>

*phPhysicalMonitorArray* \[ Cambio\]
</dt> <dd>

Matrice che riceve gli handle per i monitoraggi fisici. Ogni handle deve essere rilasciato chiamando [**DestroyPhysicalMonitor.**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-destroyphysicalmonitor)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, restituisce **STATUS \_ SUCCESS**. In caso contrario, restituisce un **codice di errore NTSTATUS.**

## <a name="remarks"></a>Commenti

Anziché usare questa funzione, le applicazioni devono chiamare una delle funzioni seguenti:

-   [**GetPhysicalMonitorsFromHMONITOR**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromhmonitor)
-   [**GetPhysicalMonitorsFromIDirect3DDevice9**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromidirect3ddevice9)

A questa funzione non è associata alcuna libreria di importazione. Per chiamare questa funzione, è necessario usare le [**funzioni LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) per il collegamento dinamico Gdi32.dll.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Gdi32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Monitorare le funzioni di configurazione](monitor-configuration-functions.md)
</dt> </dl>

 

