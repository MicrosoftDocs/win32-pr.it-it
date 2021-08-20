---
title: Funzione GetPhysicalMonitorDescription
description: Ottiene una descrizione di un monitoraggio fisico.
ms.assetid: 81789eaf-7831-4833-87e1-7f318f831c96
keywords:
- Configurazione del monitoraggio della funzione GetPhysicalMonitorDescription
topic_type:
- apiref
api_name:
- GetPhysicalMonitorDescription
api_location:
- gdi32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 251c24db32271802b94bd2beb7a381cc9b3adb50dd97842203947ea6a6895583
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119534891"
---
# <a name="getphysicalmonitordescription-function"></a>Funzione GetPhysicalMonitorDescription

> [!IMPORTANT]
> Questa funzione viene usata dall'API di configurazione del monitoraggio per accedere alle funzionalità nel driver video. Le applicazioni non devono chiamare questa funzione.

 

Ottiene una descrizione di un monitoraggio fisico.

## <a name="syntax"></a>Sintassi


```C++
NTSTATUS WINAPI GetPhysicalMonitorDescription(
  _In_  HANDLE hMonitor,
  _In_  DWORD  dwPhysicalMonitorDescriptionSizeInChars,
  _Out_ LPWSTR szPhysicalMonitorDescription
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hMonitor* \[ Pollici\]
</dt> <dd>

Handle per un monitoraggio fisico.

</dd> <dt>

*dwPhysicalMonitorDescriptionSizeInChars* \[ Pollici\]
</dt> <dd>

Numero di caratteri nella *matrice szPhysicalMonitorDescription.*

</dd> <dt>

*szPhysicalMonitorDescription* \[ Cambio\]
</dt> <dd>

Puntatore a una matrice che riceve la descrizione. Il numero di elementi nella matrice deve essere almeno **PHYSICAL \_ MONITOR DESCRIPTION \_ \_ SIZE**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, restituisce **STATUS \_ SUCCESS**. In caso contrario, restituisce un **codice di errore NTSTATUS.**

## <a name="remarks"></a>Commenti

Anziché usare questa funzione, le applicazioni devono chiamare una delle funzioni seguenti:

-   [**GetPhysicalMonitorsFromHMONITOR**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromhmonitor)
-   [**GetPhysicalMonitorsFromIDirect3DDevice9**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromidirect3ddevice9)

A questa funzione non è associata alcuna libreria di importazione. Per chiamare questa funzione, è necessario usare le [**funzioni LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) per collegarsi dinamicamente Gdi32.dll.

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

 

