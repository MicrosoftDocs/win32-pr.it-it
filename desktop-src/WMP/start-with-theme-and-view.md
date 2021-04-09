---
title: Inizia con tema e visualizzazione
description: Inizia con tema e visualizzazione
ms.assetid: 1ac92f3a-463a-4343-a269-5230c644b57f
keywords:
- creazione di interfacce, elemento THEME
- Windows Media Player Skin, elemento THEME
- Skin, elemento THEME
- file di definizione dell'interfaccia, elemento del tema
- Elemento THEME
- creazione di interfacce, visualizzazione di elementi
- Interfacce Media Player di Windows, elemento di visualizzazione
- Skin, elemento VIEW
- file di definizione dell'interfaccia, elemento di visualizzazione
- Elemento VIEW
- elementi, visualizzazione
- elementi, tema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 499444ee2093e743f58174797794a50fbf74555a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856826"
---
# <a name="start-with-theme-and-view"></a>Inizia con tema e visualizzazione

Ogni interfaccia deve avere esattamente un elemento del **tema** e almeno un elemento di **visualizzazione** .

Usando l'editor di testo, creare il testo seguente:


```C++
<THEME>
    <VIEW
        clippingColor = "#CCCC00"
        backgroundImage = "background.bmp"
        titleBar = "False">


    </VIEW>
</THEME>

```



Lasciare alcune righe vuote prima del tag della **visualizzazione** di chiusura perché verrà aggiunto altro codice in un secondo momento.

Salvare il file con un nome di file desiderato, ma assicurarsi che l'estensione sia. WMS. Ad esempio, un nome di file tipico potrebbe essere skinone. WMS.

Ogni interfaccia deve iniziare con <THEME> e terminare con </THEME>. È possibile avere un solo elemento del **tema** nell'interfaccia, ma è necessario disporre di uno.

È inoltre necessario disporre di almeno un elemento di **visualizzazione** . È possibile avere più di una **vista**, ma in questo esempio ne è presente solo una. È necessario avere un'apertura <VIEW> e una chiusura <VIEW>. Si noti che il </VIEW> tag di apertura non chiude immediatamente il tag, ma include diversi attributi prima della parentesi angolare di chiusura (>). Gli attributi seguenti vengono usati nell'elemento **Theme** in questo esempio:

**clippingColor**

L'attributo **clippingColor** non sarà sempre necessario se i bordi dell'interfaccia sono rettangolari. L'interfaccia in questo esempio è a forma ovale, quindi è necessario un colore di ritaglio per le parti dell'interfaccia da visualizzare sul desktop; essenzialmente tutte le parti al di fuori dell'Oval. In questo esempio di interfaccia, verrà usato un colore giallo scuro, specificato come " \# CCCC00" nel formato Web. I motivi di questa scelta sono forniti nella [creazione del file](creating-the-primary-art-file.md)di immagine principale. In sostanza, questo valore sarà sempre un numero ottenuto dal programma di grafica.

**backgroundImage**

Si tratta del nome del file di immagine principale. Deve corrispondere esattamente al nome file e al percorso del file di immagine principale. Sono supportati solo i file BMP, JPG, GIF e PNG ed è consigliabile usare BMP.

**titleBar**

Questa interfaccia non ha una **barra** del titolo, quindi il valore sarà "false". Si vuole una barra del titolo solo se si vuole che l'interfaccia abbia un colore di sfondo e sia rettangolare.

Assicurarsi di inserire la parentesi angolare di chiusura (>) dopo il valore della **barra** del titolo per indicare che è stata terminata la definizione della **visualizzazione**. Lasciare alcune righe vuote prima della **visualizzazione** di chiusura e dei tag del **tema** . Sono necessarie le righe per il codice che si aggiungerà in un secondo momento.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Creazione del file di definizione dell'interfaccia**](creating-the-skin-definition-file.md)
</dt> </dl>

 

 




