---
title: TEXT. Value
description: L'attributo value specifica o Recupera il testo visualizzato nel controllo di testo.
ms.assetid: dbc50be2-ee18-4661-a343-9e906879aba0
keywords:
- Media Player di Windows TEXT. Value
topic_type:
- apiref
api_name:
- TEXT.value
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d87f688f7afffeb588a37ac13ebff4cdc7cc105
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327482"
---
# <a name="textvalue"></a>TEXT. Value

L'attributo **value** specifica o Recupera il testo visualizzato nel controllo di testo.

``` syntax
        elementID.value
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è una **stringa** di lettura/scrittura.

## <a name="remarks"></a>Commenti

Se la larghezza del controllo di testo non è sufficiente per contenere il testo specificato, il testo viene ritagliato e vengono visualizzati i puntini di sospensione per illustrare il fatto. Se l'attributo **ToolTip** non è stato impostato, il testo completo verrà visualizzato come descrizione comando quando il cursore passa il puntatore del mouse sul controllo.

Se non viene specificata una larghezza, la larghezza predefinita per il controllo corrisponde a quella della stringa.

Se l'altezza del controllo non è specificata, l'altezza predefinita è una riga.

Se l'attributo **WordWrap** è impostato su true e l'altezza del controllo è sufficiente per contenere un'altra riga di testo, il testo viene incapsulato in una riga successiva. Il wrapping si verifica solo tra le parole. È anche possibile forzare le interruzioni di riga, come descritto in **WordWrap**.

## <a name="examples"></a>Esempio

L'esempio seguente è un file di definizione dell'interfaccia completa che illustra come vengono usati gli attributi dell'elemento di **testo** . Si trova nella directory degli esempi installata con l'SDK.


```C++
<THEME>
  <VIEW
    height = "175"
  >
    <TEXT 
      width = "150"
      fontSize = "30"
      hoverFontStyle = "Bold"
      hoverForegroundColor = "red"
      disabledForegroundColor = "#CCCCCC"
      justification = "Center"
      value = "Play"
      cursor = "hand"
      enabled = "wmpenabled:player.controls.play"
      onClick = "JScript: player.URL='https://proseware.com/laure.wma';"
    />
    <TEXT
      top = "50"
      width = "150"
      fontSize = "30"
      hoverFontStyle = "Bold"
      hoverForegroundColor = "red"
      disabledForegroundColor = "#CCCCCC"
      justification = "Center"
      value = "Stop"
      cursor = "hand"
      enabled = "wmpenabled:player.controls.stop"
      onClick = "JScript: player.controls.stop();"
    />
    <TEXT
      top = "100"
      width = "150"
      fontSize = "30"
      hoverFontStyle = "Bold"
      hoverForegroundColor = "red"
      justification = "Center"
      value = "Close"
      cursor = "hand"
      onClick = "JScript: view.close();"
    />
    <TEXT
      top = "30"
      left = "120"
      width = "200"
      fontSize = "20"
      fontStyle = "Underline"
      justification = "Center"
      value = "Volume"
    />
    <TEXT
      top = "60"
      left = "120"
      width = "200"
      fontSize = "40"
      justification = "Center"
      value = "wmpprop:player.settings.volume"
    />
    <TEXT
      top = "65"
      left = "142"
      width = "40"
      fontSize = "30"
      hoverFontStyle = "Bold"
      hoverForegroundColor = "red"
      justification = "Center"
      value = "-"
      cursor = "hand"
      toolTip = "decrease volume"
      onClick = "player.settings.volume = player.settings.volume - 5"
    />
    <TEXT
      top = "65"
      left = "260"
      width = "40"
      fontSize = "30"
      hoverFontStyle = "Bold"
      hoverForegroundColor = "red"
      justification = "Center"
      value = "+"
      cursor = "hand"
      toolTip = "increase volume"
      onClick = "player.settings.volume = player.settings.volume + 5"
    />
    <TEXT
      top = "155"
      width = "300"
      height = "30"
      fontFace = "System"
      backgroundColor = "blue"
      foregroundColor = "white"
      justification = "Center"
      scrolling = "true"
      scrollingAmount = "1"
      scrollingDelay = "50"
      value = "wmpprop:player.status"
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

[**Elemento TEXT**](text-element.md)
</dt> <dt>

[**TESTO. toolTip**](text-tooltip.md)
</dt> <dt>

[**TESTO. wordWrap**](text-wordwrap.md)
</dt> </dl>

 

 





