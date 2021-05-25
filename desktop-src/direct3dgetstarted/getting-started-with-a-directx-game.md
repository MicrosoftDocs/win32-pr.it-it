---
title: Introduzione a DirectX per Windows
description: La creazione di un gioco Microsoft DirectX per Windows è una sfida per un nuovo sviluppatore. Qui vengono esaminati rapidamente i concetti coinvolti e i passaggi da eseguire per iniziare a sviluppare un gioco usando DirectX e C++.
ms.assetid: fd460c52-9854-4ffe-b89e-5219be2e11f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bac8ca2805fed9ec42faf9deda9ddd51da39685
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343586"
---
# <a name="get-started-with-directx-for-windows"></a>Introduzione a DirectX per Windows

La creazione di un gioco Microsoft DirectX per Windows è una sfida per un nuovo sviluppatore. Qui vengono esaminati rapidamente i concetti coinvolti e i passaggi da eseguire per iniziare a sviluppare un gioco usando DirectX e C++.

A questo punto, procedere con l'esercitazione.

## <a name="what-skills-do-you-need"></a>Quali competenze sono necessarie?

Per sviluppare un gioco in DirectX per Windows, è necessario avere alcune competenze di base. In particolare, è necessario essere in grado di:

-   Leggere e scrivere codice C++ moderno (C++11 è più utile) e acquisire familiarità con i principi e i modelli di progettazione C++ di base, ad esempio i modelli e il modello factory. È anche necessario avere familiarità con le librerie C++ comuni, ad esempio la libreria di modelli standard, in particolare con gli operatori di cast, i tipi di puntatore e le strutture di dati della libreria modello standard (ad esempio std::vector).
-   Comprendere la geometria di base, la trigonometria e l'algebra lineare. Gran parte del codice che si trova negli esempi presuppone che si comprendino queste forme di matematica e le relative regole comuni.
-   Avere familiarità con COM, in particolare [**Microsoft::WRL::ComPtr**](/previous-versions/visualstudio/visual-studio-2012/br244983(v=vs.110)) (puntatore intelligente).
-   Comprendere le basi della tecnologia grafica e grafica, in particolare la grafica 3D. Anche se DirectX stesso ha una propria terminologia, si basa ancora su una conoscenza consolidata dei principi generali della grafica 3D.
-   Comprendere il concetto di ciclo di messaggi, perché verrà implementato un ciclo in ascolto sul sistema operativo Windows.

## <a name="and-were-off"></a>E siamo spenti.

Sei pronto per iniziare? Si esamini prima di procedere. Precisamente:

-   Un'installazione aggiornata e funzionante di Windows 8.1.
-   Installazione di [Microsoft Visual Studio](https://visualstudio.microsoft.com/downloads/download-visual-studio-vs).
-   Un'intrepida voglia di saperne di più sullo sviluppo di giochi DirectX.

## <a name="next-steps"></a>Passaggi successivi



| Argomento                                                                                                   | Descrizione                                                                                                           |
|----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [Usare le risorse del dispositivo DirectX](work-with-dxgi.md)                                           | Informazioni su come usare DXGI per creare un dispositivo grafico virtualizzato e creare e configurare una catena di scambio.     |
| [Informazioni sulla pipeline di rendering Direct3D 11](understand-the-directx-11-2-graphics-pipeline.md) | Informazioni su come eseguire l'hook alla classe delle risorse del dispositivo DirectX e disegnare usando la pipeline grafica Direct3D. |
| [Usare shader e risorse shader](work-with-shaders-and-shader-resources.md)               | Informazioni su come scrivere programmi shader HLSL per le fasi della pipeline grafica Direct3D.                            |



 

 

 