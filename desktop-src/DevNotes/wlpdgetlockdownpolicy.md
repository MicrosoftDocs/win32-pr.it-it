---
description: Chiama la libreria per ottenere lo stato di sicurezza relativo all'host e script o msi da usare.
ms.assetid: 4CCDA3B7-7661-47F6-A015-720BDEAEDBB1
title: Funzione WldpGetLockdownPolicy (Wldp.h)
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
ms.openlocfilehash: 47ae90c966ac259791d0ffb9c60d736430ede610db3932dd08ff60cc9e3b7b21
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119390191"
---
# <a name="wldpgetlockdownpolicy-function"></a>Funzione WldpGetLockdownPolicy

Chiama la libreria per ottenere lo stato di sicurezza relativo all'host e script o msi da usare. Alla funzione non è associata alcuna libreria di importazione. È necessario usare le funzioni LoadLibrary e GetProcAddress per collegarsi in modo dinamico wldp.dll.

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

Struttura [**WLDP \_ HOST \_ INFORMATION**](wldp-host-information.md) che identifica l'host e il file di origine da valutare.

</dd> <dt>

*lockdownState* \[ Cambio\]
</dt> <dd>

Fornisce il valore di sicurezza dei criteri risultante. Se! WLDP_LOCKDOWN_IS_OFF, UMCI è abilitato. È anche possibile controllare WLDP_LOCKDOWN_IS_AUDIT e WLDP_LOCKDOWN_IS_ENFORCE per determinare se un criterio è in modalità di controllo o di imposizione.
</dd> <dt>

*lockdownFlags* \[ Pollici\]
</dt> <dd>

I valori dei flag seguenti sono definiti come flag WLDP FLAGS SKIPSIGNATUREVALIDATION 0x00000100: se impostati, ignorare la convalida \_ SaferIdentifyLevel, che ignorerà se uno script è \_ firmato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce S \_ OK in caso di esito positivo o un codice di errore in caso contrario.

## <a name="remarks"></a>Commenti

Quando viene chiamato con WLDP HOST INFORMATION.szSource = NULL, vengono restituiti i criteri \_ \_ generici per l'host.

Quando viene chiamato con WLDP \_ HOST \_ INFORMATION.dwHostId = WLDP \_ HOST ID \_ \_ GLOBAL, WLDP \_ HOST \_ INFORMATION.szSource deve essere NULL e la funzione restituirà i criteri di sistema globali.

Il dwFlag WLDP FLAGS SKIPSIGNATUREVALIDATION può essere usato per ignorare la convalida \_ SaferIdentifyLevel(), che ignorerà se uno \_ script è firmato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 10 solo app desktop\]<br/>                                         |
| Server minimo supportato<br/> | \[Windows Server 2016 solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Wldp.h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Wldp.dll</dt> </dl> |



 

 




