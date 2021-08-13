---
description: Funzionalità video
ms.assetid: 305bd009-f58e-4dcc-9b70-252de87dc86d
title: Funzionalità video
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4841f5f33b39adc6bd12775e07085e14886d250cd59c988884ae7ca8a6a21b80
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119290865"
---
# <a name="video-capabilities"></a>Funzionalità video

Il [**metodo IAMStreamConfig::GetStreamCaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) presenta funzionalità video in una matrice di coppie di strutture [**AM MEDIA \_ \_ TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) e [**VIDEO STREAM CONFIG \_ \_ \_ CAPS.**](/windows/win32/api/strmif/ns-strmif-video_stream_config_caps) È possibile usarlo per esporre tutti i formati e le risoluzioni supportati in un pin, come illustrato di seguito.

Per esempi relativi all'audio di **GetStreamCaps,** vedere [Funzionalità audio.](audio-capabilities.md)

Si supponga che la scheda di acquisizione supporti il formato JPEG a tutte le risoluzioni comprese tra 160 x 120 pixel e 320 x 240 pixel, inclusi. La differenza tra le risoluzioni supportate è una in questo caso perché si aggiunge o sottrae un pixel da ogni risoluzione supportata per ottenere la risoluzione supportata successiva. Questa differenza nelle risoluzioni supportate è detta granularità.

Si supponga che la scheda supporti anche le dimensioni 640 x 480. Di seguito viene illustrata questa risoluzione singola e l'intervallo di risoluzioni precedente (tutte le dimensioni tra 160 x 120 pixel e 320 x 240 pixel).

![risoluzione da 160 x 120 a 320 x 240 pixel, più 640 x 480](images/strmcap1.png)

Si supponga anche che supporti il formato RGB a 24 bit a colori con risoluzioni tra 160 x 120 e 320 x 240, ma con una granularità di 8. La figura seguente mostra alcune delle dimensioni valide in questo caso.

![risoluzione da 160 x 120 a 320 a 240, con granularità = 8](images/strmcap3.png)

In altre parole ed elencando altre risoluzioni, di seguito sono elencate tutte le risoluzioni valide.

-   160 x 120
-   168 x 120
-   168 x 128
-   176 x 128
-   176 x 136
-   ... risoluzioni aggiuntive ...
-   312 x 232
-   320 x 240

Usare **GetStreamCaps** per esporre queste funzionalità di dimensioni e formati di colore offrendo un tipo di supporto di 320 x 240 JPEG (se si tratta della dimensione predefinita o preferita) abbinato a funzionalità minime di 160 x 120, capacità massime di 320 x 240 e granularità di 1. La coppia successiva esponga tramite **GetStreamCaps** è un tipo di supporto di 640 x 480 JPEG associato a un minimo di 640 x 480 e un massimo di 640 x 480 e una granularità pari a 0. La terza coppia include un tipo di supporto di 320 x 240, RGB a 24 bit con funzionalità minime di 160 x 120, funzionalità massime di 320 x 240 e granularità di 8. In questo modo è possibile pubblicare quasi tutti i formati e le funzionalità che la scheda potrebbe supportare. Un'applicazione che deve conoscere i formati di compressione forniti può ottenere tutte le coppie e creare un elenco di tutti i sottotipi univoci dei tipi di supporti.

Un filtro ottiene i rettangoli di origine e di destinazione del tipo di supporto rispettivamente dai membri **rcSource** e **rcTarget** della struttura [**VIDEOINFOHEADER.**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) I filtri non devono supportare rettangoli di origine e destinazione.

Il rettangolo di ritaglio descritto nella documentazione [**di IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) è uguale al rettangolo **rcSource** della struttura **VIDEOINFOHEADER** per il pin di output.

Il rettangolo di output descritto in tutta la documentazione **di IAMStreamConfig** è uguale ai membri **biWidth** e **biHeight** della struttura **BITMAPINFOHEADER** del pin di output (vedere Dati DV nel formato [di file AVI).](dv-data-in-the-avi-file-format.md)

Se il segnaposto di output di un filtro è connesso a un tipo di supporto con rettangoli di origine e destinazione non erppi, il filtro deve estendere il sottorettangolo di origine del formato di input nel sottorectangle di destinazione del formato di output. Il sottorectangle di origine viene archiviato nel membro **InputSize** della struttura [**VIDEO STREAM CONFIG \_ \_ \_ CAPS.**](/windows/win32/api/strmif/ns-strmif-video_stream_config_caps)

Si consideri, ad esempio, lo scenario video seguente: l'immagine di input è in formato RGB e ha una dimensione di 160 x 120 pixel. L'angolo superiore sinistro del rettangolo di origine è in corrispondenza della coordinata (20,20) e l'angolo inferiore destro è in corrispondenza di (30,30). L'immagine di output è in formato MPEG con dimensioni di 320 x 240. L'angolo superiore sinistro del rettangolo di destinazione è (0,0) e l'angolo inferiore destro è in corrispondenza di (100,100). In questo caso, il filtro deve prendere una parte 10 x 10 della bitmap di origine da 160 x 120 RGB e riempire l'area 100 x 100 superiore di una bitmap 320 x 240, lasciando invariato il resto della bitmap 320 x 240. Nella figura seguente viene illustrato questo scenario.

![estensione subrectangle](images/strmcap4.png)

Un filtro potrebbe non supportare questa operazione e potrebbe non riuscire a connettersi con un tipo di supporto in cui **rcSource** e **rcTarget** non sono vuoti.

La **struttura VIDEOINFOHEADER** espone informazioni sulle funzionalità di velocità dei dati di un filtro. Si supponga, ad esempio, di aver connesso il pin di output al filtro successivo con un determinato tipo di supporto (direttamente o usando il tipo di supporto passato dalla [**funzione CMediaType::SetFormat).**](cmediatype-setformat.md) Esaminare il membro **dwBitRate** della struttura di formato **VIDEOINFOHEADER** del tipo di supporto per vedere la frequenza dei dati in cui comprimere il video. Se si moltiplica il numero di unità di tempo per fotogramma nel membro **AvgTimePerFrame** della struttura **VIDEOINFOHEADER** per la velocità dei dati nel membro **dwBitRate** e si divide per 10.000.000 (il numero di unità al secondo), è possibile determinare il numero di byte che ogni frame deve essere. È possibile produrre un frame di dimensioni inferiori, ma mai un frame più grande. Per determinare la frequenza dei fotogrammi per un video o un filtro di acquisizione, usare **AvgTimePerFrame** dal tipo di supporto del pin di output.

 

 



