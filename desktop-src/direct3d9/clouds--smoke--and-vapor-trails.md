---
description: Gli itinerari cloud, fumo e Vapor possono essere creati da un'estensione della tecnica di Billboard.
ms.assetid: c5607327-de46-4241-a01a-4adfe0bbf6fb
title: Percorsi cloud, fumo e Vapor (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f60bce89e23b2b2aab7affbb6947cab4d11c33ed
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104570440"
---
# <a name="clouds-smoke-and-vapor-trails-direct3d-9"></a>Percorsi cloud, fumo e Vapor (Direct3D 9)

Gli itinerari cloud, fumo e Vapor possono essere creati da un'estensione della tecnica di Billboard. Vedere la pagina relativa al [tabellone (Direct3D 9)](billboarding.md). Ruotando il tabellone in due assi anziché uno, l'applicazione può consentire all'utente di visualizzare un tabellone da qualsiasi angolo. In genere, un'applicazione ruota il tabellone sugli assi orizzontali e verticali.

Per creare un cloud semplice, l'applicazione può ruotare una primitiva rettangolare su uno o due assi in modo che la primitiva faccia fronte all'utente. Una trama simile al cloud può quindi essere applicata alla primitiva con trasparenza. Per informazioni dettagliate sull'applicazione di trame trasparenti alle primitive, vedere [blending delle trame (Direct3D 9)](texture-blending.md). È possibile aggiungere un'animazione al cloud applicando una serie di trame nel tempo.

Un'applicazione può creare cloud più complessi creandoli da un gruppo di primitive. Ogni parte del cloud è una primitiva rettangolare. Le primitive possono essere spostate in modo indipendente nel tempo per dare l'impressione di una nebbia dinamica. Nella figura seguente viene illustrato questo concetto.

![illustrazione di primitive che formano cloud più complessi](images/cloud.png)

L'aspetto del fumo viene visualizzato in modo analogo ai cloud. Richiede in genere più cartelloni, ad esempio cloud complessi. Un fumo in genere fluttua e aumenta nel tempo, quindi i tabelloni che compongono il fumo devono essere spostati di conseguenza. Potrebbe essere necessario aggiungere più tabelloni quando il pennacchio aumenta e si disperde.

Una pista di vapore è un fumo che non aumenta. Tuttavia, come un pennacchio di fumo, si disperde nel tempo. Nella figura seguente viene illustrata la tecnica di utilizzo dei tabelloni per simulare una pista di vapori.

![illustrazione dei tabelloni che simulano una pista di vapore](images/vapor.png)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esempi di Alpha](alpha-examples.md)
</dt> </dl>

 

 



