---
title: TEXT.value
description: L'attributo value specifica o recupera il testo visualizzato nel controllo Text.
ms.assetid: dbc50be2-ee18-4661-a343-9e906879aba0
keywords:
- Text.value Windows Media Player
topic_type:
- apiref
api_name:
- TEXT.value
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8eef6b17428831a52a0e3cf5b8f8ec3dd7f795d5d4b78e2c4700a6274b877820
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119762861"
---
# <a name="textvalue"></a>TEXT.value

**L'attributo** value specifica o recupera il testo visualizzato nel controllo Text.

``` syntax
        elementID.value
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è una stringa di **lettura/scrittura.**

## <a name="remarks"></a>Commenti

Se la larghezza del controllo Testo non è sufficiente per contenere il testo fornito, il testo viene ritagliato e vengono visualizzati i puntini di sospensione per illustrare il fatto. Se **l'attributo toolTip** non è stato impostato, il testo completo verrà visualizzato come descrizione comando quando il cursore viene posizionato sul controllo.

Se non viene specificata una larghezza, la larghezza predefinita per il controllo è la larghezza della stringa.

Se l'altezza del controllo non è specificata, l'altezza predefinita è una riga.

Se **l'attributo wordWrap** è impostato su true e l'altezza del controllo è sufficiente per contenere un'altra riga di testo, il testo va a capo in una riga successiva. Il ritorno a capo si verifica solo tra le parole. È anche possibile forzare le interruzioni di riga, come illustrato in **wordWrap**.

## <a name="examples"></a>Esempio

L'esempio seguente è un file di definizione dell'interfaccia completo che illustra come vengono usati **gli** attributi dell'elemento TEXT. È disponibile nella directory Samples installata con l'SDK.


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
| Versione<br/> | Windows Media Player versione 7.0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento TEXT**](text-element.md)
</dt> <dt>

[**TEXT.toolTip**](text-tooltip.md)
</dt> <dt>

[**TEXT.wordWrap**](text-wordwrap.md)
</dt> </dl>

 

 





