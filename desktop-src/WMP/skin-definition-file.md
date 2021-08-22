---
title: File di definizione dell'interfaccia
description: File di definizione dell'interfaccia
ms.assetid: ed5f7c61-c830-4075-a79f-d5539454bd3b
keywords:
- Windows Media Player, file di definizione dell'interfaccia
- skins, file di definizione dell'interfaccia
- file per le interfaccia, definizione dell'interfaccia
- file di definizione dell'interfaccia utente, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7bf162870596968872c4f146772c9e62277f5b2ccb660270794248786a71355
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995241"
---
# <a name="skin-definition-file"></a>File di definizione dell'interfaccia

I file di definizione dell'interfaccia contengono le istruzioni di base per le operazioni dell'interfaccia e la posizione in cui è possibile trovare altri file usati dall'interfaccia. Può essere presente un solo file di definizione dell'interfaccia per un'interfaccia e ha estensione wms.

Le istruzioni nel file di definizione dell'interfaccia sono scritte in Extensible Markup Language (XML), che è simile a HTML. Se è stato usato HTML per creare pagine Web, il codice XML avrà un aspetto familiare.

Il codice XML nel file di definizione dell'interfaccia usa un set di tag di elemento speciali per definire parti dell'interfaccia utente dell'interfaccia utente. Ad esempio, [l'elemento BUTTON](button-element.md) definisce il comportamento di un pulsante, la posizione in cui verrà visualizzato e l'aspetto che avrà.

Ogni tag di elemento ha attributi specifici. Ad esempio, [l'elemento BUTTON](button-element.md) ha un **attributo image** che definisce dove è possibile trovare l'immagine per il pulsante. È simile a HTML, in cui l'elemento BODY avrà un attributo **bgcolor** che definisce il colore di sfondo della pagina HTML. Informazioni dettagliate su tutti gli elementi dell'interfaccia e i relativi attributi sono incluse nella [sezione Riferimenti alla programmazione dell'interfaccia](skin-programming-reference.md) utente.

XML include alcune semplici regole che è necessario conoscere per creare le interfaccia. A differenza di HTML, XML richiede di seguire esattamente le regole.

## <a name="enclose-elements-with-angle-brackets"></a>Racchiudere gli elementi tra parentesi angolari

Tutti gli elementi sono racchiusi tra parentesi angolari. Ad esempio, **l'elemento BUTTON** è digitato nel modo seguente:


```C++
<BUTTON>

```



Non è necessario digitare la parola "BUTTON" in lettere maiuscole, ma nel codice di esempio di questo SDK viene usata la convenzione di digitazione dei nomi degli elementi in lettere maiuscole.

## <a name="put-attributes-before-the-closing-bracket"></a>Inserire attributi prima della parentesi di chiusura

Tutti gli attributi per un particolare elemento devono essere inclusi prima della parentesi uncinata chiusa. Un attributo è costituito dal nome dell'attributo seguito da un segno di uguale (=) e dal valore dell'attributo tra virgolette.


```C++
<BUTTON image="mypic.jpg">

```



Non è necessario digitare la parola "image" in minuscolo, ma la convenzione di digitazione dei nomi di attributo in minuscolo viene usata nel codice di esempio di questo SDK. Si noti anche che il valore dell'attributo è racchiuso tra virgolette.

## <a name="opening-and-closing-elements"></a>Apertura e chiusura di elementi

Alcuni elementi vengono raggruppati all'interno di un altro elemento. Ad esempio, **l'elemento BUTTONGROUP** non ha molto senso a meno che non si usino uno o più **elementi BUTTONELEMENT** con esso. Per rendere chiaro il raggruppamento, è necessario disporre di un tag di apertura e chiusura per ogni elemento. Il tag di apertura è solo il nome dell'elemento ed eventuali attributi correlati, racchiusi tra parentesi angolari. Il tag di chiusura è il nome dell'elemento, preceduto da una barra (/) e quindi racchiuso tra parentesi angolari. Ad esempio, il tag **di apertura dell'elemento BUTTONGROUP** è simile al seguente:


```C++
<BUTTONGROUP>

```



Il tag **BUTTONGROUP di** chiusura è simile al seguente:


```C++
</BUTTONGROUP>

```



Inserire i tag **BUTTONELEMENT** tra i tag di apertura e chiusura **dell'elemento BUTTONGROUP.** Esempio:


```C++
<BUTTONGROUP>
    <BUTTONELEMENT/>
    <BUTTONELEMENT/>
    <BUTTONELEMENT/>
</BUTTONGROUP>

```



## <a name="closing-off-elements"></a>Chiusura di elementi

Se un elemento non contiene altri elementi, è necessario inserire una barra alla fine del nome dell'elemento subito prima della parentesi uncinata chiusa. Nel codice precedente, ad esempio, ogni **elemento BUTTONELEMENT** ha una barra per indicare che non sono presenti altri elementi annidati al suo interno.

In altre parole, è necessario avere un tag di chiusura dell'elemento o chiudere l'elemento con una barra.

Questo è corretto:


```C++
<BUTTONGROUP>
    <BUTTONELEMENT/>
    <BUTTONELEMENT/>
</BUTTONGROUP>

```



Questo non è corretto:


```C++
<BUTTONGROUP/>
    <BUTTONELEMENT/>
    <BUTTONELEMENT/>
</BUTTONGROUP>

```



Anche questo non è corretto:


```C++
<BUTTONGROUP>
    <BUTTONELEMENT>
    <BUTTONELEMENT>
</BUTTONGROUP>

```



La sezione seguente fornisce altre informazioni sui file di definizione dell'interfaccia:

-   [Struttura del file di definizione dell'interfaccia](skin-definition-file-structure.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**File di interfaccia**](skin-files.md)
</dt> </dl>

 

 




