---
title: Gestione degli eventi in una pagina Web visualizzata da Firefox
description: Gestione degli eventi in una pagina Web visualizzata da Firefox
ms.assetid: 361c46ff-36e2-4497-a511-86b0439e9437
keywords:
- Windows Media Player,incorporamento ActiveX controllo
- Windows Media Player a oggetti, incorporamento ActiveX controllo
- modello a oggetti, incorporamento ActiveX controllo
- Windows Media Player Mobile, incorporamento ActiveX controllo
- Windows Media Player ActiveX, incorporamento
- Windows Media Player Controllo ActiveX per dispositivi mobili, incorporamento
- ActiveX, incorporamento
- Windows Media Player ActiveX, pagine Web
- Windows Media Player Controllo ActiveX per dispositivi mobili, pagine Web
- ActiveX, pagine Web
- Windows Media Player ActiveX, gestione degli eventi
- Windows Media Player Controllo ActiveX per dispositivi mobili, gestione degli eventi
- ActiveX, gestione degli eventi
- incorporamento, pagine Web
- incorporamento di pagine Web, gestione degli eventi
- Windows Media Player,Firefox
- Windows Media Player a oggetti, Firefox
- modello a oggetti,Firefox
- Windows Media Player Mobile, Firefox
- Windows Media Player ActiveX controllo, Firefox
- Windows Media Player Controllo ActiveX per dispositivi mobili,Firefox
- ActiveX controllo, Firefox
- Firefox, gestione degli eventi
- incorporamento di pagine Web,Firefox
- eventi,Firefox
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e971caef18114b670678fc76d0515858bee77a94a5e3f8b5c24ca5322177b8e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117748416"
---
# <a name="handling-events-in-a-web-page-displayed-by-firefox"></a>Gestione degli eventi in una pagina Web visualizzata da Firefox

Quando si incorpora il controllo Windows Media Player in una pagina Web, è possibile scrivere uno script che gestisce gli eventi. Per un elenco degli eventi generati dal controllo Player, vedere [Oggetto Player](player-object.md).

Se il tipo mime associato a un controllo Player incorporato è application/x-ms-wmp, è possibile scrivere gestori eventi con il formato seguente:


```HTML
<SCRIPT for="Player" language="jscript" event="EventName(Params)">
  ...
</SCRIPT>
```



dove *EventName* è il nome di un evento Windows Media Player e *Params* è un elenco dei parametri dell'evento. Ad esempio, il codice seguente include un gestore per [l'evento PlayStateChange.](player-player-playstatechange.md)


```HTML
<OBJECT id="Player" type="application/x-ms-wmp" width="300" height="200">
  <PARAM name="URL" value="c:\MediaFiles\Seattle.wmv"/>
</OBJECT>

<P id="p1">...</P>

<SCRIPT for="Player" event="PlayStateChange(NewState)">
  document.getElementById("p1").innerHTML = "Play state: " + NewState;
</SCRIPT>
```



Se si dispone di diverse istanze del controllo Player in una pagina Web e si usa il formato illustrato nell'esempio precedente, ogni gestore eventi è associato a un'istanza specifica del controllo Player. Nell'esempio precedente, il gestore eventi viene chiamato solo quando lo stato di riproduzione cambia per il controllo con id="Player".

Se il tipo mime associato a un controllo Player incorporato non è application/x-ms-wmp, è possibile scrivere gestori eventi con il formato seguente:


```HTML
<SCRIPT language="jscript">
  function OnDSEventNameEvt(Params)
  {...}
</SCRIPT>
```



dove *EventName* è il nome di un evento Windows Media Player e *Params* è un elenco dei parametri dell'evento. Ad esempio, il codice seguente include un gestore per **l'evento PlayStateChange.**


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



Se si dispone di diverse istanze del controllo Player in una pagina Web e si usa il formato illustrato nell'esempio precedente, ogni gestore eventi è associato a tutte le istanze del controllo Player e il gestore eventi viene chiamato quando lo stato di riproduzione cambia per qualsiasi controllo Player nella pagina.

> [!Note]  
> Se il tipo mime non è application/x-ms-wmp, l'evento **DoubleClick** viene inviato come OnDSDblClickEvt (non OnDSDoubleClickEvt) per la compatibilità con la versione 6.4 del controllo Player.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Uso del controllo Windows Media Player con Firefox**](using-the-windows-media-player-control-with-firefox.md)
</dt> </dl>

 

 




