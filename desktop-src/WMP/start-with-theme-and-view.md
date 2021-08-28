---
title: Iniziare con THEME e VIEW
description: Iniziare con THEME e VIEW
ms.assetid: 1ac92f3a-463a-4343-a269-5230c644b57f
keywords:
- creazione di interfaccia, elemento THEME
- Windows Media Player, elemento THEME
- skins,theme - elemento
- file di definizione dell'interfaccia utente,elemento THEME
- THEME - elemento
- creazione di interfaccia, elemento VIEW
- Windows Media Player, elemento VIEW
- skins,view - elemento
- file di definizione dell'interfaccia utente,elemento VIEW
- VIEW - elemento
- elementi, VIEW
- elementi, THEME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51bcb18a9d56a8780e56d81d6de60ca269036c72
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122883720"
---
# <a name="start-with-theme-and-view"></a>Iniziare con THEME e VIEW

Ogni interfaccia deve avere esattamente **un elemento THEME** e almeno un elemento **VIEW.**

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



Lasciare alcune righe vuote prima del tag **VIEW di** chiusura perché in seguito si aggiungerà altro codice.

Salvare il file con il nome desiderato, ma assicurarsi che l'estensione sia wms. Ad esempio, un nome di file tipico potrebbe essere skinone.wms.

Ogni interfaccia deve iniziare con &lt; THEME &gt; e terminare con </THEME> . È possibile avere un solo **elemento THEME** nell'interfaccia, ma è necessario disporre di un elemento .

È inoltre necessario disporre di almeno un **elemento VIEW.** È possibile avere più DI **VIEW,** ma in questo esempio ne è presente una sola. È necessario disporre di un elemento &lt; VIEW di apertura e di un elemento VIEW di &gt; &lt; &gt; chiusura. Si noti che il tag /VIEW di apertura non chiude immediatamente il tag, ma include diversi attributi prima della parentesi uncinata di chiusura &lt; &gt; (>). Nell'elemento THEME di questo esempio **vengono usati** gli attributi seguenti:

**clippingColor**

Non sarà sempre necessario **l'attributo clippingColor** se i bordi dell'interfaccia sono rettangolari. L'interfaccia in questo esempio è a forma di ovale, quindi è necessario un colore di ritaglio per le parti dell'interfaccia da visualizzare sul desktop; essenzialmente tutte le parti esterne all'ovale. In questa interfaccia di esempio si userà un giallo scuro, specificato come " \# CCCC00" in formato Web. I motivi di questa scelta sono disponibili in [Creating the Primary Art File](creating-the-primary-art-file.md). Essenzialmente, questo valore sarà sempre un numero che si ottiene dal programma di grafica.

**backgroundImage**

Questo è il nome del file di grafica principale. Deve essere il nome e il percorso esatti del file art principale. Sono supportati solo file BMP, JPG, GIF e PNG ed è consigliabile utilizzare BMP.

**Titlebar**

Questa interfaccia non ha **titleBar**, quindi il valore sarà "false". È possibile usare una barra del titolo solo se si vuole che l'interfaccia abbia un colore di sfondo e sia rettangolare.

Assicurarsi di inserire la parentesi uncinata di chiusura (>) dopo il valore **titleBar** per indicare che la definizione di **VIEW è terminata.** Lasciare alcune righe vuote prima dei tag **VIEW e** **THEME di** chiusura. Saranno necessarie le righe per il codice che verrà aggiunto in un secondo momento.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Creazione del file di definizione dell'interfaccia**](creating-the-skin-definition-file.md)
</dt> </dl>

 

 




