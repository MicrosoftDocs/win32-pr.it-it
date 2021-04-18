---
title: Proprietà burnFormat di IWMPCdromBurn
description: La proprietà burnFormat ottiene un valore che indica il tipo di CD da masterizzare.
ms.assetid: f60fcbd2-5d34-46f3-a2e2-29dac2ecf689
keywords:
- Finestra delle proprietà di burnFormat Media Player
- Proprietà di burnFormat Media Player Windows, interfaccia IWMPCdromBurn
- Interfaccia IWMPCdromBurn Windows Media Player, proprietà burnFormat
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
ms.openlocfilehash: 17e379727376b1ce272a95cd77c688fa611b291a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329672"
---
# <a name="iwmpcdromburnburnformat-property"></a>Proprietà IWMPCdromBurn:: burnFormat

La proprietà **burnFormat** ottiene un valore che indica il tipo di CD da masterizzare.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```CSharp
public WMPBurnFormat burnFormat {get;}
```


```VB

Public ReadOnly Property burnFormat As WMPBurnFormat
```





## <a name="property-value"></a>Valore proprietà

Oggetto **wmplib. WMPBurnFormat** che corrisponde a un valore dell'enumerazione **WMPBurnFormat** che indica il tipo di CD da masterizzare.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|----------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player 11<br/>                                                                             |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                          |
| Assembly<br/>  | <dl> <dt>Interop. WMPLib (Interop.WMPLib.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMPCdromBurn (VB e C#)**](iwmpcdromburn--vb-and-c.md)
</dt> <dt>

[**WMPBurnFormat**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpburnformat)
</dt> </dl>

 

 





