---
title: Metodo IWMPPlaylist setItemInfo
description: Il metodo setItemInfo imposta il valore di un attributo della playlist corrente.
ms.assetid: b3874298-8fbe-47a4-b696-cef0382aec7c
keywords:
- Metodo setItemInfo Windows Media Player
- Metodo setItemInfo Windows Media Player, interfaccia IWMPPlaylist
- Interfaccia IWMPPlaylist Windows Media Player, metodo setItemInfo
topic_type:
- apiref
api_name:
- IWMPPlaylist.setItemInfo
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cce882d050f1ce7839fe3589fced3a87d9052fec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330343"
---
# <a name="iwmpplaylistsetiteminfo-method"></a>Metodo IWMPPlaylist:: setItemInfo

Il metodo **setItemInfo** imposta il valore di un attributo della playlist corrente.

## <a name="syntax"></a>Sintassi


```CSharp
public void setItemInfo(
  System.String bstrName,
  System.String bstrValue
);
```


```VB

Public Sub setItemInfo( _
  ByVal bstrName As System.String, _
  ByVal bstrValue As System.String _
)
Implements IWMPPlaylist.setItemInfo
```





## <a name="parameters"></a>Parametri

<dl> <dt>

*bstrName* \[ in\]
</dt> <dd>

**System. String** che rappresenta il nome dell'attributo.

</dd> <dt>

*bstrValue* \[ in\]
</dt> <dd>

**System. String** che corrisponde al valore dell'attributo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Prima di chiamare questo metodo, è necessario disporre dell'accesso completo alla libreria. Per altre informazioni, vedere [accesso alla libreria](library-access.md).

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

[**IWMPPlaylist. getItemInfo (VB e C#)**](wmplibiwmpplaylist-iwmpplaylist-getiteminfo--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2. mediaAccessRights (VB e C#)**](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2. requestMediaAccessRights (VB e C#)**](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





