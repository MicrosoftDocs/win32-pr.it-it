---
description: Ottiene le informazioni sulla versione relative al sistema operativo attualmente in esecuzione.
ms.assetid: F04F0981-A07D-4B38-9DE4-B8461EAFC19F
title: Funzione RtlGetVersion (ntddk. h)
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
ms.openlocfilehash: a6a026ee55a6ccd75162915729070ad76f621bc8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126405"
---
# <a name="rtlgetversion-function"></a>RtlGetVersion (funzione)

Ottiene le informazioni sulla versione relative al sistema operativo attualmente in esecuzione.

## <a name="syntax"></a>Sintassi


```C++
NTSTATUS RtlGetVersion(
  _Out_ PRTL_OSVERSIONINFOW lpVersionInformation
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lpVersionInformation* \[ out\]
</dt> <dd>

Puntatore a una struttura [**\_ OSVERSIONINFOW RTL**](/windows-hardware/drivers/ddi/wdm/ns-wdm-_osversioninfow) o a una [**struttura \_ OSVERSIONINFOEXW RTL**](/windows-hardware/drivers/ddi/wdm/ns-wdm-_osversioninfoexw) che contiene le informazioni sulla versione relative al sistema operativo attualmente in esecuzione. Un chiamante specifica quale struttura di input viene utilizzata impostando il membro **dwOSVersionInfoSize** della struttura sulla dimensione in byte della struttura utilizzata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce lo stato \_ riuscito.

## <a name="remarks"></a>Commenti

**RtlGetVersion** è l'equivalente della funzione [**GetVersionEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa) nel Windows SDK. Vedere l'esempio nell'Windows SDK che Mostra come ottenere la versione del sistema.

Quando si usa **RtlGetVersion** per determinare se una particolare versione del sistema operativo è in esecuzione, un chiamante deve verificare la presenza di numeri di versione maggiori o uguali al numero di versione richiesto. In questo modo si garantisce la riuscita di un test della versione per le versioni successive di Windows.

Poiché è possibile aggiungere funzionalità del sistema operativo in una DLL ridistribuibile, controllare solo i numeri di versione principale e secondaria non è il modo più affidabile per verificare la presenza di una funzionalità di sistema specifica. Un driver deve utilizzare [**RtlVerifyVersionInfo**](/windows-hardware/drivers/ddi/wdm/nf-wdm-rtlverifyversioninfo) per verificare la presenza di una funzionalità di sistema specifica.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                                                                     |
| Piattaforma di destinazione<br/>          | <dl> <dt>[Universale](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt> </dl>                  |
| Intestazione<br/>                   | <dl> <dt>Ntddk. h (include ntddk. h)</dt> </dl>                                                     |
| Libreria<br/>                  | <dl> <dt>Ntdll. lib; </dt> <dt>NtosKrnl. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ntdll.dll; </dt> <dt>NtosKrnl.exe</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**PsGetVersion**](/windows-hardware/drivers/ddi/wdm/nf-wdm-psgetversion)
</dt> </dl>

 

 
