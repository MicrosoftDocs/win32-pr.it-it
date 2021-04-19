---
title: Metodo elemento IWMPPlaylistArray
description: Il metodo Item restituisce un'interfaccia IWMPPlaylist che rappresenta la playlist in corrispondenza dell'indice specificato.
ms.assetid: 5cb4b89f-b679-4d92-a5f9-5d0fe686775d
keywords:
- Metodo Item Media Player Windows
- Metodo Item Media Player Windows, interfaccia IWMPPlaylistArray
- Interfaccia IWMPPlaylistArray Windows Media Player, metodo Item
topic_type:
- apiref
api_name:
- IWMPPlaylistArray.Item
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 660e919ef51bbb9584971f25bdf92296d331de23
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329901"
---
# <a name="iwmpplaylistarrayitem-method"></a>Metodo IWMPPlaylistArray:: Item

Il metodo **Item** restituisce un'interfaccia **IWMPPlaylist** che rappresenta la playlist in corrispondenza dell'indice specificato.

## <a name="syntax"></a>Sintassi


```CSharp
public IWMPPlaylist Item(
  System.Int32 lIndex
);
```


```VB

Public Function Item( _
  ByVal lIndex As System.Int32 _
) As IWMPPlaylist
Implements IWMPPlaylistArray.Item
```





## <a name="parameters"></a>Parametri

<dl> <dt>

*lIndex* \[ in\]
</dt> <dd>

**System. Int32** che contiene l'indice che identifica la playlist che il metodo deve recuperare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Interfaccia **wmplib. IWMPPlaylist** per la playlist recuperata.

## <a name="remarks"></a>Commenti

Prima di chiamare questo metodo, è necessario disporre dell'accesso in lettura alla libreria. Per altre informazioni, vedere [accesso alla libreria](library-access.md).

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

[**Interfaccia IWMPPlaylistArray (VB e C#)**](iwmpplaylistarray--vb-and-c.md)
</dt> </dl>

 

 





