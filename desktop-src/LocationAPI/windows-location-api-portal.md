---
description: API di posizione
ms.assetid: 0182461a-df06-46ea-a9c2-7aedbde5033b
title: API di posizione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3e9dccf5f88da1c608cfbc03898899f171a2627
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110889"
---
# <a name="location-api"></a>API di posizione

\[L'API Percorso Win32 ed è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile. Usare invece l'API [**Windows.Devices.Geolocation.**](/uwp/api/Windows.Devices.Geolocation) Per accedere alla posizione da un sito Web, usare [l'API di georilevazione W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). \]

## <a name="purpose"></a>Scopo

I computer sono oggi più mobili che mai. Da portatili di piccole dimensioni a Tablet PC, molti computer possono andare ovunque l'utente voglia andare. I programmi che sfruttano la mobilità del computer possono aggiungere valore significativo alla vita delle persone. Ad esempio, un programma in grado di trovare ristoranti nelle vicinanze e fornire indicazioni stradali sembra essere una misura naturale per un computer portatile. Ma anche se la tecnologia per determinare la posizione corrente dell'utente è comune e conveniente, la creazione di soluzioni su questa tecnologia può essere un'attività difficile.

Per creare un programma in grado di riconoscere la posizione, potrebbe essere necessario risolvere diversi problemi, tra cui:

-   Dispositivi GPS (Global Positioning System) che usano porte COM virtuali, che forniscono l'accesso a un solo programma alla volta.
-   Informazioni e programmazione per i protocolli, ad esempio la specifica NMEA (National Marine Electronics Association), nonché le estensioni del fornitore proprietario.
-   Limitarsi alla programmazione per soluzioni hardware verticali note.
-   Implementazione della logica per gestire le transizioni tra vari provider di posizione, ad esempio ricevitori GPS, reti connesse, reti telefoniche cellulari, Internet e impostazioni utente.

Questa documentazione descrive l'API (Application Programming Interface) del percorso di Windows. L'API Location consente di semplificare la programmazione in grado di riconoscere la posizione fornendo un modo standard per recuperare i dati sulla posizione utente e standardizzare i formati per i report dei dati di posizione. L'API Location gestisce automaticamente le transizioni tra i provider di dati di posizione e sceglie sempre il provider più accurato per la situazione corrente.

## <a name="developer-audience"></a>Sviluppatori

L'API Location fornisce le funzionalità tramite un set di interfacce COM. La funzionalità dell'API Location può essere usata dai programmatori che hanno familiarità con l'uso di COM tramite il linguaggio di programmazione C++ o con gli oggetti COM nei linguaggi di scripting, ad esempio Microsoft JScript.

## <a name="in-this-section"></a>Contenuto della sezione

-   [Informazioni di riferimento sulla programmazione C++ dell'API Location](windows-location-programming-reference.md)
-   [Informazioni di riferimento sul modello a oggetti dell'API Location](windows-location-script-programming-reference.md)

 

 
