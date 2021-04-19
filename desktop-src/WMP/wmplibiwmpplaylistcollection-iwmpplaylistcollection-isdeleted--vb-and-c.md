---
title: Metodo IWMPPlaylistCollection eliminato
description: Il metodo isvalidd restituisce un valore che indica se la playlist specificata si trova nella cartella Deleted Items.
ms.assetid: 02bc4b9f-6149-4fe2-8417-6484b22f2d74
keywords:
- Metodo eliminato Media Player Windows
- Metodo di eliminazione di Windows Media Player, interfaccia IWMPPlaylistCollection
- Interfaccia IWMPPlaylistCollection Windows Media Player, metodo eliminato
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
ms.openlocfilehash: 7d4ce4a314378c5a4a211a52b99ea1b36ae1fda8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324066"
---
# <a name="iwmpplaylistcollectionisdeleted-method"></a>Metodo IWMPPlaylistCollection:: IsValid

Il **Metodo** isvalidd restituisce un valore che indica se la playlist specificata si trova nella cartella Deleted Items.

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

*pItem* \[ in\]
</dt> <dd>

Interfaccia **wmplib. IWMPPlaylist** per la playlist sottoposta a query.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

**System. Boolean** che specifica se la playlist è stata eliminata.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player 9 serie o versione successiva.<br/>                                                                     |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMPPlaylist (VB e C#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**Interfaccia IWMPPlaylistCollection (VB e C#)**](iwmpplaylistcollection--vb-and-c.md)
</dt> </dl>

 

 





