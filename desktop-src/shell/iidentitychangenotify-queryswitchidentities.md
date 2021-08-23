---
description: Chiamato quando l'utente corrente ha richiesto di cambiare l'identità utente, ma prima che si verifichi il passaggio.
ms.assetid: f159b829-623c-4348-9692-7317663811a7
title: Metodo IIdentityChangeNotify::QuerySwitchIdentities (Msident.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IIdentityChangeNotify.QuerySwitchIdentities
api_type:
- COM
api_location:
- Msoe.dll
ms.openlocfilehash: 38469490db92278c82e7935e1078181010757dd22be220203361d2d4c18ef380
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119593081"
---
# <a name="iidentitychangenotifyqueryswitchidentities-method"></a>Metodo IIdentityChangeNotify::QuerySwitchIdentities

\[**QuerySwitchIdentities** è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile.\]

Chiamato quando l'utente corrente ha richiesto di cambiare l'identità utente, ma prima che si verifichi il passaggio.

## <a name="syntax"></a>Sintassi


```C++
HRESULT QuerySwitchIdentities();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Risultato della query switch. Se l'opzione deve continuare, restituire S \_ OK. In caso contrario, restituire E \_ PROCESS \_ CANCELLED \_ SWITCH per indicare che l'opzione di identità utente deve essere interrotta.

## <a name="remarks"></a>Commenti

È possibile implementare questo metodo per fornire un comportamento personalizzato per l'applicazione quando un utente richiede che le identità siano cambiate. È possibile arrestare l'opzione identity in sospeso restituisce il valore E \_ PROCESS \_ CANCELLED \_ SWITCH.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                             |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                   |
| Fine del supporto client<br/>    | Windows 2000 Professional<br/>                                                   |
| Fine del supporto server<br/>    | Windows 2000 Server<br/>                                                         |
| Intestazione<br/>                   | <dl> <dt>Msident.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Msident.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Msoe.dll</dt> </dl>    |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IIdentityChangeNotify**](iidentitychangenotify.md)
</dt> <dt>

[**IIdentityChangeNotify::SwitchIdentities**](iidentitychangenotify-switchidentities.md)
</dt> </dl>

 

 




