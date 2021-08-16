---
title: Codice completo per l'interfaccia semplice
description: Codice completo per l'interfaccia semplice
ms.assetid: ece437d2-1a11-4096-8b3b-db2b4def8248
keywords:
- creazione di interfaccia, esempi di codice
- Windows Media Player, esempi di codice
- skins, esempi di codice
- file di definizione dell'interfaccia utente, esempi di codice
- creazione di interfaccia, esempi
- Windows Media Player, esempi
- skins,examples
- file di definizione dell'interfaccia, esempi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a3b4d4380c6d7fb44290e8faff26bf5cb84dae552d09fe13594402dbe434ab0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135794"
---
# <a name="complete-code-for-simple-skin"></a>Codice completo per l'interfaccia semplice

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



A questo punto sono state riunite tutte le parti.

Creare un file compresso con un'.zip file con estensione . Questo file compresso contiene il file di definizione dell'interfaccia, le bitmap e tutti i file multimediali digitali da includere. Rinominare il file in modo che abbia estensione wmz. Quindi, facendo doppio clic sull'interfaccia compressa, verrà avviata la riproduzione.

È possibile visualizzare un'interfaccia semplice funzionante simile nella sezione degli esempi dell'SDK.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Creazione del file di definizione dell'interfaccia**](creating-the-skin-definition-file.md)
</dt> </dl>

 

 




