---
description: Descrive le modalità protette per un dispositivo Windows.
ms.assetid: CE50AC56-0295-477C-93CB-ABAB92482A59
title: Enumerazione WLDP_WINDOWS_LOCKDOWN_MODE (Wldp. h)
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
ms.openlocfilehash: 438a44bec0745ea67b2b40c3f8aa9c0dd6bd0072
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332366"
---
# <a name="wldp_windows_lockdown_mode-enumeration"></a>\_Enumerazione della \_ modalità di blocco di Windows WLDP \_

Descrive le modalità protette per un dispositivo Windows. Usato principalmente in [**WldpQueryWindowsLockdownMode**](wldpquerywindowslockdownmode.md).

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

<span id="WLDP_WINDOWS_LOCKDOWN_MODE_UNLOCKED"></span><span id="wldp_windows_lockdown_mode_unlocked"></span>**\_modalità di blocco di Windows WLDP \_ \_ \_ sbloccata**
</dt> <dd>

Sbloccato. Usato principalmente per i dispositivi Windows senza la modalità S.

</dd> <dt>

<span id="WLDP_WINDOWS_LOCKDOWN_MODE_TRIAL"></span><span id="wldp_windows_lockdown_mode_trial"></span>**versione di valutazione di WLDP \_ Windows \_ Lockdown \_ mode \_**
</dt> <dd>

Valutazione. Usato principalmente per un dispositivo di valutazione Windows 10 con la modalità S. La modalità di valutazione è un caso speciale per i dispositivi Windows 10 con la modalità S: i criteri vengono applicati, ma non esiste alcuna protezione anti-rollback per l'applicazione dei criteri.

</dd> <dt>

<span id="WLDP_WINDOWS_LOCKDOWN_MODE_LOCKED"></span><span id="wldp_windows_lockdown_mode_locked"></span>**\_modalità di blocco di Windows WLDP \_ \_ \_ bloccata**
</dt> <dd>

Bloccato. Usato principalmente per un dispositivo Windows 10 con la modalità S. Un dispositivo bloccato imporrà i criteri di Device Guard firmati forniti con l'immagine del sistema operativo Windows 10 con la modalità S.

</dd> <dt>

<span id="WLDP_WINDOWS_LOCKDOWN_MODE_MAX"></span><span id="wldp_windows_lockdown_mode_max"></span>**WLDP \_ \_ modalità blocco \_ Windows \_ Max**
</dt> <dd>

Valore massimo dell'enumerazione.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-----------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wldp. h</dt> </dl> |



 

 




