---
title: GetPhysicalMonitors (funzione)
description: Ottiene i monitoraggi fisici associati a un dispositivo di visualizzazione.
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
ms.openlocfilehash: d95ccb801dbf06e096534754bd0adffbe36b5084
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301584"
---
# <a name="getphysicalmonitors-function"></a>GetPhysicalMonitors (funzione)

> [!IMPORTANT]
> Questa funzione viene usata dall'API di configurazione del monitoraggio per accedere alla funzionalità nel driver di visualizzazione. Le applicazioni non devono chiamare questa funzione.

 

Ottiene i monitoraggi fisici associati a un dispositivo di visualizzazione.

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

*pstrDeviceName* \[ in\]
</dt> <dd>

Puntatore a una struttura [**di \_ stringhe Unicode**](/windows/desktop/api/subauth/ns-subauth-unicode_string) che contiene il nome del dispositivo di visualizzazione, come restituito dalla funzione [**GetMonitorInfo**](/windows/desktop/api/winuser/nf-winuser-getmonitorinfoa) .

</dd> <dt>

*dwPhysicalMonitorArraySize* \[ in\]
</dt> <dd>

Numero di elementi nella matrice *pdwNumPhysicalMonitorHandlesInArray* . Per ottenere le dimensioni richieste della matrice, chiamare [**GetNumberOfPhysicalMonitors**](getnumberofphysicalmonitors.md).

</dd> <dt>

*pdwNumPhysicalMonitorHandlesInArray* \[ out\]
</dt> <dd>

Riceve il numero di elementi che la funzione copia nella matrice *phPhysicalMonitorArray* .

</dd> <dt>

*phPhysicalMonitorArray* \[ out\]
</dt> <dd>

Matrice che riceve handle per i monitoraggi fisici. Ogni handle deve essere rilasciato chiamando [**DestroyPhysicalMonitor**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-destroyphysicalmonitor).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, viene restituito **lo stato \_ Success**. In caso contrario, restituisce un codice di errore **NTSTATUS** .

## <a name="remarks"></a>Commenti

Anziché utilizzare questa funzione, le applicazioni devono chiamare una delle funzioni seguenti:

-   [**GetPhysicalMonitorsFromHMONITOR**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromhmonitor)
-   [**GetPhysicalMonitorsFromIDirect3DDevice9**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromidirect3ddevice9)

A questa funzione non è associata alcuna libreria di importazione. Per chiamare questa funzione, è necessario usare le funzioni [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) per eseguire il collegamento dinamico a Gdi32.dll.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Gdi32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Monitorare le funzioni di configurazione](monitor-configuration-functions.md)
</dt> </dl>

 

