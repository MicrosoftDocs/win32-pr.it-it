---
title: Proprietà count di IWMPPlaylist
description: La proprietà count ottiene il numero di elementi multimediali in una playlist.
ms.assetid: dbff3c86-2d42-4d47-a5cb-b8199efac728
keywords:
- Proprietà count Windows Media Player
- Proprietà count Windows Media Player, interfaccia IWMPPlaylist
- Interfaccia IWMPPlaylist Windows Media Player , proprietà count
topic_type:
- apiref
api_name:
- IWMPPlaylist.count
- IWMPPlaylist.get_count
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aad690278b45563395c926adb4d0329bff8a01c7e8ace2f25ff3fefdb9c39cee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118568696"
---
# <a name="iwmpplaylistcount-property"></a>Proprietà IWMPPlaylist::count

La **proprietà count** ottiene il numero di elementi multimediali in una playlist.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```CSharp
public System.Int32 count {get;}
```


```VB

Public ReadOnly Property count As System.Int32
```





## <a name="property-value"></a>Valore proprietà

**System.Int32** che rappresenta il numero di elementi multimediali nella playlist.

## <a name="remarks"></a>Commenti

Prima di usare questa proprietà, è necessario avere accesso in lettura alla libreria. Per altre informazioni, vedere [Accesso alla libreria.](library-access.md)

Vedere la [proprietà attributeCount](wmplibiwmpplaylist-iwmpplaylist-attributecount--vb-and-c.md) per il codice di esempio che usa questa proprietà.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player serie 9 o successive<br/>                                                                      |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMPPlaylist (VB e C#)**](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





