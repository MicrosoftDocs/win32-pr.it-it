---
title: Gestione degli eventi in una pagina Web visualizzata da Firefox
description: Gestione degli eventi in una pagina Web visualizzata da Firefox
ms.assetid: 361c46ff-36e2-4497-a511-86b0439e9437
keywords:
- Windows Media Player, incorporamento del controllo ActiveX
- Modello a oggetti di Windows Media Player, incorporamento del controllo ActiveX
- modello a oggetti, incorporamento del controllo ActiveX
- Windows Media Player Mobile, incorporamento del controllo ActiveX
- Controllo ActiveX di Windows Media Player, incorporamento
- Controllo ActiveX Windows Media Player Mobile, incorporamento
- Controllo ActiveX, incorporamento
- Controllo ActiveX di Windows Media Player, pagine Web
- Controllo ActiveX Windows Media Player Mobile, pagine Web
- Controllo ActiveX, pagine Web
- Controllo ActiveX Windows Media Player, gestione eventi
- Controllo ActiveX Windows Media Player Mobile, gestione eventi
- Controllo ActiveX, gestione eventi
- incorporamento, pagine Web
- Incorporamento di pagine Web, gestione degli eventi
- Windows Media Player, Firefox
- Modello a oggetti di Windows Media Player, Firefox
- modello a oggetti, Firefox
- Windows Media Player Mobile, Firefox
- Controllo ActiveX di Windows Media Player, Firefox
- Controllo ActiveX Windows Media Player Mobile, Firefox
- Controllo ActiveX, Firefox
- Firefox, gestione degli eventi
- Incorporamento di pagine Web, Firefox
- eventi, Firefox
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b9659d1920ffc4d5e39f4cd44e15e24b08f6ddc
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/21/2019
ms.locfileid: "104332876"
---
# <a name="handling-events-in-a-web-page-displayed-by-firefox"></a>Gestione degli eventi in una pagina Web visualizzata da Firefox

Quando si incorpora il controllo Windows Media Player in una pagina Web, è possibile scrivere uno script che gestisce gli eventi. Per un elenco degli eventi generati dal controllo Player, vedere [oggetto Player](player-object.md).

Se il tipo MIME associato a un controllo Player incorporato è application/x-ms-WMP, è possibile scrivere i gestori eventi che hanno il formato seguente:


```HTML
<SCRIPT for="Player" language="jscript" event="EventName(Params)">
  ...
</SCRIPT>
```



dove *EventName* è il nome di un evento Windows Media Player e *params* è un elenco dei parametri dell'evento. Il codice seguente, ad esempio, ha un gestore per l'evento [PlayStateChange](player-player-playstatechange.md) .


```HTML
<OBJECT id="Player" type="application/x-ms-wmp" width="300" height="200">
  <PARAM name="URL" value="c:\MediaFiles\Seattle.wmv"/>
</OBJECT>

<P id="p1">...</P>

<SCRIPT for="Player" event="PlayStateChange(NewState)">
  document.getElementById("p1").innerHTML = "Play state: " + NewState;
</SCRIPT>
```



Se si dispone di più istanze del controllo Player in una pagina Web e si usa il formato illustrato nell'esempio precedente, ogni gestore eventi è associato a un'istanza specifica del controllo Player. Nell'esempio precedente, il gestore eventi viene chiamato solo quando lo stato di riproduzione viene modificato per il controllo con ID = "Player".

Se il tipo MIME associato a un controllo Player incorporato non è application/x-ms-WMP, è possibile scrivere i gestori eventi che hanno il formato seguente:


```HTML
<SCRIPT language="jscript">
  function OnDSEventNameEvt(Params)
  {...}
</SCRIPT>
```



dove *EventName* è il nome di un evento Windows Media Player e *params* è un elenco dei parametri dell'evento. Il codice seguente, ad esempio, ha un gestore per l'evento **PlayStateChange** .


```HTML
<OBJECT id="Player" type="application/asx" width="300" height="200">
  <PARAM name="URL" value="c:\MediaFiles\Test.asx"/>
</OBJECT>

<P id="p1">...</P>

<SCRIPT>
  function OnDSPlayStateChangeEvt(NewState)
  {
    p1.innerHTML = "Play state: " + NewState;
  }
</SCRIPT>

```



Se si dispone di più istanze del controllo Player in una pagina Web e si usa il formato illustrato nell'esempio precedente, ogni gestore eventi è associato a tutte le istanze del controllo lettore e il gestore eventi viene chiamato quando lo stato di riproduzione per qualsiasi controllo del lettore nella pagina.

> [!Note]  
> Se il tipo MIME non è application/x-ms-WMP, l'evento **DoubleClick** viene inviato come OnDSDblClickEvt (non OnDSDoubleClickEvt) per la compatibilità con la versione 6,4 del controllo Player.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Uso del controllo Media Player Windows con Firefox**](using-the-windows-media-player-control-with-firefox.md)
</dt> </dl>

 

 




