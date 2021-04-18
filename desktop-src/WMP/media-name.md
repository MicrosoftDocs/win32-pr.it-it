---
title: Media.name
description: La proprietà Name specifica o Recupera il nome dell'elemento multimediale.
ms.assetid: 68aba78a-86fd-4411-9ac4-58f38d915e2c
keywords:
- Media Player Windows Media.name
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
ms.openlocfilehash: 9de8095d88c3ddec9049e0b43461adcf5553ec74
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329306"
---
# <a name="medianame"></a>Media.name

La proprietà **Name** specifica o Recupera il nome dell'elemento multimediale.

## <a name="syntax"></a>Sintassi

*Player*. *currentMedia*. **nome**

## <a name="possible-values"></a>Valori possibili

Questa proprietà è una **stringa** di lettura/scrittura contenente il nome dell'elemento multimediale.

## <a name="remarks"></a>Commenti

Per recuperare il valore di questa proprietà, è necessario l'accesso in lettura alla libreria. Per specificare il valore di questa proprietà, è necessario l'accesso completo alla libreria. Per altre informazioni, vedere [accesso alla libreria](library-access.md).

Prima di utilizzare questo metodo per specificare il nome di un elemento multimediale, utilizzare **isReadOnlyItem** per determinare se è possibile impostare il nome.

**Windows Media Player 10 Mobile:** Questa proprietà è di sola lettura.

## <a name="examples"></a>Esempio

Nell'esempio JScript seguente viene usato il *supporto*. **nome** per modificare il nome dell'elemento multimediale corrente. Un elemento input di testo HTML denominato NameText consente all'utente di immettere una stringa di testo per il nuovo nome. L'oggetto **Player** è stato creato con ID = "Player".


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
| Versione<br/> | Windows Media Player versione 7,0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto multimediale**](media-object.md)
</dt> <dt>

[**Settings. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





