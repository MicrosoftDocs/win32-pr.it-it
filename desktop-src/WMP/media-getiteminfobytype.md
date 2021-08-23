---
title: Metodo Media.getItemInfoByType
description: Il metodo getItemInfoByType recupera il valore dell'attributo corrispondente al nome dell'attributo, alla lingua e all'indice specificati.
ms.assetid: 9d3377c2-7ae8-48ce-a42e-9c965f6b79f9
keywords:
- Metodo getItemInfoByType Windows Media Player
- Metodo getItemInfoByType Windows Media Player , classe Media
- Classe media Windows Media Player metodo , getItemInfoByType
topic_type:
- apiref
api_name:
- Media.getItemInfoByType
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa180834d70c8dd078beafc360400c931e7058994f1cc46d4e9abb011987d158
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135124"
---
# <a name="mediagetiteminfobytype-method"></a>Metodo Media.getItemInfoByType

Il **metodo getItemInfoByType** recupera il valore dell'attributo corrispondente al nome dell'attributo, alla lingua e all'indice specificati.

## <a name="syntax"></a>Sintassi


```JScript
retVal = Media.getItemInfoByType(
  name,
  language,
  index
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*name* \[ Pollici\]
</dt> <dd>

**Stringa** contenente il nome dell'attributo. Per informazioni sugli attributi supportati da Windows Media Player, vedere le informazioni di Windows Media Player [sugli attributi.](attribute-reference.md)

</dd> <dt>

*lingua* \[ Pollici\]
</dt> <dd>

**Stringa** che rappresenta la lingua. Se il valore è impostato su Null o "" (stringa vuota), viene usata la stringa delle impostazioni locali corrente. In caso contrario, il valore deve essere una stringa di lingua RFC 1766 valida, ad esempio "en-us".

</dd> <dt>

*index* \[ Pollici\]
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
| Tutti gli altri attributi        | **Stringa**                     |



 

Per gli attributi il cui valore sottostante **è booleano,** questo metodo restituisce la stringa "true" o "false".

## <a name="remarks"></a>Commenti

Questo metodo recupera i metadati per un singolo elemento multimediale digitale o un elemento multimediale che fa parte di una playlist.

Questo metodo supporta attributi con più valori e attributi con valori complessi. Il **metodo getItemInfo** non supporta attributi con più valori e attributi con valori complessi.

La **proprietà attributeCount** contiene il numero di nomi di attributi disponibili per un determinato **oggetto Media.** I numeri di indice possono quindi essere usati con **il metodo getAttributeName** per determinare il nome di ogni attributo disponibile. I nomi dei singoli attributi possono essere passati al *parametro name* di **getItemInfoByType.**

Il **metodo getAttributeCountByType** restituisce il numero di attributi che corrispondono a un nome di attributo specifico per un determinato **oggetto Media.** I numeri di indice possono quindi essere passati al *parametro index* di **getItemInfoByType.** Ciò è utile, ad esempio, quando un elemento multimediale digitale è stato categorizzato in più generi.

Per usare questo metodo, è necessario l'accesso in lettura alla libreria. Per altre informazioni, vedere [Accesso alla libreria.](library-access.md)

Questo metodo può causare errori. Quando si chiama questo metodo, è necessario includere il codice di gestione degli errori. Ad esempio, in JScript è possibile implementare la gestione degli errori usando il metodo **try... Prendere... struttura** finally.

**Windows Media Player 10 Mobile:** Questo metodo non è supportato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player serie 9 o successiva.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto multimediale**](media-object.md)
</dt> <dt>

[**Media.attributeCount**](media-attributecount.md)
</dt> <dt>

[**Media.getAttributeCountByType**](media-getattributecountbytype.md)
</dt> <dt>

[**Media.getAttributeName**](media-getattributename.md)
</dt> <dt>

[**Media.getItemInfo**](media-getiteminfo.md)
</dt> <dt>

[**Media.setItemInfo**](media-setiteminfo.md)
</dt> <dt>

[**Oggetto MetadataPicture**](metadatapicture-object.md)
</dt> <dt>

[**Oggetto MetadataText**](metadatatext-object.md)
</dt> <dt>

[**Lettura dei valori degli attributi**](reading-attribute-values.md)
</dt> <dt>

[**Impostazioni.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Impostazioni.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





