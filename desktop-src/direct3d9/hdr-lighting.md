---
description: L'illuminazione nel mondo reale contiene un intervallo dinamico molto elevato (HDR) di valori di luminanza.
ms.assetid: 537700e2-802d-4fd1-b026-142d6f4f0559
title: Illuminazione HDR (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f397ccef2b1fa315e64861453b13f0f6fddfe77
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104225295"
---
# <a name="hdr-lighting-direct3d-9"></a>Illuminazione HDR (Direct3D 9)

L'illuminazione nel mondo reale contiene un intervallo dinamico molto elevato (HDR) di valori di luminanza. Il mondo reale ha circa 10 ordini di intervallo dinamico (DR) per i valori di luminanza distribuiti attraverso la gamma di oscurità alla luminosità. D'altra parte, una schermata del computer ha una gamma di visualizzazione molto limitata (o un intervallo di valori di luminanza): circa due ordini di intervallo dinamico. La sfida alla produzione di immagini con rendering HDR consiste nel mappare i valori HDR del mondo reale alla gamma limitata di uno schermo del computer.

Il mapping dei toni è la tecnica usata da DirectX per il mapping delle informazioni HDR in un intervallo più limitato. Il mapping dei toni applicato al rendering CGI può migliorare significativamente la quantità di dettagli di illuminazione di cui è stato eseguito il rendering, consentendo di visualizzare i dettagli nelle aree più scure e mettendo a confronto le aree che sono così luminose, sembrano bruciate. Le scene risultanti eseguono il rendering con dettagli di illuminazione molto più visibili.

L' [esempio HDRLighting](https://msdn.microsoft.com/library/Ee417769(v=VS.85).aspx) è un esempio di SDK che illustra l'illuminazione HDR.

## <a name="tone-mapping"></a>Mapping dei toni

Il mapping dei toni consente in genere di simulare fenomeni ottici che non possono essere causati dal ripristino di emergenza del monitor. Esempi di questo scenario sono i fuochi o i fiori (che sono principalmente proprietà delle lenti), il turno blu che si verifica nell'occhio umano in condizioni di scarsa luminosità e altri adattamenti che sono il risultato della biochimica dell'occhio. Se il ripristino di emergenza del display era sufficientemente grande, il mapping dei toni non sarebbe stato necessario, a meno che non si forniscano effetti artistici o alcune delle proprietà di una fotocamera o un dispositivo a pagamento (CCD).

Il mapping dei toni divide l'intervallo di valori di luminanza in una scena in un set di zone. Ogni zona comprende un intervallo di valori di luminanza.

HDR usa i termini seguenti:

-   Area-intervallo di valori di luminanza
-   Grigio medio-area della luminosità intermedia della scena
-   Intervallo dinamico-rapporto della luminanza della scena più alta alla luminanza della scena più bassa
-   Misurazione soggettiva dell'illuminazione della scena: varia da chiaro a moderato a scuro

Per calcolare la luminanza dai valori RGB, usare:


```
L = 0.27R + 0.67G + 0.06B;
```



La luminanza media dei log è un'approssimazione utile per la chiave di una scena. Un'equazione generale ha un aspetto simile al seguente:

L<sub>w</sub> = exp \[ 1/N ( \[ log Sum (Delta + L<sub>w</sub>(x, y)) \] ) \]

Dove:

-   L<sub>w</sub> -log-luminanza media
-   N: numero di pixel nell'immagine
-   Delta: fattore ridotto per evitare problemi con i pixel neri
-   L<sub>w</sub>(x, y): luminanza dello spazio globale per pixel (x, y)

Per eseguire il mapping di questo oggetto a un valore grigio medio, di seguito è riportato un operatore di ridimensionamento della luminanza:

L (x, y) = a \* l<sub>w</sub>(x, y)/L<sub>w</sub>

Dove:

-   L (x, y): luminanza ridimensionata per pixel (x, y)
-   valore della chiave-image dopo l'applicazione del ridimensionamento

Infine, di seguito è riportato un semplice operatore di mapping dei toni per comprimere le luminanze elevate:

L<sub>d</sub>(x, y) = l (x, y)/(1 + L (x, y))

Dove:

-   L<sub>d</sub>(x, y): luminanza compressa e scalata per pixel (x, y)
-   valore della chiave-image dopo l'applicazione del ridimensionamento

Questo operatore ridimensiona le luminanze elevate di 1/L e le luminanze basse di 1. Per ulteriori informazioni, vedere il seguente documento.

Reinhard, Erik, Mike Stark, Peter Shirley e James Ferwerda. ["Riproduzione del tono fotografico per le immagini digitali"](https://www.cs.utah.edu/~reinhard/cdrom/tonemap.pdf). ACM Transactions on Graphics (TOG), procedimenti della 29a annuale Conference on computer graphics and Interactive Techniques (SIGGRAPH), pp. 267-276. New York, NY: ACM Press, 2002.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Argomenti avanzati](advanced-topics.md)
</dt> </dl>

 

 



