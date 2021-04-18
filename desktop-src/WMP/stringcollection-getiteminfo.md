---
title: StringCollection. getItemInfo, metodo
description: Il metodo getItemInfo recupera la stringa corrispondente all'indice e al nome dell'elemento StringCollection specificato.
ms.assetid: a031b91e-9d3b-47ac-bc5b-c111d5e3bc12
keywords:
- metodo getItemInfo Windows Media Player
- metodo getItemInfo Windows Media Player, classe StringCollection
- StringCollection (classe) Windows Media Player, metodo getItemInfo
topic_type:
- apiref
api_name:
- StringCollection.getItemInfo
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c9552dcebbc7d565ebc797c62ac3bc00ee109fb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328870"
---
# <a name="stringcollectiongetiteminfo-method"></a>StringCollection. getItemInfo, metodo

Il metodo **GetItemInfo** recupera la stringa corrispondente all'indice e al nome dell'elemento **StringCollection** specificato.

## <a name="syntax"></a>Sintassi


```JScript
strRetVal = StringCollection.getItemInfo(
  index,
  name
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Indice* \[ di in\]
</dt> <dd>

**Numero** (**Long**) che specifica l'indice in base zero dell'elemento **StringCollection** da cui ottenere l'attributo.

</dd> <dt>

*nome* \[ in\]
</dt> <dd>

**Stringa** contenente il nome dell'attributo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce una **stringa** che rappresenta il valore dell'attributo specificato. Per gli attributi il cui valore sottostante è **booleano**, viene restituita la stringa "true" o "false".

## <a name="remarks"></a>Commenti

Per recuperare gli attributi con più valori e attributi con valori complessi, usare il metodo **getItemInfoByType** .

Per usare questo metodo, è necessario l'accesso in lettura alla libreria. Per altre informazioni, vedere [accesso alla libreria](library-access.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**StringCollection. getItemInfoByType**](stringcollection-getiteminfobytype.md)
</dt> <dt>

[**StringCollection (oggetto)**](stringcollection-object.md)
</dt> </dl>

 

 





