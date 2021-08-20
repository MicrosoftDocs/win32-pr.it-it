---
description: Ottiene informazioni sulla versione del sistema operativo attualmente in esecuzione.
ms.assetid: F04F0981-A07D-4B38-9DE4-B8461EAFC19F
title: Funzione RtlGetVersion (Ntddk.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlGetVersion
api_type:
- DllExport
api_location:
- Ntdll.dll
- NtosKrnl.exe
ms.openlocfilehash: 7420b9dba03e3b136331f4463f476908882ca5564d0fc7ac563036c7acccb356
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118161683"
---
# <a name="rtlgetversion-function"></a>Funzione RtlGetVersion

Ottiene informazioni sulla versione del sistema operativo attualmente in esecuzione.

## <a name="syntax"></a>Sintassi


```C++
NTSTATUS RtlGetVersion(
  _Out_ PRTL_OSVERSIONINFOW lpVersionInformation
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lpVersionInformation* \[ Cambio\]
</dt> <dd>

Puntatore a una [**struttura RTL \_ OSVERSIONINFOW**](/windows-hardware/drivers/ddi/wdm/ns-wdm-_osversioninfow) o a una struttura [**RTL \_ OSVERSIONINFOEXW**](/windows-hardware/drivers/ddi/wdm/ns-wdm-_osversioninfoexw) che contiene le informazioni sulla versione del sistema operativo attualmente in esecuzione. Un chiamante specifica quale struttura di input viene usata impostando il membro **dwOSVersionInfoSize** della struttura sulla dimensione in byte della struttura utilizzata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce STATUS \_ SUCCESS.

## <a name="remarks"></a>Commenti

**RtlGetVersion** è l'equivalente della [**funzione GetVersionEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa) in Windows SDK. Vedere l'esempio in Windows SDK che illustra come ottenere la versione del sistema.

Quando si **usa RtlGetVersion** per determinare se una determinata versione del sistema operativo è in esecuzione, un chiamante deve verificare la presenza di numeri di versione maggiori o uguali al numero di versione richiesto. In questo modo si garantisce che un test della versione riesca per le versioni successive di Windows.

Poiché le funzionalità del sistema operativo possono essere aggiunte in una DLL ridistribuibile, il controllo solo dei numeri di versione principale e secondario non è il modo più affidabile per verificare la presenza di una funzionalità di sistema specifica. Un driver deve usare [**RtlVerifyVersionInfo**](/windows-hardware/drivers/ddi/wdm/nf-wdm-rtlverifyversioninfo) per verificare la presenza di una funzionalità di sistema specifica.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                                                                     |
| Piattaforma di destinazione<br/>          | <dl> <dt>[Universale](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt> </dl>                  |
| Intestazione<br/>                   | <dl> <dt>Ntddk.h (includere Ntddk.h)</dt> </dl>                                                     |
| Libreria<br/>                  | <dl> <dt>Ntdll.lib; </dt> <dt>NtosKrnl.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ntdll.dll; </dt> <dt>NtosKrnl.exe</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**PsGetVersion**](/windows-hardware/drivers/ddi/wdm/nf-wdm-psgetversion)
</dt> </dl>

 

 
