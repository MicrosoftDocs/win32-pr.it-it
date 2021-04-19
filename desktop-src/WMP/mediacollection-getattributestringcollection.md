---
title: Mediacollection. getAttributeStringCollection, metodo
description: Il metodo getAttributeStringCollection recupera un oggetto StringCollection che rappresenta il set di tutti i valori di un attributo specificato all'interno di un tipo di supporto specificato.
ms.assetid: 75563a75-88f5-419e-983b-d105bce02511
keywords:
- Metodo getAttributeStringCollection Windows Media Player
- Metodo getAttributeStringCollection Windows Media Player, classe Mediacollection
- Mediacollection (classe) Windows Media Player, metodo getAttributeStringCollection
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
ms.openlocfilehash: 3d50d25488a05e6076c99802ce738edf02298ade
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330352"
---
# <a name="mediacollectiongetattributestringcollection-method"></a>Mediacollection. getAttributeStringCollection, metodo

Il metodo **getAttributeStringCollection** recupera un oggetto **StringCollection** che rappresenta il set di tutti i valori di un attributo specificato all'interno di un tipo di supporto specificato.

## <a name="syntax"></a>Sintassi


```JScript
retVal = MediaCollection.getAttributeStringCollection(
  attribute,
  mediaType
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*attributo* \[ in\]
</dt> <dd>

**Stringa** che specifica l'attributo.

</dd> <dt>

*mediaType* \[ in\]
</dt> <dd>

**Stringa** che rappresenta il tipo di supporto. Contiene uno dei valori seguenti: "audio", "video", "playlist" o "other".

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce un oggetto **StringCollection** .

## <a name="remarks"></a>Commenti

Per usare questo metodo, è necessario l'accesso in lettura alla libreria. Per altre informazioni, vedere [accesso alla libreria](library-access.md).

Per informazioni sugli attributi supportati da Windows Media Player, vedere la sezione [riferimento all'attributo](attribute-reference.md) .

## <a name="examples"></a>Esempio

Nell'esempio JScript seguente viene utilizzato *mediacollection*. **getAttributeStringCollection** per visualizzare un elenco di valori che corrispondono a un particolare attributo per gli elementi audio nell'insieme di supporti. Un elemento HTML SELECT, creato con ID = "Attribute", consente all'utente di selezionare un attributo, ad esempio artista, genere o album. Un elemento TEXTAREA HTML, creato con ID = "AttributeVals", Visualizza il risultato. L'oggetto **Player** è stato creato con ID = "Player".


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
| Versione<br/> | Windows Media Player versione 7,0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Mediacollection (oggetto)**](mediacollection-object.md)
</dt> <dt>

[**Settings. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> <dt>

[**StringCollection (oggetto)**](stringcollection-object.md)
</dt> </dl>

 

 





