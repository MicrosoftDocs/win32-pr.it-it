---
title: Media. GetAttribute (metodo)
description: Il metodo GetAttribute Recupera il nome dell'attributo corrispondente all'indice specificato.
ms.assetid: f74d81c6-49f8-4b1e-a367-acb4a0914c5a
keywords:
- Metodo GetAttributeName Windows Media Player
- Metodo GetAttribute Media Player Windows, classe media
- Media class Media Player Windows, metodo GetAttribute
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
ms.openlocfilehash: d7134b68837a7a5d1b765c64320ae68c56c6fc56
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326123"
---
# <a name="mediagetattributename-method"></a>Media. GetAttribute (metodo)

Il metodo **GetAttribute** Recupera il nome dell'attributo corrispondente all'indice specificato.

## <a name="syntax"></a>Sintassi


```JScript
strRetVal = Media.getAttributeName(
  index
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Indice* \[ di in\]
</dt> <dd>

**Numero** (**Long**) che contiene l'indice dell'attributo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce una **stringa** che specifica il nome dell'attributo.

## <a name="remarks"></a>Commenti

Il nome dell'attributo restituito può essere utilizzato insieme a **GetItemInfo** per recuperare il valore per un attributo denominato specifico.

Per usare questo metodo, è necessario l'accesso in lettura alla libreria. Per altre informazioni, vedere [accesso alla libreria](library-access.md).

Per informazioni sugli attributi supportati da Windows Media Player, vedere le informazioni di [riferimento sull'attributo](attribute-reference.md)Windows Media Player.

**Windows Media Player 10 Mobile:** Gli attributi per un elemento multimediale sono disponibili solo durante la riproduzione, a meno che non vengano recuperati dall'elemento tramite la raccolta di supporti.

## <a name="examples"></a>Esempio

Nell'esempio JScript seguente viene usato il *supporto*. **GetAttribute** per riempire un'area di testo HTML denominata text con l'indice e il nome di ogni attributo per l'elemento multimediale corrente. L'oggetto **Player** è stato creato con ID = "Player".


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
| Versione<br/> | Windows Media Player versione 7,0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto multimediale**](media-object.md)
</dt> <dt>

[**Media. attributeCount**](media-attributecount.md)
</dt> <dt>

[**Media. getItemInfo**](media-getiteminfo.md)
</dt> <dt>

[**Settings. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





