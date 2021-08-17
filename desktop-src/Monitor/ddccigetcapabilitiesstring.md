---
title: Funzione DDCCIGetCapabilitiesString
description: Ottiene una stringa che descrive le funzionalità di un monitoraggio.
ms.assetid: 54041126-b710-4448-a9f0-9b644d6b8186
keywords:
- Configurazione del monitoraggio della funzione DDCCIGetCapabilitiesString
topic_type:
- apiref
api_name:
- DDCCIGetCapabilitiesString
api_location:
- gdi32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f21cf89ef459e2585dda9f05e4f16d032949d423c627225380481d71c59400d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117806129"
---
# <a name="ddccigetcapabilitiesstring-function"></a>Funzione DDCCIGetCapabilitiesString

> [!IMPORTANT]
> Questa funzione viene usata dall'API di configurazione del monitoraggio per accedere alle funzionalità nel driver video. Le applicazioni non devono chiamare questa funzione.

 

Ottiene una stringa che descrive le funzionalità di un monitoraggio.

## <a name="syntax"></a>Sintassi


```C++
NTSTATUS WINAPI DDCCIGetCapabilitiesString(
  _In_  HANDLE hMonitor,
  _Out_ LPSTR  pszString,
  _In_  DWORD  dwLength
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hMonitor* \[ Pollici\]
</dt> <dd>

Handle per un monitor fisico.

</dd> <dt>

*pszString* \[ Cambio\]
</dt> <dd>

Puntatore a un buffer che riceve la stringa di funzionalità. Per ottenere la lunghezza della stringa delle funzionalità, chiamare [**DDCCIGetCapabilitiesStringLength.**](ddccigetcapabilitiesstringlength.md)

</dd> <dt>

*dwLength* \[ Pollici\]
</dt> <dd>

Dimensione del buffer *pszString,* in caratteri, incluso il carattere Null di terminazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, restituisce **STATUS \_ SUCCESS**. In caso contrario, restituisce un **codice di errore NTSTATUS.**

## <a name="remarks"></a>Commenti

Le applicazioni devono [**chiamare CapabilitiesRequestAndCapabilitiesReply**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-capabilitiesrequestandcapabilitiesreply) invece di chiamare questa funzione.

A questa funzione non è associata alcuna libreria di importazione. Per chiamare questa funzione, è necessario usare le [**funzioni LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) per collegarsi in modo dinamico Gdi32.dll.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Gdi32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Monitorare le funzioni di configurazione](monitor-configuration-functions.md)
</dt> </dl>

 

