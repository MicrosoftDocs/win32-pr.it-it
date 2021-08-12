---
title: Unità VML
description: Questo articolo descrive le unità VML. VML è una funzionalità deprecata a Windows Internet Explorer 9.
ms.assetid: f95e65ad-d92a-460f-baeb-30fd8a35f84e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5c510bacd2081fb5a051637b6b577fc9415662737d384d10d7c3dd73348c694
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118597382"
---
# <a name="vml-units"></a>Unità VML

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su VML devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato.](/previous-versions/windows/internet-explorer/ie-developer/) Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Le unità CSS seguenti vengono usate da VML.



Unità di lunghezza relativa

Em

Altezza del tipo di carattere dell'elemento.

ad esempio

Altezza della lettera "x".

px

Pixel.

%

Percentuale.

Unità di lunghezza assoluta

in

Pollici (1 pollice = 2,54 centimetri).

cm

Centimetri.

MM

Millimetri.

pt

Punti (1 punto = 1/72 pollici).

pc

Picas (1 immagine = 12 punti ).



 

Le misure e le posizioni nelle proprietà CSS (Cascading Style Sheet) vengono effettuate usando unità di lunghezza. Internet Explorer supporta due tipi di unità di lunghezza: relative e absolute.

Un'unità di lunghezza relativa specifica una lunghezza in relazione a un'altra proprietà length. Le unità di lunghezza relativa vengono ridimensionate meglio da un dispositivo di output a un altro, ad esempio da un monitor a una stampante. Le percentuali e le parole chiave hanno prestazioni simili.

Un'unità di lunghezza assoluta specifica una misura assoluta, ad esempio pollici o centimetri. Le unità di lunghezza assoluta sono utili quando le proprietà fisiche del dispositivo di output sono note.

## <a name="other-units-of-measurement"></a>Altre unità di misura

**Emu**

L'EMU (unità metrica inglese) è l'unità di misura più piccola utile e viene usata da VML per l'archiviazione unità interna. Sono presenti 914400 EMU per pollice e 12700 EMU in un punto. Le EMUL non possono essere frazionarie.

Poiché le EKU sono definite da numeri integrali con segno a 32 bit, il numero maggiore di EMUL è di 2348 pollici (circa 59 metri o 65 piedi). Poiché le misurazioni si adattano sempre a un dispositivo di output a schermo o a pagina, saranno sempre all'interno di questo intervallo.

**Angoli**

Le misurazioni dell'angolo possono essere definite con i suffissi seguenti.



Suffisso

Fd

Gradi frazionari.

Nessuno

Degrees

deg

Degrees

rad

Radians



 

 

 