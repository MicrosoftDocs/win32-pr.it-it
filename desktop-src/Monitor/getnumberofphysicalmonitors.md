---
title: GetNumberOfPhysicalMonitors (funzione)
description: Ottiene il numero di monitoraggi phyical associati a un dispositivo di visualizzazione.
ms.assetid: 498404e7-867d-4971-bea1-16e9f8fd9838
keywords:
- Configurazione del monitoraggio della funzione GetNumberOfPhysicalMonitors
topic_type:
- apiref
api_name:
- GetNumberOfPhysicalMonitors
api_location:
- gdi32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09bec6abf296d807f80ab77cdc7ad8b4062fea9b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873753"
---
# <a name="getnumberofphysicalmonitors-function"></a>GetNumberOfPhysicalMonitors (funzione)

> [!IMPORTANT]
> Questa funzione viene usata dall'API di configurazione del monitoraggio per accedere alla funzionalità nel driver di visualizzazione. Le applicazioni non devono chiamare questa funzione.

 

Ottiene il numero di monitoraggi phyical associati a un dispositivo di visualizzazione.

## <a name="syntax"></a>Sintassi


```C++
NTSTATUS WINAPI GetNumberOfPhysicalMonitors(
  _In_  UNICODE_STRING *pstrDeviceName,
  _Out_ LPDWORD        pdwNumberOfPhysicalMonitors
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pstrDeviceName* \[ in\]
</dt> <dd>

Puntatore a una struttura [**di \_ stringhe Unicode**](/windows/desktop/api/subauth/ns-subauth-unicode_string) che contiene il nome del dispositivo di visualizzazione, come restituito dalla funzione [**GetMonitorInfo**](/windows/desktop/api/winuser/nf-winuser-getmonitorinfoa) .

</dd> <dt>

*pdwNumberOfPhysicalMonitors* \[ out\]
</dt> <dd>

Riceve il numero di monitoraggi fisici.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, viene restituito **lo stato \_ Success**. In caso contrario, restituisce un codice di errore **NTSTATUS** .

## <a name="remarks"></a>Commenti

Anziché utilizzare questa funzione, le applicazioni devono chiamare una delle funzioni seguenti:

-   [**GetNumberOfPhysicalMonitorsFromHMONITOR**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getnumberofphysicalmonitorsfromhmonitor)
-   [**GetNumberOfPhysicalMonitorsFromIDirect3DDevice9**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getnumberofphysicalmonitorsfromidirect3ddevice9)

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

 

