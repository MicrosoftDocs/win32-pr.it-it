---
title: ClosedCaption.SAMILang
description: La proprietà SAMILang specifica o recupera la lingua visualizzata per la didascalia chiusa.
ms.assetid: 990fb180-cb37-4022-b236-03f5acfd3ad3
keywords:
- Media Player Windows ClosedCaption. SAMILang
topic_type:
- apiref
api_name:
- ClosedCaption.SAMILang
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae99b9a164e29b4adeb2fd7b23a1b79945dcb26e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326730"
---
# <a name="closedcaptionsamilang"></a>ClosedCaption.SAMILang

La proprietà **SAMILang** specifica o recupera la lingua visualizzata per la didascalia chiusa.

``` syntax
player.closedCaption.SAMILang
```

## <a name="possible-values"></a>Valori possibili

Questa proprietà è una **stringa** di lettura/scrittura.

## <a name="remarks"></a>Commenti

Un file SAMI può contenere testo per una o più lingue. Le lingue disponibili per la didascalia chiusa sono definite tra i tag <STYLE> e </STYLE> nel file Sami. Un identificatore di lingua viene specificato con una stringa alfanumerica univoca preceduta da un punto (.). Il nome specificato per una lingua può essere qualsiasi stringa. È ad esempio possibile utilizzare il codice seguente per definire l'inglese (Stati Uniti):


```
.ENUSCC {Name:'English Captions' lang: en-US; SAMIType:CC;}

```



Se non si specifica alcun linguaggio SAMI, per impostazione predefinita viene usata la prima lingua definita nel file SAMI.

Valore passato utilizzando *ClosedCaption*. **SAMILang** deve corrispondere all'attributo **Name** nell'identificatore di linguaggio.

**Windows Media Player 10 Mobile:** Questa proprietà è di sola lettura e restituisce sempre una stringa vuota.

## <a name="examples"></a>Esempio

Nell'esempio JScript seguente viene usato *ClosedCaption*. **SAMILang** in un elemento HTML SELECT per specificare la lingua del titolo closed. L'oggetto **Player** è stato creato con ID = "Player".


```JScript
<!-- Create the SELECT element. -->
<SELECT ID = CCLANG  NAME = "CCLANG"  LANGUAGE = "JScript"

     /* Set the closed caption language when the SELECT element changes. */
        onChange = "Player.closedCaption.SAMILang = CCLANG.value;
        ">

        /* Fill in the SELECT element options. */
           <OPTION VALUE = "'Spanish Captions'">Spanish
           <OPTION VALUE = "'Japanese Captions'">Japanese
           <OPTION VALUE = "'English Captions'">English
           <OPTION VALUE = "'French Captions'">French
           <OPTION VALUE = "'German Captions'" SELECTED>German
</SELECT>

```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Aggiunta di didascalie chiuse a file multimediali digitali**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**Oggetto ClosedCaption**](closedcaption-object.md)
</dt> </dl>

 

 





