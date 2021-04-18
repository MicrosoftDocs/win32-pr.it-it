---
title: Aggiunta del pulsante di riproduzione
description: Aggiunta del pulsante di riproduzione
ms.assetid: 895850a7-7538-4581-8348-41cbb3bc9717
keywords:
- creazione di interfacce, elemento BUTTONelement
- Windows Media Player Skin, elemento BUTTONelement
- interfacce, elemento BUTTONelement
- file di definizione dell'interfaccia, elemento BUTTONelement
- BUTTONelement (elemento)
- Elements, BUTTONelement
- creazione di interfacce, pulsanti di riproduzione
- Interfacce di Media Player di Windows, pulsanti di riproduzione
- interfacce, pulsanti di riproduzione
- file di definizione dell'interfaccia, pulsanti di riproduzione
- Pulsanti di riproduzione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a92b5416adf2e323043eb563ec08e1e4d2525733
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515787"
---
# <a name="adding-the-play-buttonelement"></a>Aggiunta del pulsante di riproduzione

Infine, è possibile aggiungere gli elementi **ButtonElement** che connettono i pulsanti visivi sullo schermo alle azioni di Windows Media Player. Questo è il nucleo della pelle ed è possibile considerarlo come un cablaggio della superficie dell'interfaccia alla macchina interna di Windows Media Player.

I **pulsanti** sono contenuti all'interno di un **ButtonGroup**. È necessario disporre sempre di almeno un **pulsanteelement** all'interno di ogni **ButtonGroup**.

Inserire il codice del **pulsante** di riproduzione dopo la parentesi angolare di chiusura di **ButtonGroup**.


```C++
        <BUTTONELEMENT
            mappingColor = "#00FF00"
            upToolTip = "Play"
            onClick = "JScript: player.URL='https://proseware.com/laure.wma';" />

```



Gli attributi seguenti vengono usati per definire il **pulsante ButtonElement** per il pulsante Play:

**mappingColor**

Si tratta del valore del colore di un'area nel file di grafica di mapping creato in precedenza. In questo caso si tratta del colore verde tinta unita. Questo attributo è obbligatorio per qualsiasi **pulsanteelement**. Definendo questo colore, si indica a Windows Media Player di associare questa area dei colori al codice XML di questo pulsante.

**Descrizione comando**

Definisce il testo che verrà visualizzato se l'utente posiziona il puntatore del mouse sul pulsante. Non confondere questo oggetto con l'Art hover che verrà visualizzato. Una descrizione comando è una piccola didascalia a fumetti che richiede un istante per la visualizzazione. L'immagine del passaggio del mouse, tuttavia, verrà visualizzata immediatamente in base al colore e alla forma scelti.

**onClick**

Definisce l'evento che si verifica quando si fa clic con il mouse sul pulsante. Il valore di questo attributo evento è denominato gestore eventi e sarà una riga di codice Microsoft JScript o una funzione JScript in un file di testo esterno caricato dall'attributo **loadScript** di una **vista**. In questo caso, il codice JScript chiama il metodo **URL** di Windows Media Player, che carica e avvia la riproduzione di un file denominato "Laure. WMA". Si noti che la riga termina con un punto e virgola all'interno delle virgolette, che è un'ottima pratica del codice JScript. Si noti anche l'uso delle virgolette singole all'interno delle virgolette doppie per impostare il nome del file. Per ulteriori informazioni su JScript, vedere [utilizzo di JScript](using-jscript.md) nella sezione about Skins di questo SDK.

Si noti che non è presente alcun tag **ButtonElement** finale. Se un elemento non racchiude un altro elemento, è possibile chiuderlo con la barra immediatamente prima della parentesi angolare di chiusura. Ciò indica a XML che l'elemento è terminato. Ad esempio,


```C++
<BUTTONELEMENT></BUTTONELEMENT>
```



e


```C++
<BUTTONELEMENT/>
```



fornire le stesse informazioni in XML.

La potenza delle interfacce deriva dall'uso dei gestori eventi. Se l'utente esegue un'operazione con il mouse, è possibile gestire l'evento con JScript. Il codice può essere costituito da una singola riga che consente a Windows Media Player di eseguire operazioni semplici come la riproduzione o un'applicazione completa scritta in JScript.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Creazione del file di definizione dell'interfaccia**](creating-the-skin-definition-file.md)
</dt> </dl>

 

 




