---
title: ClosedCaption.SAMIStyle
description: La proprietà SAMIStyle specifica o recupera lo stile di sottotitoli codificati.
ms.assetid: 5535fb31-f1c0-49c4-b758-df74964b1e67
keywords:
- ClosedCaption.SAMIStyle Windows Media Player
topic_type:
- apiref
api_name:
- ClosedCaption.SAMIStyle
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6bd45977e3d433239e74aee21def913b640fad12
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122882174"
---
# <a name="closedcaptionsamistyle"></a>ClosedCaption.SAMIStyle

La **proprietà SAMIStyle** specifica o recupera lo stile di sottotitoli codificati.

``` syntax
player.closedCaption.SAMIStyle
```

## <a name="possible-values"></a>Valori possibili

Questa proprietà è una stringa di **lettura/scrittura.**

## <a name="remarks"></a>Commenti

Un file SAMI può contenere diverse definizioni di stile di formato. Gli stili SAMI vengono definiti tra &lt; i tag STYLE e nel file &gt; </STYLE> SAMI. Uno stile viene definito con una stringa di testo preceduta da un \# carattere. Ad esempio:


```
#Emphasis1 {Name: Big Bold Italic; font-size: 14pt; text-align: center;
            color: blue; font-family: sans-serif; font-weight: bold;
            font-style: italic;}

```



Specifica uno stile che produce un tipo di carattere specifico.

Se non viene specificato alcuno stile SAMI, per impostazione predefinita viene usato il primo stile definito nel file SAMI.

**Windows Media Player 10 Mobile:** Questa proprietà è di sola lettura e restituisce sempre una stringa vuota.

## <a name="examples"></a>Esempio

Nell'JScript seguente viene creato un elemento HTML SELECT che usa *closedCaption*. **SAMIStyle per** modificare l'aspetto del testo del sottotitolo codificato. **L'oggetto** Player è stato creato con ID = "Player".


```JScript
<!-- Create the SELECT element. -->
<SELECT ID = CCMode  NAME = "CCMode"  LANGUAGE = "JScript"

       /* Change the text style when the SELECT element changes. */
        onChange = "Player.closedCaption.SAMIStyle = CCMode.value;
        ">

       /* Fill the SELECT list with options, set the default to Strong. */
        <OPTION VALUE = "Normal">Normal
        <OPTION VALUE = "Small">Small 
        <OPTION VALUE = "Big Bold Italic" SELECTED>Strong
</SELECT>

```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Aggiunta di sottotitoli codificati ai supporti digitali**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**Oggetto ClosedCaption**](closedcaption-object.md)
</dt> </dl>

 

 





