---
title: Media.name
description: La proprietà name specifica o recupera il nome dell'elemento multimediale.
ms.assetid: 68aba78a-86fd-4411-9ac4-58f38d915e2c
keywords:
- Media.name Windows Media Player
topic_type:
- apiref
api_name:
- Media.name
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3abe6df00b5674cfbd443a5838b208814e30c5ecf75875586907314fc3a39d9f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119616857"
---
# <a name="medianame"></a>Media.name

La **proprietà name** specifica o recupera il nome dell'elemento multimediale.

## <a name="syntax"></a>Sintassi

*lettore*. *currentMedia*. **name**

## <a name="possible-values"></a>Valori possibili

Questa proprietà è una stringa di **lettura/scrittura** contenente il nome dell'elemento multimediale.

## <a name="remarks"></a>Commenti

Per recuperare il valore di questa proprietà, è necessario l'accesso in lettura alla libreria. Per specificare il valore di questa proprietà, è necessario l'accesso completo alla libreria. Per altre informazioni, vedere [Accesso alla libreria](library-access.md).

Prima di usare questo metodo per specificare il nome di un elemento multimediale, usare **isReadOnlyItem** per determinare se è possibile impostare il nome.

**Windows Media Player 10 Mobile:** Questa proprietà è di sola lettura.

## <a name="examples"></a>Esempio

Nell'esempio JScript seguente viene utilizzato *Media*. **name** per modificare il nome dell'elemento multimediale corrente. Un elemento di input HTML TEXT denominato NameText consente all'utente di immettere una stringa di testo per il nuovo nome. **L'oggetto** Player è stato creato con ID = "Player".


```JScript
<!<entity type="mdash"/>-Create an HTML BUTTON element to execute the name change. -->
<INPUT type = "BUTTON"  id = "NewName"  name = "NewName"  value = "Change Name" 
    onClick = "

        /* Store the current media item. */
        var cm = Player.currentMedia;

        /* Change the name. */
        cm.name = NameText.value;
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

[**Impostazioni.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Impostazioni.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





