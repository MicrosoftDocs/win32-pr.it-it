---
description: Chiama la libreria per ottenere lo stato di sicurezza relativo all'host e lo script o l'identità del servizio gestito da usare.
ms.assetid: 4CCDA3B7-7661-47F6-A015-720BDEAEDBB1
title: Funzione WldpGetLockdownPolicy (Wldp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WldpGetLockdownPolicy
api_type:
- DllExport
api_location:
- wldp.dll
ms.openlocfilehash: a8f5e4da11e8ce7443d9a9bab323742cfc1b3a9d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523465"
---
# <a name="wldpgetlockdownpolicy-function"></a>WldpGetLockdownPolicy (funzione)

Chiama la libreria per ottenere lo stato di sicurezza relativo all'host e lo script o l'identità del servizio gestito da usare. Alla funzione non è associata alcuna libreria di importazione. È necessario utilizzare le funzioni LoadLibrary e GetProcAddress per collegare dinamicamente a wldp.dll.

## <a name="syntax"></a>Sintassi


```C++
HRESULT WINAPI WldpGetLockdownPolicy(
  _In_opt_ PWLDP_HOST_INFORMATION hostInformation,
  _Out_    PDWORD                 lockdownState,
  _In_     DWORD                  lockdownFlags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hostInformation* \[ in, facoltativo\]
</dt> <dd>

Struttura [**di \_ \_ informazioni sull'host WLDP**](wldp-host-information.md) che identifica l'host e il file di origine da valutare.

</dd> <dt>

*lockdownState* \[ out\]
</dt> <dd>

Fornisce il valore sicuro del criterio risultante. Se! WLDP_LOCKDOWN_IS_OFF, UMCI è abilitato. È inoltre possibile controllare WLDP_LOCKDOWN_IS_AUDIT e WLDP_LOCKDOWN_IS_ENFORCE per determinare se un criterio è in modalità di controllo o di applicazione.
</dd> <dt>

*lockdownFlags* \[ in\]
</dt> <dd>

I valori di flag seguenti sono definiti WLDP \_ flags \_ SKIPSIGNATUREVALIDATION 0x00000100 – When set, Skip the SaferIdentifyLevel Validation, che ignorerà se uno script è firmato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce \_ OK se l'esito è positivo o un codice di errore; in caso contrario,.

## <a name="remarks"></a>Commenti

Quando viene chiamato con \_ \_ le informazioni sull'host WLDP. SZSOURCE = null, vengono restituiti i criteri generici per l'host.

Quando viene chiamato con \_ le \_ informazioni sull'host WLDP. DWHOSTID = WLDP \_ \_ ID host \_ globale, WLDP \_ host \_ Information. szSource deve essere null e la funzione restituirà i criteri di sistema globali.

I flag dwFlag \_ WLDP \_ SKIPSIGNATUREVALIDATION possono essere usati per ignorare la convalida SaferIdentifyLevel (), che ignorerà se uno script è firmato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows 10\]<br/>                                         |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2016\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Wldp. h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Wldp.dll</dt> </dl> |



 

 




