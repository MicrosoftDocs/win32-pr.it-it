---
title: Ricampionamento audio
description: Ricampionamento audio
ms.assetid: ec6ad6b2-1d35-4ac4-9a1e-3fc9c053000c
keywords:
- Windows Media Format SDK, ricampionamento audio
- Windows Media Format SDK, ricampionamento di audio
- Advanced Systems Format (ASF), ricampionamento audio
- ASF (Advanced Systems Format), ricampionamento audio
- Advanced Systems Format (ASF), ricampionamento dell'audio
- ASF (Advanced Systems Format), ricampionamento dell'audio
- ricampionamento audio
- ricampionamento di audio, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a5d95ed50117ac9d0fe7d71a2148314e1b9faf3ba8a26b99bb69083029b991c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118434475"
---
# <a name="audio-resampling"></a>Ricampionamento audio

Ogni formato compresso di un codec audio ha una frequenza di campionamento e dimensioni di campionamento specifiche. Non è necessario che corrispondano alle impostazioni del formato di input o di output. Se un formato di input ha impostazioni diverse rispetto al formato compresso descritto nel profilo, il writer ricampionerà l'audio, durante il processo di codifica, in modo che corrisponda al formato compresso. Solo determinati formati vengono accettati dal writer come input. Quando si enumerano i formati di input per un flusso audio compresso, è possibile ricampionare tutti i formati recuperati in modo che corrispondano al formato nel profilo.

Durante la lettura dell'audio compresso, il lettore ricampionerà il contenuto in modo che corrisponda al formato di output. È necessario usare uno dei formati di output enumerati dal lettore, in modo da garantire che l'audio possa essere ricampionato in base alle impostazioni del formato di output.

Ogni ricampionamento influisce potenzialmente sulla qualità dell'audio. Quando possibile, è consigliabile usare formati di input e output con impostazioni corrispondenti al formato compresso.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Funzionalità di scrittura di file**](file-writing-features.md)
</dt> <dt>

[**Uso degli input**](working-with-inputs.md)
</dt> <dt>

[**Uso degli output**](working-with-outputs.md)
</dt> </dl>

 

 




