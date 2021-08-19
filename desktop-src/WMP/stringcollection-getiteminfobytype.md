---
title: Metodo StringCollection.getItemInfoByType
description: Il metodo getItemInfoByType recupera il valore corrispondente all'indice, al nome, alla lingua e all'attributo StringCollection specificati.
ms.assetid: 32a25c69-9399-4857-84c1-143c529be58f
keywords:
- Metodo getItemInfoByType Windows Media Player
- Metodo getItemInfoByType Windows Media Player , classe StringCollection
- Classe StringCollection Windows Media Player metodo , getItemInfoByType
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
ms.openlocfilehash: 7b9d270ab746618f81f7c2e4135f7a6057f207d2cc89961ebe7c8f47d9fd1abd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120123031"
---
# <a name="stringcollectiongetiteminfobytype-method"></a>Metodo StringCollection.getItemInfoByType

Il **metodo getItemInfoByType** recupera il valore corrispondente all'indice, al nome, alla lingua e all'attributo **StringCollection** specificati.

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

*index* \[ Pollici\]
</dt> <dd>

**Numero** (**long**) che specifica l'indice in base zero dell'elemento **StringCollection** da cui ottenere l'attributo.

</dd> <dt>

*name* \[ Pollici\]
</dt> <dd>

**Stringa** contenente il nome dell'attributo.

</dd> <dt>

*language* \[ Pollici\]
</dt> <dd>

**Stringa** contenente la lingua. Se il valore è impostato su Null o la stringa vuota ("") viene usata la stringa delle impostazioni locali corrente. In caso contrario, il valore deve essere una stringa di lingua RFC 1766 valida, ad esempio "en-us".

</dd> <dt>

*attributeIndex* \[ Pollici\]
</dt> <dd>

**Numero** (**long**) contenente l'indice in base zero del valore da recuperare dall'attributo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce un **oggetto Number,** **String,** **MetadataPicture** o **MetadataText** come indicato nella tabella seguente.



| Attributo                   | Valore restituito                   |
|-----------------------------|--------------------------------|
| **SyncState**               | **Number** (**unsigned long**) |
| **WM/Lyrics \_ Synchronised** | **Oggetto MetadataText**        |
| **WM/Picture**              | **Oggetto MetadataPicture**     |
| **WM/UserWebURL**           | **Oggetto MetadataText**        |
| Tutti gli altri attributi        | string                         |



 

Per gli attributi il cui valore sottostante è **booleano,** questo metodo restituisce la stringa "true" o "false".

## <a name="remarks"></a>Commenti

Questo metodo supporta attributi con più valori e attributi con valori complessi. Il **metodo getItemInfo** non supporta attributi con valori multipli o complessi.

Per usare questo metodo, è necessario l'accesso in lettura alla libreria. Per altre informazioni, vedere [Accesso alla libreria](library-access.md).

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

[**StringCollection.getItemInfo**](stringcollection-getiteminfo.md)
</dt> <dt>

[**Oggetto StringCollection**](stringcollection-object.md)
</dt> </dl>

 

 





