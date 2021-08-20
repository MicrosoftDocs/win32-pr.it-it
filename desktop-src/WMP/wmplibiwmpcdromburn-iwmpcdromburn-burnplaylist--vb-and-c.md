---
title: Proprietà burnPlaylist IWMPCdromPlaylist
description: La proprietà burnPlaylist ottiene la playlist corrente da masterizzare nel CD.
ms.assetid: 973032de-7249-4ccd-9909-ccc888f4490f
keywords:
- Proprietà burnPlaylist Windows Media Player
- Proprietà burnPlaylist Windows Media Player, interfaccia IWMPCdromCombo
- Interfaccia IWMPCdrom Windows Media Player , proprietà burnPlaylist
topic_type:
- apiref
api_name:
- IWMPCdromBurn.burnPlaylist
- IWMPCdromBurn.get_burnPlaylist
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 186996632a5b25c89019f9bbb692d9804ae33130650d4b0a29c0cb51e30d0792
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118116594"
---
# <a name="iwmpcdromburnburnplaylist-property"></a>Proprietà IWMPCdromComb::burnPlaylist

La **proprietà burnPlaylist** ottiene la playlist corrente da masterizzare nel CD.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```CSharp
public IWMPPlaylist burnPlaylist {get;}
```


```VB

Public ReadOnly Property burnPlaylist As IWMPPlaylist
```





## <a name="property-value"></a>Valore proprietà

Interfaccia **WMPLib.IWMPPlaylist** della playlist da masterizzare.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player 11<br/>                                                                                     |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMPCdrom Sistema (VB e C#)**](iwmpcdromburn--vb-and-c.md)
</dt> <dt>

[**Interfaccia IWMPPlaylist (VB e C#)**](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





