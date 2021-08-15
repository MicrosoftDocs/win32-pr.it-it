---
title: Metodo IWMPPlaylistArray Item
description: Il metodo Item restituisce un'interfaccia IWMPPlaylist che rappresenta la playlist in corrispondenza dell'indice specificato.
ms.assetid: 5cb4b89f-b679-4d92-a5f9-5d0fe686775d
keywords:
- Metodo Item Windows Media Player
- Metodo Item Windows Media Player, interfaccia IWMPPlaylistArray
- Interfaccia IWMPPlaylistArray Windows Media Player , metodo Item
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
ms.openlocfilehash: 9e73614e1ef00f29d6b09d3d49e2c7e514bae807245f00f30f4d3382d8f1a2e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118331160"
---
# <a name="iwmpplaylistarrayitem-method"></a>Metodo IWMPPlaylistArray::Item

Il **metodo Item** restituisce **un'interfaccia IWMPPlaylist** che rappresenta la playlist in corrispondenza dell'indice specificato.

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

*lIndex* \[ Pollici\]
</dt> <dd>

Oggetto **System.Int32** contenente l'indice che identifica la playlist che il metodo deve recuperare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Interfaccia **WMPLib.IWMPPlaylist** per la playlist recuperata.

## <a name="remarks"></a>Commenti

Prima di chiamare questo metodo, è necessario avere accesso in lettura alla libreria. Per altre informazioni, vedere [Accesso alla libreria](library-access.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player serie 9 o successive.<br/>                                                                     |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMPPlaylist (VB e C#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**Interfaccia IWMPPlaylistArray (VB e C#)**](iwmpplaylistarray--vb-and-c.md)
</dt> </dl>

 

 





