---
title: Aggiunta di una playlist
description: Aggiunta di una playlist
ms.assetid: be0c2cac-245d-4435-87d9-4f17076e005a
keywords:
- creazione di skin, playlist
- Windows Media Player, playlist
- skins, playlist
- playlist, skin
- playlist di metafile, skin
- Windows playlist metafile multimediali, skin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e23d9198f1f913b83cef40cea9f6ec47976f9f1e08a5e54257ab16df63e538b1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120031591"
---
# <a name="adding-a-playlist"></a>Aggiunta di una playlist

È possibile usare le playlist per scegliere tra raccolte di audio e video.

Usando il disegno della prima interfaccia, è possibile apportare alcune modifiche al file di definizione dell'interfaccia.

Il primo passaggio consiste nell'usare la shell che verrà utilizzata per la maggior parte delle skin:


```C++
<THEME>
    <VIEW
        clippingColor = "#CCCC00"
        backgroundImage = "background.bmp"
        titleBar = "false">

        <BUTTONGROUP
            mappingImage = "map.bmp"
            hoverImage = "hover.bmp"> 
                
    </VIEW>


</THEME>

```



Aggiungere ora una seconda **vista**, che contiene una playlist. Inserire il codice seguente dopo </VIEW> il del codice della shell.


```C++
     <VIEW 
          id = "playview">
          <PLAYLIST/>
     </VIEW>

```



È necessario assegnare a questa seconda visualizzazione un ID in modo che sia possibile fare riferimento ad essa in un secondo momento. Aggiungere un ELEMENTO PLAYELEMENT e un ELEMENTO STOPELEMENT. Questi pulsanti predefiniti semplificano la vita.


```C++
        <PLAYELEMENT
            mappingColor = "#00FF00" />
                          
        <STOPELEMENT
            mappingColor = "#FF0000" />

```



Infine, aggiungere un evento onClick a PLAYELEMENT per visualizzare una playlist nella seconda visualizzazione:


```C++
            onClick = "JScript: theme.openView('playview');" />

```



È possibile visualizzare un'interfaccia di playlist funzionante simile nella sezione di esempio dell'SDK.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Guida alla creazione dell'interfaccia**](skin-creation-guide.md)
</dt> </dl>

 

 




