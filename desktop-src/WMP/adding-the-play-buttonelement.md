---
title: Aggiunta di PLAY BUTTONELEMENT
description: Aggiunta di PLAY BUTTONELEMENT
ms.assetid: 895850a7-7538-4581-8348-41cbb3bc9717
keywords:
- creazione di skin, elemento BUTTONELEMENT
- Windows Media Player skin, elemento BUTTONELEMENT
- skins,ELEMENTO BUTTONELEMENT
- File di definizione dell'interfaccia,elemento BUTTONELEMENT
- Elemento BUTTONELEMENT
- elementi,BUTTONELEMENT
- creazione di skin, pulsanti di riproduzione
- Windows Media Player skin, Pulsanti di riproduzione
- skins,Pulsanti di riproduzione
- file di definizione dell'interfaccia, pulsanti Di riproduzione
- Pulsanti di riproduzione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cab52691b48876327f45fbaf30a98de78c8c0c46a2eafd0a2c342e51c5a8683
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118583545"
---
# <a name="adding-the-play-buttonelement"></a>Aggiunta di PLAY BUTTONELEMENT

Infine, è possibile aggiungere gli **elementi BUTTONELEMENT** che connettono i pulsanti visivi sullo schermo per Windows Media Player azioni. Questo è il nucleo della tua interfaccia e puoi pensarlo come cablare la superficie della pelle ai macchinari interni della Windows Media Player.

**GLI ELEMENTI BUTTONELEMENT** sono contenuti in **un oggetto BUTTONGROUP.** È necessario avere sempre almeno un **ELEMENTO BUTTONELEMENT all'interno** di **ogni BUTTONGROUP.**

Inserire il codice **PLAY BUTTONELEMENT** dopo la parentesi uncinata di chiusura **di BUTTONGROUP**.


```C++
        <BUTTONELEMENT
            mappingColor = "#00FF00"
            upToolTip = "Play"
            onClick = "JScript: player.URL='https://proseware.com/laure.wma';" />

```



Gli attributi seguenti vengono usati per definire **BUTTONELEMENT** per il pulsante Play:

**mappingColor**

Si tratta del valore del colore di un'area nel file di mapping creato in precedenza. In questo caso è il colore verde a tinta unita. Questo attributo è obbligatorio per **qualsiasi ELEMENTO BUTTONELEMENT.** Definendo questo colore, si indica Windows Media Player di associare questa area colori al codice XML di questo pulsante.

**upToolTip**

Definisce il testo che verrà visualizzato se l'utente passa il mouse sul pulsante. Non confondere questo oggetto con l'immagine al passaggio del mouse che verrà visualizzata. Una descrizione comando è una piccola didascalia del fumetto che richiede un momento per la visualizzazione. L'immagine grafica al passaggio del mouse, tuttavia, verrà visualizzata immediatamente in qualsiasi colore e forma scelta.

**Onclick**

Definisce l'evento che si verifica quando il mouse fa clic sul pulsante. Il valore di questo attributo dell'evento viene chiamato gestore eventi e sarà una riga di codice Microsoft JScript o una funzione JScript in un file di testo esterno caricato dall'attributo **loadScript** di un **oggetto VIEW**. In questo caso, il JScript chiama il metodo **URL** di Windows Media Player, che carica e avvia la riproduzione di un file denominato "laure.wma". Si noti che la riga termina con un punto e virgola all'interno delle virgolette, che è una buona JScript di codifica. Si noti anche l'uso di virgolette singole all'interno delle virgolette doppie per impostare il nome del file. Per altre informazioni sui JScript, vedere [Using JScript](using-jscript.md) nella sezione About Skins di questo SDK.

Si noti che non è presente alcun tag **BUTTONELEMENT** finale. Se un elemento non racchiude un altro elemento, è possibile chiuderlo con la barra prima della parentesi uncinata di chiusura. Ciò indica a XML che l'elemento è stato completato. Ad esempio,


```C++
<BUTTONELEMENT></BUTTONELEMENT>
```



e


```C++
<BUTTONELEMENT/>
```



trasmettere le stesse informazioni in XML.

La potenza delle skin deriva dall'uso di gestori eventi. Se l'utente esegue un'azione con il mouse, è possibile gestire l'evento con JScript. Il codice può essere una singola riga che Windows Media Player eseguire qualcosa di semplice come il gioco o può essere un'applicazione completa scritta in JScript.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Creazione del file di definizione dell'interfaccia**](creating-the-skin-definition-file.md)
</dt> </dl>

 

 




