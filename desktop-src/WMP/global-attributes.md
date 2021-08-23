---
title: Attributi globali (Windows Media Player SDK)
description: Attributi globali
ms.assetid: 2ed09506-990e-4da2-89d6-6ff77dc43eb2
keywords:
- Windows Media Player, attributi globali
- skins, attributi globali
- informazioni di riferimento per le interfaccia, attributi globali
- attributi globali
- attributi, globale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69c2d52b6489a28eff20e3a7e5c7180fc9e2db9309c0fe42880bfc779a23f563
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119648081"
---
# <a name="global-attributes"></a>Attributi globali

Gli attributi globali sono attributi che consentono di accedere facilmente a determinati elementi o oggetti del lettore da qualsiasi posizione all'interno di un'interfaccia.

**L'attributo** globale del giocatore è un riferimento all'oggetto [Player](player-object.md) e viene usato per accedere alla funzionalità principale di Windows Media Player. Nell'esempio seguente viene utilizzato **il lettore** per avviare la riproduzione multimediale digitale.


```C++
<BUTTON
  onclick="jscript:player.controls.play();"
/>

```



**L'attributo** globale theme è un riferimento all'elemento [THEME.](theme-element.md) Questo è il modo corretto per accedere agli **attributi THEME,** anziché specificando un ID all'interno dell'elemento **THEME.** Nell'esempio seguente viene **utilizzato il** tema per aprire una nuova visualizzazione.


```C++
<TEXT 
  value="open" 
  onclick="jscript:theme.openView('newView');"
/>

```



**L'attributo** globale della vista è un riferimento all'oggetto [VIEW corrente.](view-element.md) Può essere usato al posto dell'ID specificato all'interno dei **vari elementi VIEW.** Nell'esempio seguente **viene utilizzata la** vista per chiudere la visualizzazione corrente.


```C++
<BUTTON 
  id="quitbutton"
  onclick="jscript:view.close();"
/>

```



**L'attributo** globale dell'evento viene usato per accedere agli attributi dell'evento di ambiente dall'interno dei gestori eventi. Nell'esempio seguente viene **utilizzato l'evento** per determinare se il tasto ALT viene premuto quando si fa clic su un pulsante.


```C++
<BUTTON
  onclick="jscript:if (event.altKey == true) myText.value='ALT';"
/>

```



**L'attributo globale playerApplication** è un riferimento all'oggetto [PlayerApplication](playerapplication-object.md) e viene usato dai file di interfaccia forniti come interfacce utente personalizzate per i controlli Player remoti. Il controllo Player può essere incorporato in modalità remota solo nei programmi C++ che implementano **l'interfaccia IWMPRemoteMediaServices.** L'esempio seguente **usa playerApplication** per passare alla modalità completa del lettore.


```C++
<BUTTON
  onclick="jscript:playerApplication.switchToPlayerApplication();"
/>

```



Per altre informazioni, vedere [Attributi degli eventi di ambiente.](ambient-event-attributes.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Varie**](miscellaneous.md)
</dt> </dl>

 

 




