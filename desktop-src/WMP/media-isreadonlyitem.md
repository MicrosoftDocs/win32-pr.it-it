---
title: Metodo Media.isReadOnlyItem
description: Il metodo isReadOnlyItem restituisce un valore che indica se l'attributo specificato dell'elemento multimediale può essere modificato.
ms.assetid: 5e398e76-f64a-45b5-9b4f-679c65e5a0d1
keywords:
- Metodo isReadOnlyItem Windows Media Player
- Metodo isReadOnlyItem Windows Media Player classe Media
- Classe media Windows Media Player metodo , isReadOnlyItem
topic_type:
- apiref
api_name:
- Media.isReadOnlyItem
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 501aacb7b9a56fd9780aba75a15aa9f717640ebff7619df020bad432cdffd459
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120123391"
---
# <a name="mediaisreadonlyitem-method"></a>Metodo Media.isReadOnlyItem

Il **metodo isReadOnlyItem** restituisce un valore che indica se l'attributo specificato dell'elemento multimediale può essere modificato.

## <a name="syntax"></a>Sintassi


```JScript
bRetVal = Media.isReadOnlyItem(
  attribute
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*attributo* \[ Pollici\]
</dt> <dd>

**Stringa** che indica il nome dell'attributo da testare. Per informazioni sugli attributi supportati da Windows Media Player, vedere il riferimento Windows Media Player [attributi](attribute-reference.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce un valore **booleano**.

## <a name="remarks"></a>Commenti

Se un attributo è di sola lettura, non può essere impostato con il **metodo setItemInfo.** Si noti che questo metodo può restituire valori diversi per un particolare attributo se usato con versioni diverse Windows Media Player.

Per usare questo metodo, è necessario l'accesso in lettura alla libreria. Per altre informazioni, vedere [Accesso alla libreria](library-access.md).

**Windows Media Player 10 Mobile:** Questa proprietà restituisce sempre **true.**

## <a name="examples"></a>Esempio

Nell'esempio JScript seguente viene *utilizzato Media*. **isReadOnlyItem per** riempire un elemento TEXTAREA HTML denominato rwText con informazioni sull'elemento multimediale corrente. Il codice restituisce ogni attributo dell'elemento multimediale corrente, insieme al testo che indica se l'attributo è di sola lettura o di lettura/scrittura. **L'oggetto** Player è stato creato con ID = "Player".


```JScript
// Store the current media item object.
var cm = Player.currentMedia;

// Create a variable to hold each attribute name.
var atName;

// Loop through the attribute list.
for(var i = 0; i < cm.attributeCount; i++){

   // Get the attribute name.
   atName = cm.getAttributeName(i);

   // Test whether the attribute is read-only.
   var test = ((cm.isReadOnlyItem(atName))?"Read-Only":"Read/Write");

// Print the attribute information to the text area.
   rwText.value += atName + " is " + test;
   rwText.value += "\n";
}

```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto multimediale**](media-object.md)
</dt> <dt>

[**Media.setItemInfo**](media-setiteminfo.md)
</dt> <dt>

[**Impostazioni.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Impostazioni.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





