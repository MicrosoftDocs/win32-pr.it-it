---
title: Metodo Media.getAttributeName
description: Il metodo getAttributeName recupera il nome dell'attributo corrispondente all'indice specificato.
ms.assetid: f74d81c6-49f8-4b1e-a367-acb4a0914c5a
keywords:
- Metodo getAttributeName Windows Media Player
- Metodo getAttributeName Windows Media Player , classe Media
- Classe media Windows Media Player metodo , getAttributeName
topic_type:
- apiref
api_name:
- Media.getAttributeName
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b6b9a288830283b3711c6e4eb652be968979628af48d2ce5b718150b9018568
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120123431"
---
# <a name="mediagetattributename-method"></a>Metodo Media.getAttributeName

Il **metodo getAttributeName** recupera il nome dell'attributo corrispondente all'indice specificato.

## <a name="syntax"></a>Sintassi


```JScript
strRetVal = Media.getAttributeName(
  index
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*index* \[ Pollici\]
</dt> <dd>

**Numero** (**long**) contenente l'indice dell'attributo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce un **valore String** che specifica il nome dell'attributo.

## <a name="remarks"></a>Commenti

Il nome dell'attributo restituito può essere usato insieme a **getItemInfo** per recuperare il valore per un attributo denominato specifico.

Per usare questo metodo, è necessario l'accesso in lettura alla libreria. Per altre informazioni, vedere [Accesso alla libreria.](library-access.md)

Per informazioni sugli attributi supportati da Windows Media Player, vedere Windows Media Player [riferimento agli attributi.](attribute-reference.md)

**Windows Media Player 10 Mobile:** Gli attributi per un elemento multimediale sono disponibili solo durante la riproduzione, a meno che non vengano recuperati dall'elemento tramite la raccolta multimediale.

## <a name="examples"></a>Esempio

Nell'esempio JScript seguente viene utilizzato *Media*. **getAttributeName per** riempire un'area di testo HTML denominata myText con l'indice e il nome di ogni attributo per l'elemento multimediale corrente. **L'oggetto Player** è stato creato con ID = "Player".


```JScript
// Store the current media object.
var cm = Player.currentMedia;

// Get the number of attributes for the current media. 
var atCount = cm.attributeCount;

// Loop through the attribute list.
for(var i=0; i < atCount; i++){
   
   // Print each attribute index and name.   
   myText.value += "Attribute " + i +": ";
   myText.value += cm.getAttributeName(i);
   myText.value += "\n";
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

[**Media.attributeCount**](media-attributecount.md)
</dt> <dt>

[**Media.getItemInfo**](media-getiteminfo.md)
</dt> <dt>

[**Impostazioni.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Impostazioni.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





