---
title: Metodo MediaCollection.getAttributeStringCollection
description: Il metodo getAttributeStringCollection recupera un oggetto StringCollection che rappresenta il set di tutti i valori per un attributo specificato all'interno di un tipo di supporto specificato.
ms.assetid: 75563a75-88f5-419e-983b-d105bce02511
keywords:
- Metodo getAttributeStringCollection Windows Media Player
- Metodo getAttributeStringCollection Windows Media Player , classe MediaCollection
- Classe MediaCollection Windows Media Player metodo , getAttributeStringCollection
topic_type:
- apiref
api_name:
- MediaCollection.getAttributeStringCollection
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c27b7c6dbef585763ecfda1abdc7beadfa3d883476033424ff868a3d56c4bb96
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996301"
---
# <a name="mediacollectiongetattributestringcollection-method"></a>Metodo MediaCollection.getAttributeStringCollection

Il **metodo getAttributeStringCollection** recupera un **oggetto StringCollection** che rappresenta il set di tutti i valori per un attributo specificato all'interno di un tipo di supporto specificato.

## <a name="syntax"></a>Sintassi


```JScript
retVal = MediaCollection.getAttributeStringCollection(
  attribute,
  mediaType
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*attributo* \[ Pollici\]
</dt> <dd>

**Stringa** che specifica l'attributo.

</dd> <dt>

*mediaType* \[ Pollici\]
</dt> <dd>

**Stringa** che rappresenta il tipo di supporto. Contiene uno dei valori seguenti: "Audio", "Video", "Playlist" o "Other".

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce un **oggetto StringCollection.**

## <a name="remarks"></a>Commenti

Per usare questo metodo, è necessario l'accesso in lettura alla libreria. Per altre informazioni, vedere [Accesso alla libreria](library-access.md).

Per informazioni sugli attributi supportati da Windows Media Player, vedere la [sezione Informazioni di riferimento sugli](attribute-reference.md) attributi.

## <a name="examples"></a>Esempio

Nell'JScript seguente viene utilizzato *MediaCollection*. **getAttributeStringCollection** per visualizzare un elenco di valori che corrispondono a un attributo specifico per gli elementi audio nella raccolta multimediale. Un elemento HTML SELECT, creato con ID = "Attribute", consente all'utente di selezionare un attributo, ad esempio Artist, Genre o Album. Un elemento HTML TEXTAREA, creato con ID = "AttributeVals", visualizza il risultato. **L'oggetto** Player è stato creato con ID = "Player".


```JScript
// Clear the text in the display area.
AttributeVals.value = "";

// Store the mediaCollection object.
var library = Player.mediaCollection;

// Get the string collection for the attribute type the user selects.
var all = library.getAttributeStringCollection(Attribute.value, "Audio");

// Loop through the string collection.
for (i = 0; i < all.count; i++){

    // Display the items one line at a time.
    AttributeVals.value += all.item(i);
    AttributeVals.value += "\n";
}

```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto MediaCollection**](mediacollection-object.md)
</dt> <dt>

[**Impostazioni.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Impostazioni.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> <dt>

[**Oggetto StringCollection**](stringcollection-object.md)
</dt> </dl>

 

 





