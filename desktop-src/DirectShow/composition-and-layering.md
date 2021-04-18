---
description: Composizione e sovrapposizione
ms.assetid: c1aefd92-b47f-4af1-8299-9ba401ad5fe8
title: Composizione e sovrapposizione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7dce1e1df87b5ffc5c65e9090c6fb7266b972d3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303823"
---
# <a name="composition-and-layering"></a>Composizione e sovrapposizione

\[Questa API non è supportata e può essere modificata o non disponibile in futuro.\]

In una raccolta di tracce, la prima traccia ha la priorità più bassa (priorità 0) e ogni traccia successiva ha priorità di un livello superiore. A ogni livello di priorità, le clip di origine in tale traccia nascondono le clip di origine nelle tracce sottostanti, a meno che tale livello non contenga anche una transizione. In questo modo è possibile immaginare che la creazione di più passaggi quando viene eseguito il rendering.

Viene innanzitutto eseguito il rendering di Track 0. Non è presente alcun elemento "in" Track 0, quindi viene eseguito il rendering delle aree vuote come immagine nera a tinta unita. Le transizioni in questo livello si verificano tra l'immagine nera e la traccia 0 o viceversa. DES stabilisce la traccia 1 nella parte superiore della traccia 0, generando le transizioni tra le due tracce. Il risultato è costituito da un composto di due tracce. Quindi posiziona il Track 2 su questo composto. Le transizioni a questo livello si verificano tra composito e Track 2. Il processo continua fino a quando non viene disattivata l'ultima traccia (priorità più alta).

Quando più tracce sono composte insieme, si comportano come una singola traccia (denominata traccia virtuale). L'oggetto Composition incapsula questo comportamento, rendendo possibili transizioni complesse. Ad esempio, un clip video può essere cancellato da un secondo clip, mentre il composito (entrambi i clip più la cancellazione) si dissolve in una terza clip.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Introduzione con i servizi di modifica DirectShow](getting-started-with-directshow-editing-services.md)
</dt> </dl>

 

 



