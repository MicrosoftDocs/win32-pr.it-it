---
description: È possibile migliorare la velocità percepita di un oggetto in una scena 3D sfocando l'oggetto e lasciando un tracciato sfocato di immagini oggetto dietro l'oggetto. Per eseguire questa operazione, le applicazioni Direct3D eseguono il rendering dell'oggetto più volte per frame.
ms.assetid: 8b1a1f0d-5857-4ab4-828c-8ca7c17a4890
title: Sfocatura movimento (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fccb5c00d1208041afc31d4afe1cf0c7a5425037
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521921"
---
# <a name="motion-blur-direct3d-9"></a>Sfocatura movimento (Direct3D 9)

È possibile migliorare la velocità percepita di un oggetto in una scena 3D sfocando l'oggetto e lasciando un tracciato sfocato di immagini oggetto dietro l'oggetto. Per eseguire questa operazione, le applicazioni Direct3D eseguono il rendering dell'oggetto più volte per frame.

Tenere presente che le applicazioni Direct3D eseguono in genere il rendering di scene in un buffer fuori schermo. Il contenuto del buffer viene visualizzato sullo schermo quando l'applicazione chiama il metodo [**IDirect3DDevice9::P reinviato**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) . L'applicazione Direct3D può eseguire il rendering dell'oggetto più volte in una scena prima di visualizzare il frame sullo schermo.

A livello di codice, l'applicazione effettua più chiamate a un metodo DrawPrimitive, passando ripetutamente lo stesso oggetto 3D. Prima di ogni chiamata, la posizione dell'oggetto viene aggiornata leggermente, producendo una serie di immagini oggetto sfocate sulla superficie di rendering di destinazione. Se l'oggetto ha una o più trame, l'applicazione può migliorare l'effetto di sfocatura del movimento eseguendo il rendering della prima immagine dell'oggetto con tutte le relative trame quasi trasparenti. Ogni volta che viene eseguito il rendering dell'oggetto, la trasparenza della trama dell'oggetto diminuisce. Quando l'applicazione esegue il rendering dell'oggetto nella posizione finale, deve eseguire il rendering delle trame dell'oggetto senza trasparenza. L'eccezione si verifica se si aggiunge Motion Blur a un altro effetto che richiede la trasparenza della trama. In ogni caso, l'immagine iniziale dell'oggetto nel frame dovrebbe essere la più trasparente. L'immagine finale dovrebbe essere la meno trasparente.

Quando l'applicazione esegue il rendering della serie di immagini oggetto sulla superficie di rendering di destinazione ed esegue il rendering del resto della scena, deve chiamare il metodo [**IDirect3DDevice9::P**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) reinviato per visualizzare il frame sullo schermo.

Se l'applicazione sta simulando l'effetto dell'utente che si sposta in una scena ad alta velocità, può aggiungere la sfocatura di movimento all'intera scena. In questo caso, l'applicazione esegue il rendering dell'intera scena più volte per fotogramma. Ogni volta che viene eseguito il rendering della scena, l'applicazione deve spostare leggermente il punto di visualizzazione. Se la scena è molto complessa, è possibile che l'utente visualizzi un calo delle prestazioni visibile perché l'accelerazione è aumentata a causa del numero crescente di rendering della scena per fotogramma.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Anti-aliasing](antialiasing.md)
</dt> </dl>

 

 
