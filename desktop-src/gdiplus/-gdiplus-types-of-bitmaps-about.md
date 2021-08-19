---
description: Una bitmap è una matrice di bit che specifica il colore di ogni pixel in una matrice rettangolare di pixel.
ms.assetid: fac60d01-d07e-41e9-98a3-34c592d97a92
title: Tipi di bitmap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0503bec0f8b029e373ff414b51a60c3b1201a37b9151b722cdfc94d4cdea46cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118977301"
---
# <a name="types-of-bitmaps"></a>Tipi di bitmap

Una bitmap è una matrice di bit che specifica il colore di ogni pixel in una matrice rettangolare di pixel. Il numero di bit dedicati a un singolo pixel determina il numero di colori che possono essere assegnati a tale pixel. Ad esempio, se ogni pixel è rappresentato da 4 bit, a un determinato pixel può essere assegnato uno dei 16 colori diversi (2^4 = 16). La tabella seguente illustra alcuni esempi del numero di colori che possono essere assegnati a un pixel rappresentato da un determinato numero di bit.



| Bit per pixel | Numero di colori che possono essere assegnati a un pixel |
|----------------|--------------------------------------------------|
| 1              | 2^1 = 2                                          |
| 2              | 2^2 = 4                                          |
| 4              | 2^4 = 16                                         |
| 8              | 2^8 = 256                                        |
| 16             | 2^16 = 65,536                                    |
| 24             | 2^24 = 16, 777, 216                              |



 

I file su disco che archiviano bitmap contengono in genere uno o più blocchi di informazioni che archiviano informazioni quali il numero di bit per pixel, il numero di pixel in ogni riga e il numero di righe nella matrice. Un file di questo tipo può contenere anche una tabella dei colori (talvolta denominata tavolozza dei colori). Una tabella dei colori esegue il mapping dei numeri nella bitmap a colori specifici. La figura seguente mostra un'immagine ingrandita insieme alla relativa bitmap e tabella dei colori. Ogni pixel è rappresentato da un numero a 4 bit, quindi nella tabella dei colori sono presenti 2^4 = 16 colori. Ogni colore nella tabella è rappresentato da un numero a 24 bit: 8 bit per il rosso, 8 bit per il verde e 8 bit per il blu. I numeri vengono visualizzati in formato esadecimale (base 16): A = 10, B = 11, C = 12, D = 13, E = 14, F = 15.

