---
title: Attributi globali (Windows Media Player SDK)
description: Attributi globali
ms.assetid: 2ed09506-990e-4da2-89d6-6ff77dc43eb2
keywords:
- Windows Media Player Skin, attributi globali
- interfacce, attributi globali
- riferimento per le interfacce, attributi globali
- attributi globali
- attributi, globali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19c3f7a605b5c277b3207cefbbeaaa641f81f026
ms.sourcegitcommit: 40a1246849dba8ececf54c716b2794b99c96ad50
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/12/2019
ms.locfileid: "104398178"
---
# <a name="global-attributes"></a>Attributi globali

Gli attributi globali sono attributi che consentono di accedere facilmente a determinati elementi o oggetti dei giocatori da qualsiasi punto all'interno di un'interfaccia.

L'attributo globale **Player** è un riferimento all'oggetto [Player](player-object.md) e viene usato per accedere alle funzionalità principali di Windows Media Player. Nell'esempio seguente viene usato **Player** per iniziare la riproduzione di file multimediali digitali.


```C++
<BUTTON
  onclick="jscript:player.controls.play();"
/>

```



L'attributo globale del **tema** è un riferimento all'elemento [Theme](theme-element.md) . Questo è il modo giusto per accedere agli attributi del **tema** , anziché specificare un ID nell'elemento **Theme** . Nell'esempio seguente viene usato il **tema** per aprire una nuova visualizzazione.


```C++
<TEXT 
  value="open" 
  onclick="jscript:theme.openView('newView');"
/>

```



L'attributo **View** Global è un riferimento alla [visualizzazione](view-element.md)corrente. Questa operazione può essere utilizzata al posto dell'ID specificato nei vari elementi di **visualizzazione** . Nell'esempio seguente viene utilizzata la **vista** per chiudere la visualizzazione corrente.


```C++
<BUTTON 
  id="quitbutton"
  onclick="jscript:view.close();"
/>

```



L'attributo Global dell' **evento** viene usato per accedere agli attributi degli eventi di ambiente dall'interno di gestori eventi. Nell'esempio seguente viene usato l' **evento** per determinare se il tasto ALT viene premuto quando si fa clic su un pulsante.


```C++
<BUTTON
  onclick="jscript:if (event.altKey == true) myText.value='ALT';"
/>

```



L'attributo globale **playerApplication** è un riferimento all'oggetto [playerApplication](playerapplication-object.md) e viene usato dai file di interfaccia specificati come interfacce utente personalizzate per i controlli del lettore remoto. Il controllo Player può essere incorporato in modalità remota solo nei programmi C++ che implementano l'interfaccia **IWMPRemoteMediaServices** . Nell'esempio seguente viene usato **playerApplication** per passare alla modalità completa del lettore.


```C++
<BUTTON
  onclick="jscript:playerApplication.switchToPlayerApplication();"
/>

```



Per altre informazioni, vedere [attributi degli eventi di ambiente](ambient-event-attributes.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Varie**](miscellaneous.md)
</dt> </dl>

 

 




