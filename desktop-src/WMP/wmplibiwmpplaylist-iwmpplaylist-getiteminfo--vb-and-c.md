---
title: Metodo IWMPPlaylist getItemInfo
description: Il metodo getItemInfo restituisce il valore di un attributo playlist specificato in base al nome.
ms.assetid: 62e882d6-66bb-450c-9700-b99d30dd42fa
keywords:
- Metodo getItemInfo Windows Media Player
- Metodo getItemInfo Windows Media Player, interfaccia IWMPPlaylist
- Interfaccia IWMPPlaylist Windows Media Player metodo , getItemInfo
topic_type:
- apiref
api_name:
- IWMPPlaylist.getItemInfo
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54e3ad24f12333dbc9db5baf977300d1755a9cecc60739504da05478d5acc48e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117745753"
---
# <a name="iwmpplaylistgetiteminfo-method"></a>Metodo IWMPPlaylist::getItemInfo

Il **metodo getItemInfo** restituisce il valore di un attributo playlist specificato in base al nome.

## <a name="syntax"></a>Sintassi


```CSharp
public System.String getItemInfo(
  System.String bstrName
);
```


```VB

Public Function getItemInfo( _
  ByVal bstrName As System.String _
) As System.String
Implements IWMPPlaylist.getItemInfo
```





## <a name="parameters"></a>Parametri

<dl> <dt>

*bstrName* \[ Pollici\]
</dt> <dd>

Oggetto **System.String** che rappresenta il nome dell'attributo della playlist.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Oggetto **System.String** che rappresenta il valore dell'attributo playlist.

## <a name="remarks"></a>Commenti

Prima di usare questo metodo, è necessario avere accesso in lettura alla libreria. Per altre informazioni, vedere [Accesso alla libreria](library-access.md).

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
</dt> <dt>

[**IWMPPlaylist.setItemInfo (VB e C#)**](wmplibiwmpplaylist-iwmpplaylist-setiteminfo--vb-and-c.md)
</dt> </dl>

 

 





