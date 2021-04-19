---
title: TESTO. wordWrap
description: L'attributo wordWrap specifica o recupera un valore che indica se il ritorno a capo automatico è abilitato o disabilitato.
ms.assetid: 3bb127d8-42f1-4167-986a-d41690cb5647
keywords:
- Media Player di Windows TEXT. wordWrap
topic_type:
- apiref
api_name:
- TEXT.wordWrap
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff2b4d030a7e9efdda1bc7503ae3bf8eb5985401
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331849"
---
# <a name="textwordwrap"></a>TESTO. wordWrap

L'attributo **WordWrap** specifica o recupera un valore che indica se il ritorno a capo automatico è abilitato o disabilitato.

``` syntax
        elementID.wordWrap
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è un **valore booleano** di lettura/scrittura.



| Valore | Descrizione                                                                                       |
|-------|---------------------------------------------------------------------------------------------------|
| true  | Ritorno a capo automatico abilitato.                                                                             |
| false | Valore predefinito. Ritorno a capo automatico disabilitato. Se il testo non rientra nel controllo, il testo viene ritagliato. |



 

## <a name="remarks"></a>Commenti

Il controllo testo non divide le parole. Se una parola si estende oltre la larghezza del controllo, viene utilizzato il ritorno a capo automatico per spostare la parola nella riga successiva. Se una singola parola supera la larghezza del controllo, tale parola viene ritagliata e occupa una sola riga.

Se l'attributo **Width** non è specificato, **WordWrap** viene ignorato e il controllo di testo verrà ridimensionato anziché racchiudere il testo.

Se si desiderano interruzioni di riga in posizioni particolari, è necessario specificare in modo esplicito il **valore** utilizzando "&\# 13;" o " \\ r". Se il secondo formato viene usato quando si specifica direttamente il valore, la stringa deve essere preceduta da "JScript:" e il valore effettivo deve essere racchiuso tra virgolette singole, come illustrato di seguito. Questa operazione non è necessaria se il valore viene impostato dinamicamente dall'interno di un gestore eventi.

Se **WordWrap** è impostato su true e la **Descrizione comando** non è specificata, la descrizione comando visualizzerà il testo completo dell'attributo **value** . Se non si desidera alcuna descrizione comando, impostare **ToolTip** su "" (stringa vuota).

## <a name="examples"></a>Esempio


```C++
<THEME>
  <VIEW>
    <TEXT
      width = "50"
      height = "200"
      wordWrap = "true"
      backgroundColor = "blue"
      foregroundColor = "white"
      value = "This is a test.&#13;&#13;It is only a test."
    />
    <TEXT
      width = "50"
      height = "200"
      left = "100"
      wordWrap = "true"
      backgroundColor = "green"
      foregroundColor = "white"
      value = "JScript:'This is a test.\r\rIt is only a test.'"
    />
  </VIEW>
</THEME>

```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**AmbientAttributes. Width**](ambientattributes-width.md)
</dt> <dt>

[**Elemento TEXT**](text-element.md)
</dt> <dt>

[**TESTO. toolTip**](text-tooltip.md)
</dt> <dt>

[**TEXT. Value**](text-value.md)
</dt> </dl>

 

 





