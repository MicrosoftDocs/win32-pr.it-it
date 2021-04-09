---
title: Completa il codice per interfaccia semplice
description: Completa il codice per interfaccia semplice
ms.assetid: ece437d2-1a11-4096-8b3b-db2b4def8248
keywords:
- creazione di interfacce, esempi di codice
- Windows Media Player Skin, esempi di codice
- interfacce, esempi di codice
- file di definizione dell'interfaccia, esempi di codice
- creazione di interfacce, esempi
- Windows Media Player Skin, esempi
- interfacce, esempi
- file di definizione dell'interfaccia, esempi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3682e6143c751d1c72cd8799f849fef7c9c27adb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856442"
---
# <a name="complete-code-for-simple-skin"></a>Completa il codice per interfaccia semplice

Ecco il codice completo per la prima interfaccia di esempio:


```C++
<THEME>
    <VIEW
        clippingColor = "#CCCC00"
        backgroundImage = "background.bmp"
        titleBar = "false">
         
        <BUTTONGROUP
            mappingImage = "map.bmp"
            hoverImage = "hover.bmp"> 
                
        <BUTTONELEMENT
            mappingColor = "#00FF00"
            upToolTip = "Play"
            onClick="JScript: player.URL='https://proseware.com/laure.wma';" />
                          
        <BUTTONELEMENT
            mappingColor = "#FF0000"
            upToolTip = "Close"
            onClick = "JScript: view.close(); " />
                
        </BUTTONGROUP>
    </VIEW>
</THEME>

```



A questo punto, tutti i componenti sono stati assemblati.

Creare un file compresso con estensione zip. Questo file compresso contiene il file di definizione dell'interfaccia personalizzata, le bitmap e tutti i file multimediali digitali che si desidera includere. Rinominare il file in modo che disponga di un'estensione di file WMZ. Quindi, facendo doppio clic sull'interfaccia compressa verrà avviata la riproduzione.

Nella sezione degli esempi dell'SDK è possibile visualizzare un'interfaccia semplice e funzionante simile.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Creazione del file di definizione dell'interfaccia**](creating-the-skin-definition-file.md)
</dt> </dl>

 

 




