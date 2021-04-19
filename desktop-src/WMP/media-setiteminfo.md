---
title: Media. setItemInfo, metodo
description: Il metodo setItemInfo imposta il valore dell'attributo specificato per l'elemento multimediale corrente.
ms.assetid: 8c4ce954-45cb-4a67-9660-1a013ecd64c3
keywords:
- Metodo setItemInfo Windows Media Player
- Metodo setItemInfo Windows Media Player, classe media
- Media class Media Player Windows, metodo setItemInfo
topic_type:
- apiref
api_name:
- Media.setItemInfo
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b918e6a388cab750cc379611f5f55c6a1b1d256c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330362"
---
# <a name="mediasetiteminfo-method"></a>Media. setItemInfo, metodo

Il metodo **setItemInfo** imposta il valore dell'attributo specificato per l'elemento multimediale corrente.

## <a name="syntax"></a>Sintassi


```JScript
Media.setItemInfo(
  attribute,
  value
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*attributo* \[ in\]
</dt> <dd>

**Stringa** contenente il nome dell'attributo. Per informazioni sugli attributi supportati da Windows Media Player, vedere la Guida di [riferimento](attribute-reference.md)agli attributi di Windows Media Player.

</dd> <dt>

*valore* \[ di in\]
</dt> <dd>

**Stringa** che contiene il nuovo valore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

La proprietà **attributeCount** contiene il numero di attributi disponibili per un determinato oggetto **multimediale** . I numeri di indice possono quindi essere usati con il metodo **GetAttribute** per determinare i nomi degli attributi predefiniti che possono essere usati con questo metodo.

Prima di usare questo metodo, usare il metodo **isReadOnlyItem** per determinare se è possibile impostare un particolare attributo.

Per usare questo metodo, è necessario l'accesso completo alla libreria. Per altre informazioni, vedere [accesso alla libreria](library-access.md).

**Nota**

Se si incorpora il controllo Windows Media Player nell'applicazione, gli attributi di file modificati non verranno scritti nel file multimediale digitale fino a quando l'utente non esegue Windows Media Player. Se si usa il controllo in un'applicazione remota scritta in C++, gli attributi di file che vengono modificati verranno scritti nel file multimediale digitale subito dopo aver apportato le modifiche. In entrambi i casi, le modifiche sono immediatamente disponibili per il codice tramite la libreria.

**Windows Media Player 10 Mobile:** Questo metodo non è implementato.

## <a name="examples"></a>Esempio

Nell'esempio JScript seguente viene usato il *supporto*. **setItemInfo** per modificare il valore dell'attributo genre per l'elemento multimediale corrente. Un elemento input di testo HTML denominato genText consente all'utente di immettere una stringa di testo, che viene quindi usata per modificare le informazioni sugli attributi. L'oggetto **Player** è stato creato con ID = "Player".


```JScript
<!-- Create the button element. -->
<INPUT type = "BUTTON"  id = "NEWGEN"  name = "NEWGEN"  value = "Change Genre" 
onClick = "
    /* Store the current media item. */
    var cm = Player.currentMedia;

    /* Get the user input from the text box. */
    var atValue = genText.value;

    /* Test for read-only status of the attribute. */
    if(cm.isReadOnlyItem('Genre') == false){

        /* Change the attribute value. */
        cm.setItemInfo('Genre' ,atValue);
    } 
">

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

[**Media. getItemInfo**](media-getiteminfo.md)
</dt> <dt>

[**Media. isReadOnlyItem**](media-isreadonlyitem.md)
</dt> <dt>

[**Settings. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





