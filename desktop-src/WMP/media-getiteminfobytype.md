---
title: Media. getItemInfoByType, metodo
description: Il metodo getItemInfoByType Recupera il valore dell'attributo corrispondente al nome dell'attributo, alla lingua e all'indice specificati.
ms.assetid: 9d3377c2-7ae8-48ce-a42e-9c965f6b79f9
keywords:
- Metodo getItemInfoByType Windows Media Player
- Metodo getItemInfoByType Windows Media Player, classe media
- Media class Media Player Windows, metodo getItemInfoByType
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
ms.openlocfilehash: bc2aff2bee7641075bbac1dd04526ee751ea077a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332549"
---
# <a name="mediagetiteminfobytype-method"></a>Media. getItemInfoByType, metodo

Il metodo **getItemInfoByType** Recupera il valore dell'attributo corrispondente al nome dell'attributo, alla lingua e all'indice specificati.

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

*nome* \[ in\]
</dt> <dd>

**Stringa** contenente il nome dell'attributo. Per informazioni sugli attributi supportati da Windows Media Player, vedere la Guida di [riferimento](attribute-reference.md)agli attributi di Windows Media Player.

</dd> <dt>

*lingua* \[ di in\]
</dt> <dd>

**Stringa** che rappresenta la lingua. Se il valore è impostato su null o su "" (stringa vuota) viene utilizzata la stringa delle impostazioni locali corrente. In caso contrario, il valore deve essere una stringa di linguaggio RFC 1766 valida, ad esempio "en-US".

</dd> <dt>

*Indice* \[ di in\]
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
| Tutti gli altri attributi        | **Stringa**                     |



 

Per gli attributi il cui valore sottostante è **booleano**, questo metodo restituisce la stringa "true" o "false".

## <a name="remarks"></a>Commenti

Questo metodo recupera i metadati per un singolo elemento multimediale digitale o un elemento multimediale che fa parte di una playlist.

Questo metodo supporta attributi con più valori e attributi con valori complessi. Il metodo **GetItemInfo** non supporta attributi con più valori e attributi con valori complessi.

La proprietà **attributeCount** contiene il numero di nomi di attributi disponibili per un determinato oggetto **multimediale** . I numeri di indice possono quindi essere usati con il metodo **GetAttribute** per determinare il nome di ogni attributo disponibile. I singoli nomi di attributo possono essere passati al parametro *Name* di **getItemInfoByType**.

Il metodo **getAttributeCountByType** restituisce il numero di attributi che corrispondono a un nome di attributo specifico per un determinato oggetto **multimediale** . I numeri di indice possono quindi essere passati al parametro di *Indice* di **getItemInfoByType**. Questa operazione è utile quando un elemento multimediale digitale è stato categorizzato in più generi, ad esempio.

Per usare questo metodo, è necessario l'accesso in lettura alla libreria. Per altre informazioni, vedere [accesso alla libreria](library-access.md).

Questo metodo può causare errori. Quando si chiama questo metodo, è necessario includere il codice di gestione degli errori. In JScript, ad esempio, è possibile implementare la gestione degli errori usando il **try... rileva... Infine** , struttura.

**Windows Media Player 10 Mobile:** Questo metodo non è supportato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player 9 serie o versione successiva.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto multimediale**](media-object.md)
</dt> <dt>

[**Media. attributeCount**](media-attributecount.md)
</dt> <dt>

[**Media. getAttributeCountByType**](media-getattributecountbytype.md)
</dt> <dt>

[**Media. GetAttribute**](media-getattributename.md)
</dt> <dt>

[**Media. getItemInfo**](media-getiteminfo.md)
</dt> <dt>

[**Media. setItemInfo**](media-setiteminfo.md)
</dt> <dt>

[**Oggetto MetadataPicture**](metadatapicture-object.md)
</dt> <dt>

[**Oggetto MetadataText**](metadatatext-object.md)
</dt> <dt>

[**Lettura di valori di attributo**](reading-attribute-values.md)
</dt> <dt>

[**Settings. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





