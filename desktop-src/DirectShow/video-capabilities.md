---
description: Funzionalità video
ms.assetid: 305bd009-f58e-4dcc-9b70-252de87dc86d
title: Funzionalità video
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6287839b75bd5044644480c3abcc8248cc46dc0a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104555497"
---
# <a name="video-capabilities"></a>Funzionalità video

Il metodo [**IAMStreamConfig:: GetStreamCaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) presenta le funzionalità video in una matrice di coppie [**di \_ \_ tipi di supporto am**](/windows/win32/api/strmif/ns-strmif-am_media_type) e di [**\_ \_ configurazione \_ del flusso video**](/windows/win32/api/strmif/ns-strmif-video_stream_config_caps) . È possibile usarlo per esporre tutti i formati e le risoluzioni supportati in un PIN, come descritto di seguito.

Per esempi relativi all'audio di **GetStreamCaps**, vedere [funzionalità audio](audio-capabilities.md).

Si supponga che la scheda di acquisizione supporti il formato JPEG con tutte le risoluzioni comprese tra 160 x 120 pixel e 320 x 240 pixel, inclusi. La differenza tra le risoluzioni supportate è una in questo caso perché si aggiunge o si sottrae un pixel da ogni risoluzione supportata per ottenere la risoluzione successiva supportata. Questa differenza nelle risoluzioni supportate è detta granularità.

Si supponga che la scheda supporti anche le dimensioni 640 x 480. Di seguito viene illustrata questa singola risoluzione e l'intervallo di risoluzioni precedente (tutte le dimensioni comprese tra 160 x 120 pixel e 320 x 240 pixel).

![risoluzione da 160 x 120 a 320 x 240 pixel, più 640 x 480](images/strmcap1.png)

Si supponga inoltre che supporti il formato RGB a 24 bit alle risoluzioni comprese tra 160 x 120 e 320 x 240, ma con una granularità pari a 8. Nella figura seguente vengono illustrate alcune delle dimensioni valide in questo caso.

![risoluzione da 160 x 120 a 320 a 240, con granularità = 8](images/strmcap3.png)

Per metterlo in un altro modo e elencare altre soluzioni, di seguito sono elencate tutte le soluzioni valide.

-   160 x 120
-   168 x 120
-   168 x 128
-   176 x 128
-   176 x 136
-   ... ulteriori risoluzioni...
-   312 x 232
-   320 x 240

Usare **GetStreamCaps** per esporre le funzionalità relative al formato colori e alla dimensione offrendo un tipo di supporto di 320 x 240 JPEG (se le dimensioni predefinite o preferite) sono abbinate alle funzionalità minime di 160 x 120, alle capacità massime di 320 x 240 e a una granularità pari a 1. La coppia successiva esposta tramite **GetStreamCaps** è un tipo di supporto di 640 x 480 JPEG accoppiato con un minimo di 640 x 480 e un massimo di 640 x 480 e una granularità pari a 0. La terza coppia include un tipo di supporto di 320 x 240, RGB a 24 bit con funzionalità minime di 160 x 120, capacità massima di 320 x 240 e una granularità pari a 8. In questo modo è possibile pubblicare quasi tutti i formati e le funzionalità che la scheda potrebbe supportare. Un'applicazione che deve conoscere i formati di compressione forniti può ottenere tutte le coppie e creare un elenco di tutti i sottotipi univoci dei tipi di supporto.

Un filtro ottiene i rettangoli di origine e di destinazione del tipo di supporto rispettivamente dai membri **rcSource** e **RcTarget** della struttura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) . I filtri non devono supportare i rettangoli di origine e di destinazione.

Il rettangolo di ritaglio descritto in tutta la documentazione di [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) è uguale al rettangolo **RcSource** della struttura **VIDEOINFOHEADER** per il pin di output.

Il rettangolo di output descritto nella documentazione di **IAMStreamConfig** è identico a quello dei membri **biWidth** e **biHeight** della struttura **BITMAPINFOHEADER** del PIN di output. vedere la pagina relativa ai [dati DV nel formato di file AVI](dv-data-in-the-avi-file-format.md).

Se un pin di output di un filtro è connesso a un tipo di supporto con rettangoli di origine e di destinazione non vuoti, il filtro è necessario per estendere il sottorettangolo di origine del formato di input nel sottorettangolo di destinazione del formato di output. Il sottorettangolo di origine viene archiviato nel membro **InputSize** della struttura [**\_ Caps di \_ configurazione \_ del flusso video**](/windows/win32/api/strmif/ns-strmif-video_stream_config_caps) .

Si consideri, ad esempio, lo scenario di compressione video seguente: l'immagine di input è in formato RGB e ha una dimensione di 160 x 120 pixel. L'angolo superiore sinistro del rettangolo di origine è in corrispondenza della coordinata (20, 20) e nell'angolo inferiore destro si trova in corrispondenza di (30, 30). L'immagine di output è in formato MPEG con una dimensione di 320 x 240. L'angolo superiore sinistro del rettangolo di destinazione si trova in corrispondenza di (0, 0) e l'angolo inferiore destro è pari a (100.100). In questo caso, il filtro deve prendere un pezzo da 10 x 10 della bitmap di origine RGB 160 x 120 e riempirlo con l'area superiore 100 x 100 di una bitmap 320 x 240, lasciando invariato il resto della bitmap 320 x 240. Nella figura seguente viene illustrato questo scenario.

![estensione del sottorettangolo](images/strmcap4.png)

Un filtro potrebbe non supportare questa operazione e può non riuscire a connettersi con un tipo di supporto in cui **rcSource** e **rcTarget** non sono vuoti.

La struttura **VIDEOINFOHEADER** espone informazioni sulle funzionalità della velocità dei dati di un filtro. Si supponga, ad esempio, di aver connesso il pin di output al filtro successivo con un determinato tipo di supporto, direttamente o usando il tipo di supporto passato dalla funzione [**CMediaType:: Seformat**](cmediatype-setformat.md) . Esaminare il membro **dwBitRate** della struttura del formato **VIDEOINFOHEADER** del tipo di supporto per visualizzare la velocità dei dati in cui si deve comprimere il video. Se si moltiplica il numero di unità di tempo per fotogramma nel membro **AvgTimePerFrame** della struttura **VIDEOINFOHEADER** per la velocità dati nel membro **dwBitRate** e si divide per 10 milioni (numero di unità al secondo), è possibile determinare il numero di byte che ciascun frame deve avere. È possibile produrre un frame di dimensioni inferiori, ma mai uno più grande. Per determinare la frequenza dei fotogrammi per un commediatore video o per un filtro di acquisizione, usare **AvgTimePerFrame** dal tipo di supporto del PIN di output.

 

 



