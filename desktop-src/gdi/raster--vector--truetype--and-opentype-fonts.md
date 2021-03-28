---
description: Tipi di carattere raster, vettoriali, TrueType e OpenType
ms.assetid: 4fe98f04-3fb0-4a03-86c3-d0ea6f07f8f0
title: Tipi di carattere raster, vettoriali, TrueType e OpenType
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e9b4be20ac7d02075fcd5c6cdbefe9eb516ea21
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104993912"
---
# <a name="raster-vector-truetype-and-opentype-fonts"></a>Tipi di carattere raster, vettoriali, TrueType e OpenType

Per visualizzare e stampare il testo, le applicazioni possono utilizzare quattro tipi diversi di tecnologie per i tipi di carattere:

-   Raster
-   Vettore
-   TrueType
-   OpenType Microsoft

Le differenze tra questi tipi di carattere riflettono il modo in cui il *glifo* per ogni carattere o simbolo viene archiviato nel rispettivo file di risorse del tipo di carattere:

-   Nei tipi di carattere raster, un glifo è una bitmap utilizzata dal sistema per creare un singolo carattere o simbolo nel tipo di carattere.
-   Nei tipi di carattere vettoriali, un glifo è una raccolta di endpoint linea che definiscono i segmenti di linea usati dal sistema per creare un carattere o un simbolo nel tipo di carattere.
-   Nei tipi di carattere TrueType e OpenType, un glifo è una raccolta di comandi linea e curva, oltre a una raccolta di hint.

Il sistema usa i comandi linea e curva per definire il contorno della bitmap per un carattere o un simbolo nel tipo di carattere TrueType o Microsoft OpenType. Il sistema usa gli hint per regolare la lunghezza delle linee e delle forme delle curve usate per tracciare il carattere o il simbolo. Questi hint e le rispettive regolazioni sono basati sulla quantità di scalabilità utilizzata per ridurre o aumentare le dimensioni della bitmap. Un tipo di carattere OpenType è equivalente a un tipo di carattere TrueType, ad eccezione del fatto che un tipo di carattere OpenType consente le definizioni del glifo del PostScript oltre alle definizioni del glifo

Poiché le bitmap per ogni glifo in un tipo di carattere raster sono progettate per una risoluzione specifica del dispositivo, i tipi di carattere raster vengono in genere considerati dipendenti dal dispositivo. I tipi di carattere vettoriali, d'altra parte, non sono dipendenti dal dispositivo, perché ogni glifo viene archiviato come una raccolta di righe scalabili. Tuttavia, i tipi di carattere vettoriali vengono generalmente disegnati più lentamente dei tipi di carattere raster o TrueType e OpenType. I tipi di carattere TrueType e OpenType forniscono una velocità di disegno relativamente rapida e un'indipendenza reale del dispositivo. Utilizzando gli hint associati a un glifo, uno sviluppatore può ridimensionare i caratteri da un tipo di carattere TrueType o OpenType verso l'alto o verso il basso e mantenerne la forma originale.

Come indicato in precedenza, i glifi per un tipo di carattere vengono archiviati in un file di risorse del tipo di carattere. Un file di risorse del tipo di carattere è in realtà una DLL che contiene solo dati, ma non è presente alcun codice. Per i tipi di carattere raster e vettoriali, questi dati sono divisi in due parti: un'intestazione che descrive le metriche del tipo di carattere e i dati del glifo. Un file di risorse dei tipi di carattere per un tipo di carattere raster o Vector viene identificato dall'estensione di file FON. Per i tipi di carattere TrueType e OpenType sono disponibili due file per ogni tipo di carattere: il primo file contiene un'intestazione relativamente breve e il secondo contiene i dati effettivi sui tipi di carattere. Il primo file è identificato da un'estensione. UFT e il secondo è identificato da un'estensione. ttf.

 

 



