---
title: Introduzione a DirectX per Windows
description: La creazione di un gioco Microsoft DirectX per Windows è una sfida per un nuovo sviluppatore. In questo articolo vengono esaminati rapidamente i concetti e i passaggi necessari per iniziare lo sviluppo di un gioco con DirectX e C++.
ms.assetid: fd460c52-9854-4ffe-b89e-5219be2e11f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae09cd127a30401ae0493f5dd770fe1e67607b45
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300000"
---
# <a name="get-started-with-directx-for-windows"></a>Introduzione a DirectX per Windows

La creazione di un gioco Microsoft DirectX per Windows è una sfida per un nuovo sviluppatore. In questo articolo vengono esaminati rapidamente i concetti e i passaggi necessari per iniziare lo sviluppo di un gioco con DirectX e C++.

A questo punto, procedere con l'esercitazione.

## <a name="what-skills-do-you-need"></a>Quali competenze sono necessarie?

Per sviluppare un gioco in DirectX per Windows, è necessario disporre di alcune competenze di base. In particolare, è necessario essere in grado di:

-   Leggi e Scrivi codice C++ moderno (C++ 11 più semplice) ed è familiare con i principi di progettazione e i modelli di base di C++, come i modelli e il modello Factory. È anche necessario avere familiarità con le librerie C++ comuni, come la libreria di modelli standard, e in particolare con gli operatori di cast, i tipi di puntatore e le strutture di dati della libreria di modelli standard, ad esempio std:: Vector.
-   Informazioni sulla geometria di base, sulla trigonometria e sull'algebra lineare. Gran parte del codice che si troverà negli esempi presuppone che si conoscano queste forme di matematica e le regole comuni.
-   Hanno familiarità con COM, in particolare [**Microsoft:: WRL:: ComPtr**](/previous-versions/visualstudio/visual-studio-2012/br244983(v=vs.110)) (puntatore intelligente).
-   Informazioni sulle fondamenta della grafica e della tecnologia grafica, in particolare grafica 3D. Sebbene DirectX abbia una propria terminologia, si basa comunque su una conoscenza ben definita dei principi grafici 3D generali.
-   Comprendere il concetto di ciclo di messaggi perché verrà implementato un ciclo che resta in ascolto del sistema operativo Windows.

## <a name="and-were-off"></a>E ci siamo disattivati.

Sei pronto per iniziare? Esaminiamo prima di tutto. Precisamente:

-   Installazione aggiornata e funzionante di Windows 8.1.
-   Installazione di [Microsoft Visual Studio](https://visualstudio.microsoft.com/downloads/download-visual-studio-vs).
-   Uno spirito intrepido e il desiderio di saperne di più sullo sviluppo di giochi DirectX.

## <a name="next-steps"></a>Passaggi successivi



|                                                                                                    |                                                                                                           |
|----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [Usare le risorse del dispositivo DirectX](work-with-dxgi.md)                                           | Informazioni su come usare DXGI per creare un dispositivo di grafica virtualizzato e creare e configurare una catena di scambio.     |
| [Informazioni sulla pipeline di rendering Direct3D 11](understand-the-directx-11-2-graphics-pipeline.md) | Informazioni su come collegare la classe delle risorse del dispositivo DirectX e creare usando la pipeline grafica Direct3D. |
| [Usare shader e risorse shader](work-with-shaders-and-shader-resources.md)               | Informazioni su come scrivere programmi shader HLSL per le fasi della pipeline grafica Direct3D.                            |



 

 

 