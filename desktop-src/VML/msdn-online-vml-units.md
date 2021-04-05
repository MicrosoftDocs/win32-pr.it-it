---
title: Unità la
description: In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.
ms.assetid: f95e65ad-d92a-460f-baeb-30fd8a35f84e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e59ff91fb134edeba7e653be30141b3f72c6b65
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728239"
---
# <a name="vml-units"></a>Unità la

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Le unità CSS seguenti vengono utilizzate da la.



Unità di lunghezza relativa

em

Altezza del tipo di carattere dell'elemento.

ex

Altezza della lettera "x".

px

Pixel.

%

Percentuale.

Unità di lunghezza assoluta

in ingresso

Pollici (1 pollice = 2,54 centimetri).

cm

Centimetri.

MM

Millimetri.

pt

Punti (1 punto = 1/72 cm).

pc

Pica (1 pica = 12 punti).



 

Le misurazioni e le posizioni nelle proprietà del foglio di stile CSS vengono effettuate usando unità di lunghezza. Internet Explorer supporta due tipi di unità di lunghezza: relativo e assoluto.

Un'unità di lunghezza relativa specifica una lunghezza rispetto a un'altra proprietà Length. Le unità di lunghezza relativa scalano meglio da un dispositivo di output a un altro, ad esempio da un monitor a una stampante. Percentuali e parole chiave vengono eseguite in modo analogo.

Un'unità di lunghezza assoluta specifica una misura assoluta, ad esempio pollici o centimetri. Le unità di lunghezza assoluta sono utili quando le proprietà fisiche del dispositivo di output sono note.

## <a name="other-units-of-measurement"></a>Altre unità di misura

**UEM**

EMU (unità metrica inglese) è la più piccola unità di misura utile e viene usata da la per l'archiviazione unità interna. Ci sono 914400 EMU per pollice e 12700 EMU in un punto. Emù non può essere frazionario.

Poiché emù sono definiti da numeri integrali con segno a 32 bit, il numero maggiore di emù è 2348 pollici (circa 59 metri o 65 yarde). Poiché le misurazioni rientrano sempre in un dispositivo di output di dimensioni dello schermo o della pagina, saranno sempre incluse in questo intervallo.

**Angoli**

Le misurazioni angolo possono essere definite con i suffissi seguenti.



Suffisso

FD

Gradi frazionari.

Nessuno

Degrees

deg

Degrees

rad

Radians



 

 

 