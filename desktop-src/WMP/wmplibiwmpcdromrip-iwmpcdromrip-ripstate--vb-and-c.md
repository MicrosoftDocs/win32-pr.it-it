---
title: Proprietà ripState di IWMPCdromRip
description: La proprietà ripState ottiene un valore di enumerazione che indica lo stato corrente del processo di estrazione.
ms.assetid: eacf36d9-725c-47cf-9f90-6241feeb67bc
keywords:
- Finestra delle proprietà di ripState Media Player
- Proprietà di ripState Media Player Windows, interfaccia IWMPCdromRip
- Interfaccia IWMPCdromRip Windows Media Player, proprietà ripState
topic_type:
- apiref
api_name:
- IWMPCdromRip.ripState
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0245ea8ff7d863faa1f44c8d0578777ae6cd605
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329287"
---
# <a name="iwmpcdromripripstate-property"></a>Proprietà IWMPCdromRip:: ripState

La proprietà **ripState** ottiene un valore di enumerazione che indica lo stato corrente del processo di estrazione.

## <a name="syntax"></a>Sintassi


```CSharp
public WMPRipState ripState {get; set;}
```


```VB

Public ReadOnly Property ripState As WMPRipState
```





## <a name="property-value"></a>Valore proprietà

Oggetto **wmplib. WMPRipState** che corrisponde a un valore dell'enumerazione **WMPRipState** che indica lo stato corrente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player 11.<br/>                                                                                    |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMPCdromRip (VB e C#)**](iwmpcdromrip--vb-and-c.md)
</dt> <dt>

[**Copia di un CD**](ripping-a-cd.md)
</dt> <dt>

[**WMPRipState**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpripstate)
</dt> </dl>

 

 





