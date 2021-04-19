---
title: Proprietà burnPlaylist di IWMPCdromBurn
description: La proprietà burnPlaylist ottiene la playlist corrente da masterizzare nel CD.
ms.assetid: 973032de-7249-4ccd-9909-ccc888f4490f
keywords:
- Finestra delle proprietà di burnPlaylist Media Player
- Proprietà di burnPlaylist Media Player Windows, interfaccia IWMPCdromBurn
- Interfaccia IWMPCdromBurn Windows Media Player, proprietà burnPlaylist
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
ms.openlocfilehash: cae095696b9c106926fb7f363430574b2eb87cea
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329670"
---
# <a name="iwmpcdromburnburnplaylist-property"></a>Proprietà IWMPCdromBurn:: burnPlaylist

La proprietà **burnPlaylist** ottiene la playlist corrente da masterizzare nel CD.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```CSharp
public IWMPPlaylist burnPlaylist {get;}
```


```VB

Public ReadOnly Property burnPlaylist As IWMPPlaylist
```





## <a name="property-value"></a>Valore proprietà

Interfaccia **wmplib. IWMPPlaylist** della playlist da masterizzare.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player 11<br/>                                                                                     |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMPCdromBurn (VB e C#)**](iwmpcdromburn--vb-and-c.md)
</dt> <dt>

[**Interfaccia IWMPPlaylist (VB e C#)**](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





