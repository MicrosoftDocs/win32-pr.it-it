---
title: Ricampionamento audio
description: Ricampionamento audio
ms.assetid: ec6ad6b2-1d35-4ac4-9a1e-3fc9c053000c
keywords:
- Windows Media Format SDK, ricampionamento audio
- Windows Media Format SDK, ripetizione del campionamento audio
- ASF (Advanced Systems Format), ricampionamento audio
- ASF (formato avanzato dei sistemi), ricampionamento audio
- ASF (Advanced Systems Format), ripetizione del campionamento audio
- ASF (Advanced Systems Format), ricampionamento audio
- ricampionamento audio
- ripetizione del campionamento audio, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 608272a7e531d7380991a705d391e6226a6758d1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329892"
---
# <a name="audio-resampling"></a>Ricampionamento audio

Ogni formato compresso di un codec audio presenta una frequenza di campionamento e una dimensione di esempio specifici. Non è necessario che corrispondano alle impostazioni del formato di input o di output. Se un formato di input presenta impostazioni diverse da quelle del formato compresso descritto nel profilo, il writer Ricampiona l'audio, durante il processo di codifica, in modo che corrisponda al formato compresso. Solo determinati formati sono accettati dal writer come input. Quando si enumerano i formati di input per un flusso audio compresso, è possibile ricampionare tutti i formati recuperati in modo che corrispondano al formato nel profilo.

Quando si legge un audio compresso, il lettore Ricampiona il contenuto in modo che corrisponda al formato di output. È necessario utilizzare uno dei formati di output enumerati dal lettore, in modo da garantire che l'audio possa essere ricampionato nelle impostazioni del formato di output.

Ogni ripetizione del campionamento potrebbe influire sulla qualità dell'audio. Quando possibile, è consigliabile usare i formati di input e output con le impostazioni che corrispondono al formato compresso.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Funzionalità di scrittura di file**](file-writing-features.md)
</dt> <dt>

[**Utilizzo degli input**](working-with-inputs.md)
</dt> <dt>

[**Uso degli output**](working-with-outputs.md)
</dt> </dl>

 

 




