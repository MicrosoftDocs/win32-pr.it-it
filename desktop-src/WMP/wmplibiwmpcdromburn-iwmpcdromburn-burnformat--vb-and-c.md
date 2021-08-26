---
title: Proprietà burnFormat IWMPCdrom BurnFormat
description: La proprietà burnFormat ottiene un valore che indica il tipo di CD da masterizzare.
ms.assetid: f60fcbd2-5d34-46f3-a2e2-29dac2ecf689
keywords:
- proprietà burnFormat Windows Media Player
- proprietà burnFormat Windows Media Player, interfaccia IWMPCdromBurn
- Interfaccia IWMPCdromBurn Windows Media Player proprietà , burnFormat
topic_type:
- apiref
api_name:
- IWMPCdromBurn.burnFormat
- IWMPCdromBurn.get_burnFormat
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93d5dc4ff27b3650ee37f16a7e90eb535ebe373401363f8c93bd16d09061b7a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120000541"
---
# <a name="iwmpcdromburnburnformat-property"></a>Proprietà IWMPCdromBurn::burnFormat

La **proprietà burnFormat** ottiene un valore che indica il tipo di CD da masterizzare.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```CSharp
public WMPBurnFormat burnFormat {get;}
```


```VB

Public ReadOnly Property burnFormat As WMPBurnFormat
```





## <a name="property-value"></a>Valore proprietà

Oggetto **WMPLib.WMPKindFormat** che è un valore **dell'enumerazione WMPKindFormat** che indica il tipo di CD da masterizzare.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|----------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player 11<br/>                                                                             |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                          |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib (Interop.WMPLib.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMPCdromBurn (VB e C#)**](iwmpcdromburn--vb-and-c.md)
</dt> <dt>

[**WMPBurnFormat**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpburnformat)
</dt> </dl>

 

 





