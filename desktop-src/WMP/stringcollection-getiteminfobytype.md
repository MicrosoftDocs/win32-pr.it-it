---
title: StringCollection. getItemInfoByType, metodo
description: Il metodo getItemInfoByType Recupera il valore corrispondente all'indice Stringacollection, al nome, alla lingua e all'indice dell'attributo specificati.
ms.assetid: 32a25c69-9399-4857-84c1-143c529be58f
keywords:
- Metodo getItemInfoByType Windows Media Player
- Metodo getItemInfoByType Windows Media Player, classe StringCollection
- StringCollection (classe) Windows Media Player, metodo getItemInfoByType
topic_type:
- apiref
api_name:
- StringCollection.getItemInfoByType
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4b3aa8c5bc367095765f24f19f107dd7cb986ec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326448"
---
# <a name="stringcollectiongetiteminfobytype-method"></a>StringCollection. getItemInfoByType, metodo

Il metodo **getItemInfoByType** Recupera il valore corrispondente all'indice **stringacollection** , al nome, alla lingua e all'indice dell'attributo specificati.

## <a name="syntax"></a>Sintassi


```JScript
retVal = StringCollection.getItemInfoByType(
  index,
  name,
  language,
  attributeIndex
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

</dd> <dt>

*lingua* \[ di in\]
</dt> <dd>

**Stringa** contenente il linguaggio. Se il valore è impostato su null o la stringa vuota ("") viene utilizzata la stringa delle impostazioni locali corrente. In caso contrario, il valore deve essere una stringa di linguaggio RFC 1766 valida, ad esempio "en-US".

</dd> <dt>

*attributeIndex* \[ in\]
</dt> <dd>

**Numero** (**Long**) che contiene l'indice in base zero del valore da recuperare dall'attributo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce un oggetto **Number**, **String**, **MetadataPicture** o **MetadataText** come indicato nella tabella seguente.



| Attributo                   | Valore restituito                   |
|-----------------------------|--------------------------------|
| **SyncState**               | **Numero** (**unsigned long**) |
| **WM/lyrics \_ sincronizzati** | Oggetto **MetadataText**        |
| **WM/immagine**              | Oggetto **MetadataPicture**     |
| **WM/UserWebURL**           | Oggetto **MetadataText**        |
| Tutti gli altri attributi        | string                         |



 

Per gli attributi il cui valore sottostante è **booleano**, questo metodo restituisce la stringa "true" o "false".

## <a name="remarks"></a>Commenti

Questo metodo supporta attributi con più valori e attributi con valori complessi. Il metodo **GetItemInfo** non supporta attributi con valori multipli o complessi.

Per usare questo metodo, è necessario l'accesso in lettura alla libreria. Per altre informazioni, vedere [accesso alla libreria](library-access.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto MetadataPicture**](metadatapicture-object.md)
</dt> <dt>

[**Oggetto MetadataText**](metadatatext-object.md)
</dt> <dt>

[**StringCollection. getItemInfo**](stringcollection-getiteminfo.md)
</dt> <dt>

[**StringCollection (oggetto)**](stringcollection-object.md)
</dt> </dl>

 

 





