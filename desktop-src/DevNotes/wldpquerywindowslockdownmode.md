---
description: Recupera la modalità protetta di Windows corrente. Windows può essere in modalità bloccata, in modalità normale o in modalità di valutazione.
ms.assetid: FD280818-C6DE-4CEA-A772-E239A8DB891F
title: Funzione WldpQueryWindowsLockdownMode (Wldp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WldpQueryWindowsLockdownMode
api_type:
- DllExport
api_location:
- wldp.dll
ms.openlocfilehash: fc746270a0634525154417cfba7e1529bee7edfb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225736"
---
# <a name="wldpquerywindowslockdownmode-function"></a>WldpQueryWindowsLockdownMode (funzione)

Recupera la modalità protetta di Windows corrente. Windows può essere in modalità bloccata, in modalità normale o in modalità di valutazione.

## <a name="syntax"></a>Sintassi


```C++
 WINAPI WldpQueryWindowsLockdownMode(
  _Out_ PWLDP_WINDOWS_LOCKDOWN_MODE lockdownMode
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lockdownMode* \[ out\]
</dt> <dd>

Se l'operazione riesce, restituisce una [**\_ modalità di \_ blocco \_ di Windows PWLDP**](wldp-windows-lockdown-mode.md) che indica la modalità protetta per il dispositivo Windows 10 corrente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce **\_ OK** se l'esito è positivo o un codice di errore; in caso contrario,.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows 10 versione 1803 \[\]<br/>                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2016\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Wldp. h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Wldp.dll</dt> </dl> |



 

 




