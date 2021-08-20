---
description: Le tracce di nuvole, fumi e vapori possono essere create da un'estensione della tecnica di creazione di pannelli pubblicitari.
ms.assetid: c5607327-de46-4241-a01a-4adfe0bbf6fb
title: Clouds, Smoke e Vapor Trails (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09da27ec1ba8f6ad8beb3c9a847226ffe63f1059c0b28dfe71e0d0582d56645f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118097163"
---
# <a name="clouds-smoke-and-vapor-trails-direct3d-9"></a>Clouds, Smoke e Vapor Trails (Direct3D 9)

Le tracce di nuvole, fumi e vapori possono essere create da un'estensione della tecnica di creazione di pannelli pubblicitari. Vedere [La creazione di manifesti (Direct3D 9)](billboarding.md). Ruotando il manifesto su due assi anziché su uno, l'applicazione può consentire all'utente di visualizzare un manifesto da qualsiasi angolazione. In genere, un'applicazione ruota il manifesto sugli assi orizzontale e verticale.

Per creare un cloud semplice, l'applicazione può ruotare una primitiva rettangolare su uno o due assi in modo che la primitiva si faccia fronte all'utente. Una trama simile al cloud può quindi essere applicata alla primitiva con trasparenza. Per informazioni dettagliate sull'applicazione di trame trasparenti alle primitive, vedere Fusione tra trame [(Direct3D 9).](texture-blending.md) È possibile animare il cloud applicando una serie di trame nel tempo.

Un'applicazione può creare cloud più complessi formandoli da un gruppo di primitive. Ogni parte del cloud è una primitiva rettangolare. Le primitive possono essere spostate in modo indipendente nel tempo per dare l'aspetto di una nebbia dinamica. Nella figura seguente viene illustrato questo concetto.

![illustrazione di primitive che formano cloud più complessi](images/cloud.png)

L'aspetto del fumo viene visualizzato in modo simile alle nuvole. In genere richiede più manifesti, ad esempio cloud complessi. Il fumo in genere si alza e si alza nel tempo, quindi i manifesti che costituiscono la pennaccia di fumata devono spostarsi di conseguenza. Potrebbe essere necessario aggiungere altri manifesti quando il pennacchino si alza e si disperde.

Una traccia di vapore è una pennaccia di fumata che non si alza. Tuttavia, come un pennarella di fumata, si disperde nel tempo. Nella figura seguente viene illustrata la tecnica dell'uso di manifesti per simulare una traccia di vapore.

![illustrazione di manifesti pubblicitari che simulano una traccia di vapore](images/vapor.png)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esempi di alfa](alpha-examples.md)
</dt> </dl>

 

 



