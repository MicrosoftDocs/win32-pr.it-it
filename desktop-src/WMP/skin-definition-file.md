---
title: File di definizione dell'interfaccia
description: File di definizione dell'interfaccia
ms.assetid: ed5f7c61-c830-4075-a79f-d5539454bd3b
keywords:
- Interfacce di Media Player di Windows, file di definizione dell'interfaccia
- interfacce, file di definizione dell'interfaccia
- file per le interfacce, definizione dell'interfaccia
- file di definizione dell'interfaccia, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bd06708a99a15dc9a8266278850c0507007f058
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298585"
---
# <a name="skin-definition-file"></a>File di definizione dell'interfaccia

I file di definizione dell'interfaccia contengono le istruzioni di base per l'utilizzo dell'interfaccia e la posizione in cui possono essere trovati altri file usati dall'interfaccia. Può essere presente un solo file di definizione di interfaccia per un'interfaccia e ha un'estensione del nome di file WMS.

Le istruzioni nel file di definizione dell'interfaccia sono scritte in Extensible Markup Language (XML), che è simile a HTML. Se è stato usato HTML per creare pagine Web, si noterà che XML ha un aspetto familiare.

Il codice XML nel file di definizione dell'interfaccia usa un set di tag di elemento speciali per definire le parti dell'interfaccia utente di skin. Ad esempio, l'elemento [Button](button-element.md) definisce il comportamento di un pulsante, la posizione in cui verrà inserito e l'aspetto.

Ogni tag di elemento ha attributi specifici. Ad esempio, l'elemento [Button](button-element.md) ha un attributo **Image** che definisce la posizione in cui è possibile trovare l'immagine per il pulsante. Questa operazione è simile a HTML, in cui l'elemento BODY avrà un attributo **bgcolor** che definisce il colore di sfondo della pagina HTML. Informazioni dettagliate su tutti gli elementi Skin e sui relativi attributi sono incluse nella sezione riferimento per la [programmazione dell'interfaccia](skin-programming-reference.md) .

XML include alcune semplici regole che è necessario tenere presente per creare le interfacce. A differenza di HTML, XML richiede di seguire esattamente le regole.

## <a name="enclose-elements-with-angle-brackets"></a>Racchiudere gli elementi tra parentesi angolari

Tutti gli elementi sono racchiusi tra parentesi angolari; ad esempio, l'elemento **Button** è tipizzato come segue:


```C++
<BUTTON>

```



Non è necessario digitare la parola "BUTTON" in tutte le lettere maiuscole, ma la convenzione di digitare i nomi degli elementi in tutti i caratteri maiuscoli viene usata nel codice di esempio di questo SDK.

## <a name="put-attributes-before-the-closing-bracket"></a>Inserire gli attributi prima della parentesi quadra di chiusura

Tutti gli attributi per un particolare elemento devono essere inclusi prima della parentesi angolare di chiusura. Un attributo è costituito dal nome dell'attributo seguito da un segno di uguale (=) e dal valore dell'attributo tra virgolette.


```C++
<BUTTON image="mypic.jpg">

```



Non è necessario digitare la parola "image" in minuscolo, ma la convenzione di tipizzazione dei nomi degli attributi in minuscolo viene usata nel codice di esempio di questo SDK. Si noti inoltre che il valore dell'attributo è racchiuso tra virgolette.

## <a name="opening-and-closing-elements"></a>Apertura e chiusura di elementi

Alcuni elementi vengono raggruppati all'interno di un altro elemento. Ad esempio, l'elemento **ButtonGroup** non ha molto senso, a meno che non si usino uno o più elementi **ButtonElement** . Per chiarire il raggruppamento, è necessario disporre di un tag di apertura e di chiusura per ogni elemento. Il tag di apertura è solo il nome dell'elemento e gli eventuali attributi correlati, racchiusi tra parentesi angolari. Il tag di chiusura è il nome dell'elemento, preceduto da una barra (/), quindi racchiuso tra parentesi angolari. Ad esempio, il tag di apertura dell'elemento **ButtonGroup** è simile al seguente:


```C++
<BUTTONGROUP>

```



Il tag di chiusura **ButtonGroup** ha un aspetto simile al seguente:


```C++
</BUTTONGROUP>

```



Inserire i tag **ButtonElement** tra i tag dell'elemento **ButtonGroup** di apertura e di chiusura. Ad esempio:


```C++
<BUTTONGROUP>
    <BUTTONELEMENT/>
    <BUTTONELEMENT/>
    <BUTTONELEMENT/>
</BUTTONGROUP>

```



## <a name="closing-off-elements"></a>Chiusura di elementi

Se un elemento non contiene altri elementi, è necessario inserire una barra alla fine del nome dell'elemento immediatamente prima della parentesi angolare di chiusura. Nel codice precedente, ad esempio, ogni elemento **ButtonElement** ha una barra per indicare che non sono presenti altri elementi annidati al suo interno.

In altre parole, è necessario avere un tag di chiusura dell'elemento o chiudere l'elemento con una barra.

Questa operazione è corretta:


```C++
<BUTTONGROUP>
    <BUTTONELEMENT/>
    <BUTTONELEMENT/>
</BUTTONGROUP>

```



Questa operazione non è corretta:


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



Nella sezione seguente vengono fornite ulteriori informazioni sui file di definizione dell'interfaccia:

-   [Struttura del file di definizione dell'interfaccia](skin-definition-file-structure.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**File di interfaccia**](skin-files.md)
</dt> </dl>

 

 




