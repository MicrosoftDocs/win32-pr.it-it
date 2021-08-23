---
title: Metodo Media.setItemInfo
description: Il metodo setItemInfo imposta il valore dell'attributo specificato per l'elemento multimediale corrente.
ms.assetid: 8c4ce954-45cb-4a67-9660-1a013ecd64c3
keywords:
- Metodo setItemInfo Windows Media Player
- Metodo setItemInfo Windows Media Player classe Media
- Classe media Windows Media Player, metodo setItemInfo
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
ms.openlocfilehash: b1639b86ce1e0643f3d6ce255e5ca492bc4fae0c1301e1a568a0c5609ceda2a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119647971"
---
# <a name="mediasetiteminfo-method"></a>Metodo Media.setItemInfo

Il **metodo setItemInfo** imposta il valore dell'attributo specificato per l'elemento multimediale corrente.

## <a name="syntax"></a>Sintassi


```JScript
Media.setItemInfo(
  attribute,
  value
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*attributo* \[ Pollici\]
</dt> <dd>

**Stringa** contenente il nome dell'attributo. Per informazioni sugli attributi supportati da Windows Media Player, vedere le informazioni di Windows Media Player [sugli attributi](attribute-reference.md).

</dd> <dt>

*value* \[ Pollici\]
</dt> <dd>

**Stringa** contenente il nuovo valore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

La **proprietà attributeCount** contiene il numero di attributi disponibili per un determinato **oggetto Media.** I numeri di indice possono quindi essere usati con il **metodo getAttributeName** per determinare i nomi degli attributi predefiniti che possono essere usati con questo metodo.

Prima di usare questo metodo, usare il **metodo isReadOnlyItem** per determinare se è possibile impostare un attributo specifico.

Per usare questo metodo, è necessario l'accesso completo alla libreria. Per altre informazioni, vedere [Accesso alla libreria](library-access.md).

**Nota**

Se si incorpora il controllo Windows Media Player nell'applicazione, gli attributi di file che si modificano non verranno scritti nel file multimediale digitale fino a quando l'utente non esegue Windows Media Player. Se si usa il controllo in un'applicazione remota scritta in C++, gli attributi di file che si modificano verranno scritti nel file multimediale digitale poco dopo aver apportato le modifiche. In entrambi i casi, le modifiche sono immediatamente disponibili per il codice tramite la libreria.

**Windows Media Player 10 Mobile:** Questo metodo non viene implementato.

## <a name="examples"></a>Esempio

Nell'esempio JScript seguente viene utilizzato *Media*. **setItemInfo per** modificare il valore dell'attributo Genre per l'elemento multimediale corrente. Un elemento di input HTML TEXT denominato genText consente all'utente di immettere una stringa di testo, che viene quindi usata per modificare le informazioni sull'attributo. **L'oggetto** Player è stato creato con ID = "Player".


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
| Versione<br/> | Windows Media Player versione 7.0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto multimediale**](media-object.md)
</dt> <dt>

[**Media.getItemInfo**](media-getiteminfo.md)
</dt> <dt>

[**Media.isReadOnlyItem**](media-isreadonlyitem.md)
</dt> <dt>

[**Impostazioni.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Impostazioni.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





