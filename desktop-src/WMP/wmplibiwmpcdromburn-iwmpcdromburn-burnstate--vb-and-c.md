---
title: Proprietà burnState di IWMPCdromBurn
description: La proprietà burnState ottiene un valore di enumerazione che indica lo stato Burn corrente.
ms.assetid: 2bb543f9-9e4c-4425-99d6-ac89ef7f5807
keywords:
- Finestra delle proprietà di burnState Media Player
- Proprietà di burnState Media Player Windows, interfaccia IWMPCdromBurn
- Interfaccia IWMPCdromBurn Windows Media Player, proprietà burnState
topic_type:
- apiref
api_name:
- IWMPCdromBurn.burnState
- IWMPCdromBurn.get_burnState
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c6b1aa8ec39f032e8f130a75370131bd2894c64
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329666"
---
# <a name="iwmpcdromburnburnstate-property"></a>Proprietà IWMPCdromBurn:: burnState

La proprietà **burnState** ottiene un valore di enumerazione che indica lo stato Burn corrente.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```CSharp
public WMPBurnState burnState {get;}
```


```VB

Public ReadOnly Property burnState As WMPBurnState
```





## <a name="property-value"></a>Valore proprietà

Oggetto **wmplib. WMPBurnState** che corrisponde a un valore dell'enumerazione **WMPBurnState** che indica lo stato corrente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player 11.<br/>                                                                                    |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMPCdromBurn (VB e C#)**](iwmpcdromburn--vb-and-c.md)
</dt> <dt>

[**WMPBurnState**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpburnstate)
</dt> </dl>

 

 





