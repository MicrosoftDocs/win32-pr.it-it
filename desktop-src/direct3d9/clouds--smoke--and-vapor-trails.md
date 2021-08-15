---
description: Cloud, smoke e trail possono essere tutti creati da un'estensione della tecnica di tabellone.
ms.assetid: c5607327-de46-4241-a01a-4adfe0bbf6fb
title: Cloud, Smoke e Trails (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09da27ec1ba8f6ad8beb3c9a847226ffe63f1059c0b28dfe71e0d0582d56645f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118097163"
---
# <a name="clouds-smoke-and-vapor-trails-direct3d-9"></a>Cloud, Smoke e Trails (Direct3D 9)

Cloud, smoke e trail possono essere tutti creati da un'estensione della tecnica di tabellone. Vedere [La creazione di un'applicazione (Direct3D 9).](billboarding.md) Ruotando il gruppo su due assi invece che su uno, l'applicazione può consentire all'utente di visualizzare un pello da qualsiasi angolo. In genere, un'applicazione ruota il grafico sugli assi orizzontale e verticale.

Per creare un cloud semplice, l'applicazione può ruotare una primitiva rettangolare su uno o due assi in modo che la primitiva si faccia fronte all'utente. Una trama simile al cloud può quindi essere applicata alla primitiva con trasparenza. Per informazioni dettagliate sull'applicazione di trame trasparenti alle primitive, vedere [Texture Blending (Direct3D 9) (Fusione delle trame (Direct3D 9).](texture-blending.md) È possibile animare il cloud applicando una serie di trame nel tempo.

Un'applicazione può creare cloud più complessi formandoli da un gruppo di primitive. Ogni parte del cloud è una primitiva rettangolare. Le primitive possono essere spostate in modo indipendente nel tempo per dare l'aspetto di una sincronizzazione dinamica. Nella figura seguente viene illustrato questo concetto.

![illustrazione di primitive che formano cloud più complessi](images/cloud.png)

L'aspetto dello smoke viene visualizzato in modo simile alle nubi. In genere richiede più ambienti, ad esempio cloud complessi. Lo smoke in genere si alza e si alza nel tempo, quindi i taser che costituiscono lo smoke devono spostarsi di conseguenza. Potrebbe essere necessario aggiungere altri elementi man appena il tempo aumenta e si disperde.

Una traccia di colore è una fumata che non si alza. Tuttavia, come una fumata, si disperde nel tempo. Nella figura seguente viene illustrata la tecnica dell'uso dei masche per simulare una traccia di un itinerario.

![illustrazione di pannelli che simulano un percorso di simulare un itinerario](images/vapor.png)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esempi alfa](alpha-examples.md)
</dt> </dl>

 

 



