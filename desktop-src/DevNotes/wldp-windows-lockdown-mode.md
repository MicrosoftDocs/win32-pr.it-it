---
description: Descrive le modalità sicure (modalità S) per un Windows dispositivo.
ms.assetid: CE50AC56-0295-477C-93CB-ABAB92482A59
title: WLDP_WINDOWS_LOCKDOWN_MODE enumerazione (Wldp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WLDP_WINDOWS_LOCKDOWN_MODE
api_type:
- HeaderDef
api_location:
- wldp.h
ms.openlocfilehash: 93a3ae8ef00c306d93995a3a97236fc9086185147144c4314726c507d8b52e57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119911341"
---
# <a name="wldp_windows_lockdown_mode-enumeration"></a>Enumerazione WLDP \_ WINDOWS \_ LOCKDOWN \_ MODE

Descrive le modalità sicure (modalità S) per un Windows dispositivo. Usato principalmente in [**WldpQueryWindowsLockdownMode.**](wldpquerywindowslockdownmode.md)

## <a name="syntax"></a>Sintassi


```C++
typedef enum _WLDP_WINDOWS_LOCKDOWN_MODE { 
  WLDP_WINDOWS_LOCKDOWN_MODE_UNLOCKED  = 0,
  WLDP_WINDOWS_LOCKDOWN_MODE_TRIAL     = 1,
  WLDP_WINDOWS_LOCKDOWN_MODE_LOCKED    = 2,
  WLDP_WINDOWS_LOCKDOWN_MODE_MAX       = 3
} WLDP_WINDOWS_LOCKDOWN_MODE, *PWLDP_WINDOWS_LOCKDOWN_MODE;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="WLDP_WINDOWS_LOCKDOWN_MODE_UNLOCKED"></span><span id="wldp_windows_lockdown_mode_unlocked"></span>**MODALITÀ DI BLOCCO DI WINDOWS WLDP \_ \_ \_ \_ SBLOCCATA**
</dt> <dd>

Sbloccato. Usato principalmente per i Windows senza la modalità S.

</dd> <dt>

<span id="WLDP_WINDOWS_LOCKDOWN_MODE_TRIAL"></span><span id="wldp_windows_lockdown_mode_trial"></span>**VERSIONE DI VALUTAZIONE DELLA MODALITÀ DI BLOCCO DI WINDOWS WLDP \_ \_ \_ \_**
</dt> <dd>

Prova. Usato principalmente per un dispositivo Windows 10 di valutazione con la modalità S. La modalità di valutazione è un caso speciale per i dispositivi Windows 10 con la modalità S: i criteri vengono applicati, ma non esiste alcuna protezione anti-rollback per l'applicazione dei criteri.

</dd> <dt>

<span id="WLDP_WINDOWS_LOCKDOWN_MODE_LOCKED"></span><span id="wldp_windows_lockdown_mode_locked"></span>**MODALITÀ DI BLOCCO DI WINDOWS WLDP \_ \_ \_ \_ BLOCCATA**
</dt> <dd>

Bloccato. Usato principalmente per un Windows 10 dispositivo con la modalità S. Un dispositivo bloccato applichi i criteri di Device Guard firmati forniti con l'immagine Windows 10 del sistema operativo con la modalità S.

</dd> <dt>

<span id="WLDP_WINDOWS_LOCKDOWN_MODE_MAX"></span><span id="wldp_windows_lockdown_mode_max"></span>**WLDP \_ WINDOWS \_ LOCKDOWN \_ MODE \_ MAX**
</dt> <dd>

Valore massimo dell'enumerazione.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-----------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wldp.h</dt> </dl> |



 

 




