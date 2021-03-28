---
description: Viene chiamato quando l'utente corrente ha richiesto la commutazione dell'identità utente, ma prima che si verifichi l'opzione.
ms.assetid: f159b829-623c-4348-9692-7317663811a7
title: 'Metodo IIdentityChangeNotify:: QuerySwitchIdentities (Msident. h)'
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
ms.openlocfilehash: 42f8033c943e402d434c973f8c768ed5a951811d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881545"
---
# <a name="iidentitychangenotifyqueryswitchidentities-method"></a>Metodo IIdentityChangeNotify:: QuerySwitchIdentities

\[**QuerySwitchIdentities** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile.\]

Viene chiamato quando l'utente corrente ha richiesto la commutazione dell'identità utente, ma prima che si verifichi l'opzione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT QuerySwitchIdentities();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Risultato della query switch. Se l'opzione deve continuare, restituire S \_ OK. In caso contrario, \_ restituire \_ l'opzione E processo annullato \_ per indicare che il cambio di identità utente deve essere interrotto.

## <a name="remarks"></a>Commenti

È possibile implementare questo metodo per fornire un comportamento personalizzato all'applicazione quando un utente richiede la commutazione delle identità. È possibile arrestare il cambio di identità in sospeso restituendo l'opzione valore E \_ processo \_ annullato \_ .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                             |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                   |
| Fine del supporto client<br/>    | Windows 2000 Professional<br/>                                                   |
| Fine del supporto server<br/>    | Windows 2000 Server<br/>                                                         |
| Intestazione<br/>                   | <dl> <dt>Msident. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Msident. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Msoe.dll</dt> </dl>    |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IIdentityChangeNotify**](iidentitychangenotify.md)
</dt> <dt>

[**IIdentityChangeNotify::SwitchIdentities**](iidentitychangenotify-switchidentities.md)
</dt> </dl>

 

 




