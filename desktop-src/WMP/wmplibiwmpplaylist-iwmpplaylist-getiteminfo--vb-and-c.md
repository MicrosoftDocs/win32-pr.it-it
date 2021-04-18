---
title: Metodo IWMPPlaylist getItemInfo
description: Il metodo getItemInfo restituisce il valore di un attributo della playlist specificato in base al nome.
ms.assetid: 62e882d6-66bb-450c-9700-b99d30dd42fa
keywords:
- metodo getItemInfo Windows Media Player
- metodo getItemInfo Windows Media Player, interfaccia IWMPPlaylist
- Interfaccia IWMPPlaylist Windows Media Player, metodo getItemInfo
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
ms.openlocfilehash: ced433b13f5af2d1df8c12dba023b7fbb55c5f7d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330976"
---
# <a name="iwmpplaylistgetiteminfo-method"></a>Metodo IWMPPlaylist:: getItemInfo

Il metodo **GetItemInfo** restituisce il valore di un attributo della playlist specificato in base al nome.

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

*bstrName* \[ in\]
</dt> <dd>

**System. String** che rappresenta il nome dell'attributo playlist.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

**System. String** che corrisponde al valore dell'attributo playlist.

## <a name="remarks"></a>Commenti

Prima di usare questo metodo, è necessario avere accesso in lettura alla libreria. Per altre informazioni, vedere [accesso alla libreria](library-access.md).

Per il codice di esempio che usa questa proprietà, vedere la proprietà [attributeCount](wmplibiwmpplaylist-iwmpplaylist-attributecount--vb-and-c.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player 9 serie o versione successiva<br/>                                                                      |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMPPlaylist (VB e C#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylist. setItemInfo (VB e C#)**](wmplibiwmpplaylist-iwmpplaylist-setiteminfo--vb-and-c.md)
</dt> </dl>

 

 





