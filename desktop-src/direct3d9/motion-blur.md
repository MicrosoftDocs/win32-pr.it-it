---
description: È possibile migliorare la velocità percepita di un oggetto in una scena 3D sfocatura dell'oggetto e lasciando una traccia sfocata di immagini dell'oggetto dietro l'oggetto. A tale scopo, le applicazioni Direct3D estrarre l'oggetto più volte per frame.
ms.assetid: 8b1a1f0d-5857-4ab4-828c-8ca7c17a4890
title: Sfocatura movimento (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3daa0b35a0c375cc798b619f18f1e363001050de4dcc950e6c6828a7d365801
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119628321"
---
# <a name="motion-blur-direct3d-9"></a>Sfocatura movimento (Direct3D 9)

È possibile migliorare la velocità percepita di un oggetto in una scena 3D sfocatura dell'oggetto e lasciando una traccia sfocata di immagini dell'oggetto dietro l'oggetto. A tale scopo, le applicazioni Direct3D estrarre l'oggetto più volte per frame.

Tenere conto del fatto che le applicazioni Direct3D in genere eseguono il rendering delle scene in un buffer fuori schermo. Il contenuto del buffer viene visualizzato sullo schermo quando l'applicazione chiama il metodo [**IDirect3DDevice9::P resent.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) L'applicazione Direct3D può eseguire il rendering dell'oggetto più volte in una scena prima di visualizzare il frame sullo schermo.

A livello di codice, l'applicazione esegue più chiamate a un metodo DrawPrimitive, passando ripetutamente lo stesso oggetto 3D. Prima di ogni chiamata, la posizione dell'oggetto viene leggermente aggiornata, producendo una serie di immagini di oggetti sfocati sulla superficie di rendering di destinazione. Se l'oggetto ha una o più trame, l'applicazione può migliorare l'effetto sfocatura del movimento rendendo quasi trasparente la prima immagine dell'oggetto con tutte le trame. Ogni volta che viene eseguito il rendering dell'oggetto, la trasparenza della trama dell'oggetto diminuisce. Quando l'applicazione esegue il rendering dell'oggetto nella posizione finale, deve eseguire il rendering delle trame dell'oggetto senza trasparenza. L'eccezione è se si aggiunge la sfocatura del movimento a un altro effetto che richiede la trasparenza della trama. In ogni caso, l'immagine iniziale dell'oggetto nel frame deve essere la più trasparente. L'immagine finale deve essere la meno trasparente.

Dopo che l'applicazione esegue il rendering della serie di immagini oggetto sulla superficie di rendering di destinazione ed esegue il rendering del resto della scena, deve chiamare il metodo [**IDirect3DDevice9::P resent**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) per visualizzare il frame sullo schermo.

Se l'applicazione simula l'effetto dell'utente che si sposta in una scena ad alta velocità, può aggiungere sfocatura movimento all'intera scena. In questo caso, l'applicazione esegue il rendering dell'intera scena più volte per fotogramma. Ogni volta che viene eseguito il rendering della scena, l'applicazione deve spostare leggermente il punto di vista. Se la scena è altamente complessa, l'utente potrebbe vedere una riduzione delle prestazioni visibile quando l'accelerazione aumenta a causa del numero crescente di rendering della scena per fotogramma.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Antialias](antialiasing.md)
</dt> </dl>

 

 
