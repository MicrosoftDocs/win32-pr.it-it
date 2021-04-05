---
description: .
ms.assetid: 0182461a-df06-46ea-a9c2-7aedbde5033b
title: API location
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f643565e80f72ffcefe6981c924b3739b1c4f5f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881517"
---
# <a name="location-api"></a>API location

\[L'API del percorso Win32 ed è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile. Usare invece l'API [**Windows. Devices. Geolocation**](/uwp/api/Windows.Devices.Geolocation) . Per accedere a location da un sito Web, usare l' [API di georilevazione W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). \]

## <a name="purpose"></a>Scopo

I computer oggi sono più mobili che mai. Da piccoli portatili a Tablet PC, molti computer possono andare ovunque si trovino. I programmi che sfruttano i vantaggi della mobilità del computer possono aggiungere un valore significativo alla vita degli utenti. Ad esempio, un programma in grado di trovare ristoranti vicini e fornire indicazioni di guida sembrerebbe una scelta naturale per un computer portatile. Tuttavia, mentre la tecnologia per determinare la posizione corrente dell'utente è comune e conveniente, la creazione di soluzioni su questa tecnologia può essere un'attività complessa.

Per creare un programma in grado di riconoscere la posizione, potrebbe essere necessario superare una serie di problemi, tra cui:

-   Dispositivi GPS (Global Positioning System) che usano porte COM virtuali, che forniscono l'accesso a un solo programma alla volta.
-   Informazioni e programmazione per i protocolli, ad esempio la specifica National Marine Electronics Association (NMEA), nonché le estensioni del fornitore proprietarie.
-   Essere limitati alla programmazione per soluzioni hardware note e verticali.
-   Implementazione della logica per gestire le transizioni tra diversi provider di località, ad esempio ricevitori GPS, reti connesse, reti telefoniche cellulari, Internet e impostazioni utente.

Questa documentazione descrive il percorso di Windows Application Programming Interface (API). L'API location consente di semplificare la programmazione in base alla posizione fornendo un metodo standard per recuperare i dati sulla posizione dell'utente e i formati di standardizzazione per i report dei dati sulla posizione. L'API location gestisce automaticamente le transizioni tra i provider di dati della posizione e sceglie sempre il provider più accurato per la situazione corrente.

## <a name="developer-audience"></a>Sviluppatori

L'API Location fornisce le funzionalità tramite un set di interfacce COM. Le funzionalità dell'API location possono essere usate dai programmatori che hanno familiarità con l'uso di COM tramite il linguaggio di programmazione C++ o con l'uso di oggetti COM in linguaggi di scripting, ad esempio Microsoft JScript.

## <a name="in-this-section"></a>Contenuto della sezione

-   [Riferimento per la programmazione dell'API location C++](windows-location-programming-reference.md)
-   [Riferimento al modello a oggetti dell'API location](windows-location-script-programming-reference.md)

 

 
