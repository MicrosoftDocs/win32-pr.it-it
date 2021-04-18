---
title: Metodo IWMPStringCollection2 getItemInfo
description: Il metodo getItemInfo restituisce la stringa corrispondente all'indice e al nome dell'elemento della raccolta di stringhe specificato.
ms.assetid: 4a107e85-9eb7-42be-b1f9-8e9e92e6e509
keywords:
- metodo getItemInfo Windows Media Player
- metodo getItemInfo Windows Media Player, interfaccia IWMPStringCollection2
- Interfaccia IWMPStringCollection2 Windows Media Player, metodo getItemInfo
topic_type:
- apiref
api_name:
- IWMPStringCollection2.getItemInfo
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4741c4a3ba74b03038974d8b66bc42c23830ebb3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331727"
---
# <a name="iwmpstringcollection2getiteminfo-method"></a>Metodo IWMPStringCollection2:: getItemInfo

Il metodo **GetItemInfo** restituisce la stringa corrispondente all'indice e al nome dell'elemento della raccolta di stringhe specificato.

## <a name="syntax"></a>Sintassi


```CSharp
public System.String getItemInfo(
  System.Int32 lCollectionIndex,
  System.String bstrItemName
);
```


```VB

Public Function getItemInfo( _
  ByVal lCollectionIndex As System.Int32, _
  ByVal bstrItemName As System.String _
) As System.String
Implements IWMPStringCollection2.getItemInfo
```





## <a name="parameters"></a>Parametri

<dl> <dt>

*lCollectionIndex* \[ in\]
</dt> <dd>

**System. Int32** che specifica l'indice in base zero dell'elemento della raccolta di stringhe da cui ottenere l'attributo.

</dd> <dt>

*bstrItemName* \[ in\]
</dt> <dd>

**System. String** che rappresenta il nome dell'attributo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

**System. String** che rappresenta il nome dell'elemento della raccolta di stringhe. Per gli attributi il cui valore sottostante è **System. Boolean**, viene restituita la stringa "true" o "false".

## <a name="remarks"></a>Commenti

Per recuperare gli attributi con più valori e attributi con valori complessi, usare il metodo **getItemInfoByType** .

Per usare questo metodo, è necessario l'accesso in lettura alla libreria. Per altre informazioni, vedere [accesso alla libreria](library-access.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player 11.<br/>                                                                                    |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMPStringCollection2**](iwmpstringcollection2--vb-and-c.md)
</dt> <dt>

[**IWMPStringCollection2. getItemInfoByType (VB e C#)**](wmplibiwmpstringcollection2-iwmpstringcollection2-getiteminfobytype--vb-and-c.md)
</dt> </dl>

 

 





