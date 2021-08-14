---
title: ClosedCaption.SAMILang
description: La proprietà SAMILang specifica o recupera la lingua visualizzata per i sottotitoli codificati.
ms.assetid: 990fb180-cb37-4022-b236-03f5acfd3ad3
keywords:
- ClosedCaption.SAMILang Windows Media Player
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
ms.openlocfilehash: 4c423b041601a38e81b1c4e83c34c010edb3365a4eb7e05596038fa887818ba1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118342286"
---
# <a name="closedcaptionsamilang"></a>ClosedCaption.SAMILang

La **proprietà SAMILang** specifica o recupera la lingua visualizzata per i sottotitoli codificati.

``` syntax
player.closedCaption.SAMILang
```

## <a name="possible-values"></a>Valori possibili

Questa proprietà è una stringa di **lettura/scrittura.**

## <a name="remarks"></a>Commenti

Un file SAMI può contenere testo per una o più lingue. Le lingue disponibili per i sottotitoli codificati sono definite tra <STYLE> i tag </STYLE> e nel file SAMI. Un identificatore di lingua viene specificato con una stringa alfanumerica univoca preceduta da un punto (.). Il nome specificato per una lingua può essere qualsiasi stringa. Ad esempio, per definire l'inglese (Stati Uniti) è possibile usare quanto segue:


```
.ENUSCC {Name:'English Captions' lang: en-US; SAMIType:CC;}

```



Se non viene specificata alcuna lingua SAMI, per impostazione predefinita viene usata la prima lingua definita nel file SAMI.

Valore passato usando *ClosedCaption.* **SAMILang deve** corrispondere **all'attributo Name** nell'identificatore di lingua.

**Windows Media Player 10 Mobile:** Questa proprietà è di sola lettura e restituisce sempre una stringa vuota.

## <a name="examples"></a>Esempio

Nell'esempio JScript seguente viene *utilizzato ClosedCaption*. **SAMILang** in un elemento HTML SELECT per specificare la lingua del sottotitolo codificato. **L'oggetto Player** è stato creato con ID = "Player".


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
| Versione<br/> | Windows Media Player versione 7.0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Aggiunta di sottotitoli codificati a supporti digitali**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**Oggetto ClosedCaption**](closedcaption-object.md)
</dt> </dl>

 

 





