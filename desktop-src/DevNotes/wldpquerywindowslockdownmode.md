---
description: Recupera l'oggetto Windows modalità protetta. Windows essere in modalità bloccata, in modalità normale sbloccata o in modalità di valutazione.
ms.assetid: FD280818-C6DE-4CEA-A772-E239A8DB891F
title: Funzione WldpQueryWindowsLockdownMode (Wldp.h)
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
ms.openlocfilehash: 94dc1665dcfa98b27fc15f68a799792b57f428875fefb88c6d35de57bad71b5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119911291"
---
# <a name="wldpquerywindowslockdownmode-function"></a>Funzione WldpQueryWindowsLockdownMode

Recupera l'oggetto Windows modalità protetta. Windows essere in modalità bloccata, in modalità normale sbloccata o in modalità di valutazione.

## <a name="syntax"></a>Sintassi


```C++
 WINAPI WldpQueryWindowsLockdownMode(
  _Out_ PWLDP_WINDOWS_LOCKDOWN_MODE lockdownMode
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lockdownMode* \[ Cambio\]
</dt> <dd>

In caso di esito positivo, restituisce [**un oggetto PWLDP \_ WINDOWS \_ LOCKDOWN \_ MODE**](wldp-windows-lockdown-mode.md) che indica la modalità sicura per il dispositivo Windows 10 corrente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce **S \_ OK in caso** di esito positivo o un codice di errore in caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 10, solo app desktop versione 1803 \[\]<br/>                           |
| Server minimo supportato<br/> | \[Windows Server 2016 solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Wldp.h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Wldp.dll</dt> </dl> |



 

 




