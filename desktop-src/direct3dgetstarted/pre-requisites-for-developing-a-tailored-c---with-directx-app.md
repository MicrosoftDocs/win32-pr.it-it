---
title: Prerequisiti per lo sviluppo con DirectX
description: Quando si inizia a sviluppare un Windows app con DirectX, tenere presenti i prerequisiti in questa pagina. Sono incluse le tecnologie che è necessario conoscere prima di approfondire.
ms.assetid: 93f566cf-0c16-4487-9d53-dc59746e4d00
keywords:
- App DirectX, prerequisiti
- App DirectX, app Windows Store
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 870c575fc24da5632582e30b9786d8c800161e5ad1a1cfbc765aa5ec33db3f94
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119950991"
---
# <a name="prerequisites-for-developing-with-directx"></a>Prerequisiti per lo sviluppo con DirectX

Quando si inizia a sviluppare un Windows app con DirectX, tenere presenti i prerequisiti in questa pagina. Sono incluse le tecnologie che è necessario conoscere prima di approfondire.

## <a name="what-should-i-know-to-develop-a-windows-game-using-directx"></a>Cosa è necessario sapere per sviluppare un gioco Windows con DirectX?

Prima di iniziare a sviluppare un'app Windows Store con DirectX, è necessario sapere come programmare in Windows con C++. Windows app che usano DirectX vengono sviluppate a un basso livello di programmazione, il che significa che si verrà esposti a molte funzionalità del sistema operativo. Questi includono la gestione della memoria e delle risorse e l'interfaccia per il dispositivo grafico stesso. Se non si ha esperienza con lo sviluppo di giochi o app grafiche, questa operazione potrebbe risultare complessa. Ma lo ritieni anche gratificante, perché lo sviluppo di giochi di apprendimento a questo livello crea possibilità molto più grandi per la progettazione e lo sviluppo di app per giochi e grafica.

È anche necessario comprendere le nozioni di base della programmazione grafica 2D e 3D e della matematica, perché molte delle API che verranno usate sono state sviluppate in base a questi principi. Se si ha familiarità con le operazioni alla base, sarà più facile comprendere i parametri e i risultati.

Come minimo, è necessario avere una conoscenza di quanto segue:

-   Windows Programmazione C/C++. Ciò significa che si comprendono puntatori e riferimenti, eventi e callback e forse alcune librerie comuni come ATL.
-   Programmazione Win32. Si comprende come vengono create le finestre e come vengono elaborati gli eventi dell'interfaccia utente. Sono anche disponibili informazioni su COM e sulle API Win32 essenziali.
-   Algebra lineare e trigonometria. Anche se non è essenziale, sarà più facile avere familiarità con i concetti di queste due discipline matematiche, perché sono alla base della maggior parte della programmazione grafica 3D.
-   Terminologia e concetti di base della grafica, ad esempio bitmap, trame, vertici, mesh e viewport.

## <a name="what-does-directx-provide-me"></a>Che cosa offre DirectX?

DirectX è il set principale di API grafiche che verranno usate per sviluppare Windows giochi. Ecco le categorie di funzionalità con cui è necessario acquisire familiarità quando si decide come sviluppare il gioco.



| Libreria     | Descrizione                                                                                                                                     |
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| Direct3D    | Set di librerie potente, orientato alle prestazioni e con accelerazione hardware per il rendering della grafica 3D.                                              |
| Direct2D    | Set di librerie grafiche 2D per bitmap con accelerazione hardware e disegno vettoriale 2D.                                                           |
| DirectXMath | Libreria di operazioni matematiche comuni e ottimizzate usate nella grafica 2D e 3D, ad esempio operazioni vettoriali e matrici.                                |
| DirectWrite | Una libreria di API di layout e rendering del testo 2D. Supporta sia l'accelerazione hardware che l'rasterizzazione del software.                              |
| XAudio2     | API audio multipiattaforma di basso livello per Microsoft Windows che fornisce una base per l'elaborazione dei segnali e la combinazione di audio per lo sviluppo di giochi. |
| XInput      | Libreria che supporta vari controlli di gioco tradizionali, con particolare attenzione al modello Xbox 360 controller.                                 |



 

## <a name="what-tools-do-i-need-to-develop-a-windows-game-with-directx"></a>Quali strumenti sono necessari per sviluppare un gioco Windows con DirectX?

Per iniziare a usare questa esercitazione, è necessario:

-   Windows 8.1 o versione successiva
-   Microsoft Visual Studio 2013 o versione successiva

 

 