![figura che mostra una matrice di numeri, un'immagine e una tabella che corrisponde ai numeri di matrice ai colori](images/aboutgdip03-art01.png)

Esaminare il pixel nella riga 3, colonna 5 dell'immagine. Il numero corrispondente nella bitmap è 1. La tabella dei colori indica che 1 rappresenta il colore rosso, quindi il pixel è rosso. Tutte le voci nella riga superiore della bitmap sono 3. La tabella dei colori indica che 3 rappresenta il blu, quindi tutti i pixel nella riga superiore dell'immagine sono blu.

> [!Note]  
> Alcune bitmap vengono archiviate in formato bottom-up. i numeri nella prima riga della bitmap corrispondono ai pixel nella riga inferiore dell'immagine.

 

Una bitmap che archivia gli indici in una tabella dei colori è detta *bitmap indicizzata con* tavolozza. Alcune bitmap non hanno bisogno di una tabella dei colori. Ad esempio, se una bitmap usa 24 bit per pixel, tale bitmap può archiviare i colori anziché gli indici in una tabella dei colori. La figura seguente mostra una bitmap che archivia i colori direttamente (24 bit per pixel) anziché usare una tabella dei colori. La figura mostra anche una visualizzazione ingrandita dell'immagine corrispondente. Nella bitmap, FFFFFF rappresenta il bianco, FF0000 rappresenta il rosso, 00FF00 rappresenta il verde e 0000FF rappresenta il blu.

![illustrazione di una matrice di valori esadecimali, seguita dall'immagine bitmap che i numeri rappresentano](images/aboutgdip03-art02.png)

 

## <a name="graphics-file-formats"></a>Formati di file di grafica

Esistono molti formati standard per il salvataggio di bitmap nei file. Windows GDI+ supporta i formati di file grafici descritti nei paragrafi seguenti.

**Bitmap (BMP)**

BMP è un formato standard usato da Windows per archiviare immagini indipendenti dal dispositivo e indipendenti dall'applicazione. Il numero di bit per pixel (1, 4, 8, 15, 24, 32 o 64) per un determinato file BMP viene specificato in un'intestazione di file. I file BMP con 24 bit per pixel sono comuni.

**Graphics Interchange Format (GIF)**

GIF è un formato comune per le immagini visualizzate nelle pagine Web. Le GIF funzionano bene per i disegni a linee, le immagini con blocchi di colore a tinta unita e le immagini con limiti netti tra i colori. Le GIF vengono compresse, ma non vengono perse informazioni nel processo di compressione. un'immagine decompressa è esattamente la stessa dell'originale. Un colore in una GIF può essere designato come trasparente, in modo che l'immagine abbia il colore di sfondo di qualsiasi pagina Web che la visualizza. Una sequenza di immagini GIF può essere archiviata in un singolo file per formare un'immagine GIF animata. Le GIF archiviano al massimo 8 bit per pixel, quindi sono limitate a 256 colori.

**Joint Photographic Experts Group (JPEG)**

JPEG è uno schema di compressione che funziona bene per le scene naturali, ad esempio le foto digitalizzate. Alcune informazioni vengono perse nel processo di compressione, ma spesso la perdita è impercettibile per l'occhio umano. Le immagini JPEG a colori archiviano 24 bit per pixel, in modo che siano in grado di visualizzare più di 16 milioni di colori. Esiste anche un formato JPEG in scala di grigi che archivia 8 bit per pixel. I file JPEG non supportano la trasparenza o l'animazione.

Il livello di compressione nelle immagini JPEG è configurabile, ma i livelli di compressione più elevati (file più piccoli) comportano una perdita maggiore di informazioni. Un rapporto di compressione di 20:1 spesso produce un'immagine che l'occhio umano trova difficile distinguere dall'originale. La figura seguente mostra un'immagine BMP e due immagini JPEG compresse da tale immagine BMP. Il primo JPEG ha un rapporto di compressione di 4:1 e il secondo JPEG ha un rapporto di compressione di circa 8:1.

![figura che mostra un'immagine bitmap e due compressioni jpeg dell'immagine; la compressione più elevata presenta più variazioni rispetto all'originale](images/aboutgdip03-art03.png)

La compressione JPEG non funziona bene per i disegni a linee, i blocchi di colore a tinta unita e i limiti acuti. La figura seguente mostra un BMP insieme a due JPEG e a una GIF. I file JPEG e i file GIF sono stati compressi dal BMP. Il rapporto di compressione è 4:1 per il file GIF, 4:1 per jpeg più piccolo e 8:3 per il formato JPEG più grande. Si noti che la GIF mantiene i limiti netti lungo le linee, ma gli JPEG tendono a sfocare i limiti.

![illustrazione che confronta una bitmap di un disegno a linee con due equivalenti jpeg e una gif; la gif mantiene al meglio il colore e la nitidezza delle linee](images/aboutgdip03-art03a.png)

JPEG è uno schema di compressione, non un formato di file. Jpeg File Interchange Format (JFIF) è un formato di file comunemente usato per l'archiviazione e il trasferimento di immagini compresse in base a uno schema JPEG. I file JFIF visualizzati dai Web browser usano l'.jpg predefinita.

**File di immagine scambiabile (Exif)**

Exif è un formato di file usato per le fotocamere digitali. Un file Exif contiene un'immagine compressa in base alla specifica JPEG. Un file Exif contiene anche informazioni sulla fotografia (data scattata, velocità dell'otturatore, tempo di esposizione e così via) e informazioni sulla fotocamera (produttore, modello e così via).

**Portable Network Graphics (PNG)**

Il formato PNG mantiene molti dei vantaggi del formato GIF, ma offre anche funzionalità oltre a quelle del formato GIF. Come i file GIF, i file PNG vengono compressi senza perdita di informazioni. I file PNG possono archiviare colori con 8, 24 o 48 bit per pixel e scale di grigi con 1, 2, 4, 8 o 16 bit per pixel. Al contrario, i file GIF possono usare solo 1, 2, 4 o 8 bit per pixel. Un file PNG può anche archiviare un valore alfa per ogni pixel, che specifica il grado di fusione del colore del pixel con il colore di sfondo.

PNG migliora la gif nella possibilità di visualizzare progressivamente un'immagine; in altri, per visualizzare approssimazioni migliori e migliori dell'immagine quando arriva tramite una connessione di rete. I file PNG possono contenere informazioni sulla correzione gamma e la correzione del colore in modo che sia possibile eseguire il rendering accurato delle immagini in un'ampia gamma di dispositivi di visualizzazione.

**Formato file di immagine tag (TIFF)**

TIFF è un formato flessibile ed estensibile supportato da un'ampia gamma di piattaforme e applicazioni di elaborazione delle immagini. I file TIFF possono archiviare immagini con un numero arbitrario di bit per pixel e possono usare un'ampia gamma di algoritmi di compressione. È possibile archiviare diverse immagini in un singolo file TIFF a più pagine. Le informazioni relative all'immagine (make scanner, computer host, tipo di compressione, orientamento, campioni per pixel e così via) possono essere archiviate nel file e disposte tramite l'uso di tag. Il formato TIFF può essere esteso in base alle esigenze con l'approvazione e l'aggiunta di nuovi tag.

 

 



