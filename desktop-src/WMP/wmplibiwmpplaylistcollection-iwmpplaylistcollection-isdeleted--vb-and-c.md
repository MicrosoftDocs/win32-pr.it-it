---
title: Metodo isDeleted IWMPPlaylistCollection
description: Il metodo isDeleted restituisce un valore che indica se la playlist specificata si trova nella cartella degli elementi eliminati.
ms.assetid: 02bc4b9f-6149-4fe2-8417-6484b22f2d74
keywords:
- Metodo isDeleted Windows Media Player
- Metodo isDeleted Windows Media Player, interfaccia IWMPPlaylistCollection
- Interfaccia IWMPPlaylistCollection Windows Media Player metodo , isDeleted
topic_type:
- apiref
api_name:
- IWMPPlaylistCollection.isDeleted
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c332a524b334933d587929cdd0e5b5fa61bc15d9110260af8af8e472d7c05fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118568478"
---
# <a name="iwmpplaylistcollectionisdeleted-method"></a>Metodo IWMPPlaylistCollection::isDeleted

Il **metodo isDeleted** restituisce un valore che indica se la playlist specificata si trova nella cartella degli elementi eliminati.

## <a name="syntax"></a>Sintassi


```CSharp
public System.Boolean isDeleted(
  IWMPPlaylist pItem
);
```


```VB

Public Function isDeleted( _
  ByVal pItem As IWMPPlaylist _
) As System.Boolean
Implements IWMPPlaylistCollection.isDeleted
```





## <a name="parameters"></a>Parametri

<dl> <dt>

*pItem* \[ Pollici\]
</dt> <dd>

Interfaccia **WMPLib.IWMPPlaylist** per la playlist su cui viene eseguita la query.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

**System.Boolean che** specifica se la playlist è stata eliminata.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player serie 9 o successiva.<br/>                                                                     |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMPPlaylist (VB e C#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**Interfaccia IWMPPlaylistCollection (VB e C#)**](iwmpplaylistcollection--vb-and-c.md)
</dt> </dl>

 

 





