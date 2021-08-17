---
description: Composizione e livelli
ms.assetid: c1aefd92-b47f-4af1-8299-9ba401ad5fe8
title: Composizione e livelli
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b173ed0727869d3630a2241d7237cf74fb5143a907a95fcc53901a7b85f285c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954230"
---
# <a name="composition-and-layering"></a>Composizione e livelli

\[Questa API non è supportata e potrebbe essere modificata o non disponibile in futuro.\]

In una raccolta di tracce, la prima traccia ha la priorità più bassa (priorità 0) e ogni traccia successiva ha una priorità di un livello superiore. A ogni livello di priorità, le clip di origine nella traccia nascondono le clip di origine nelle tracce sottostanti, a meno che tale livello non contenga anche una transizione. È quindi possibile immaginare des che effettua diversi passaggi durante il rendering.

In primo luogo, viene eseguito il rendering della traccia 0. Non c'è nulla "sotto" Traccia 0, quindi le aree vuote vengono visualizzate come un'immagine nera a tinta unita. Le transizioni in questo livello si verificano tra l'immagine nera e la traccia 0 o viceversa. DES lays track 1 on top of track 0, generating any transitions between the two tracks. Il risultato è il composto delle due tracce. Inserisce quindi la traccia 2 in questo composito. Le transizioni a questo livello si verificano tra la composita e la traccia 2. Il processo continua fino a quando non viene impostata l'ultima traccia (con priorità più alta).

Quando più tracce vengono composte insieme, si comportano come una singola traccia (detta traccia virtuale). L'oggetto di composizione incapsula questo comportamento, rendendo possibili transizioni complesse. Ad esempio, un clip video può essere cancellato in un secondo clip, mentre il clip composito (entrambe le clip più la cancellazione) si dissolve in una terza clip.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Attività iniziali con DirectShow Editing Services](getting-started-with-directshow-editing-services.md)
</dt> </dl>

 

 



