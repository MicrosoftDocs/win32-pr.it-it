---
title: Prerequisiti per lo sviluppo con DirectX
description: Quando si inizia a sviluppare un'app di Windows con DirectX, tenere presenti i prerequisiti in questa pagina. Sono incluse le tecnologie che è necessario tenere presente prima di approfondire il problema.
ms.assetid: 93f566cf-0c16-4487-9d53-dc59746e4d00
keywords:
- App DirectX, prerequisiti
- App DirectX, app di Windows Store
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d5e09484bef67546047214702fab7d2d0a5c48d
ms.sourcegitcommit: 6394972f1e8b01229db602469df6bb137e31d776
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/16/2020
ms.locfileid: "104474717"
---
# <a name="prerequisites-for-developing-with-directx"></a>Prerequisiti per lo sviluppo con DirectX

Quando si inizia a sviluppare un'app di Windows con DirectX, tenere presenti i prerequisiti in questa pagina. Sono incluse le tecnologie che è necessario tenere presente prima di approfondire il problema.

## <a name="what-should-i-know-to-develop-a-windows-game-using-directx"></a>Cosa si deve sapere per sviluppare un gioco Windows con DirectX?

Prima di iniziare a sviluppare un'app di Windows Store con DirectX, è necessario saper programmare in Windows con C++. Le app di Windows che usano DirectX sono sviluppate a un basso livello di programmazione, il che significa che l'utente sarà esposto a numerose funzionalità del sistema operativo. Sono inclusi la gestione della memoria e delle risorse e l'interfaccia per il dispositivo grafico stesso. Se non si ha familiarità con il gioco o lo sviluppo di app grafiche, è possibile trovare questo problema. Tuttavia, è anche possibile ritenerlo, perché la formazione per lo sviluppo di giochi a questo livello crea più possibilità per la progettazione e lo sviluppo di app per giochi e grafica.

Sarà anche necessario comprendere le nozioni di base della programmazione grafica 2D e 3D e della matematica, perché molte delle API da usare sono state sviluppate tenendo conto di questi principi. Se si ha familiarità con le operazioni sottostanti, sarà più semplice comprenderne i parametri e i risultati.

Come minimo, è necessario comprendere quanto segue:

-   Programmazione di Windows C/C++. Ciò significa che è possibile comprendere i puntatori e i riferimenti, gli eventi e i callback e, forse, alcune librerie comuni come ATL.
-   Programmazione Win32. È possibile comprendere come vengono create le finestre e come vengono elaborati gli eventi dell'interfaccia utente. Si comprende anche un po' di API Win32 COM ed essenziali.
-   Algebra lineare e trigonometria. Sebbene non sia fondamentale, si avrà un tempo più semplice se si ha familiarità con i concetti di queste due discipline matematiche, perché costituiscono la base di gran parte della programmazione grafica 3D.
-   Terminologia e concetti grafici di base, ad esempio bitmap, trame, vertici, mesh e Viewport.

## <a name="what-does-directx-provide-me"></a>Che cosa offre DirectX?

DirectX è il set principale di API grafiche che verrà usato per sviluppare giochi di Windows. Di seguito sono riportate le categorie di funzionalità con cui è necessario acquisire familiarità quando si decide come sviluppare il gioco.



| Libreria     | Descrizione                                                                                                                                     |
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| Direct3D    | Un set di librerie potente, orientato alle prestazioni e con accelerazione hardware per il rendering di immagini 3D.                                              |
| Direct2D    | Set di librerie grafiche 2D per la bitmap con accelerazione hardware e il disegno vettoriale 2D.                                                           |
| DirectXMath | Raccolta di operazioni matematiche comuni e ottimizzate utilizzate in grafica 2D e 3D, ad esempio operazioni di vettori e matrici.                                |
| DirectWrite | Libreria di rendering e di API di layout di testo 2D. Supporta sia l'accelerazione hardware che la rasterizzazione del software.                              |
| XAudio2     | API audio multipiattaforma di basso livello per Microsoft Windows che fornisce un'elaborazione dei segnali e una base di mixaggio audio per lo sviluppo di giochi. |
| XInput      | Raccolta che supporta vari controlli di gioco tradizionali, con particolare attenzione al modello di controller Xbox 360.                                 |



 

## <a name="what-tools-do-i-need-to-develop-a-windows-game-with-directx"></a>Quali strumenti sono necessari per sviluppare un gioco Windows con DirectX?

Per iniziare a usare questa esercitazione, è necessario:

-   Windows 8.1 o versione successiva
-   Microsoft Visual Studio 2013 o versione successiva

 

 




