---
description: Per guidare gli aggiornamenti visivi, l'applicazione deve usare IDirectManipulationCompositor.
ms.assetid: 6D8FB359-F52B-43F9-8A62-6BB2AEDE4F2B
title: Motore di composizione
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: aa4d922893472c1fe235bae60e41a00924d13bba
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481597"
---
# <a name="composition-engine"></a>Motore di composizione

Per guidare gli aggiornamenti visivi, l'applicazione deve usare [**IDirectManipulationCompositor**](/windows/win32/api/DirectManipulation/nn-directmanipulation-idirectmanipulationcompositor). Questo oggetto è responsabile dell'aggiornamento degli oggetti visivi in base agli aggiornamenti [diretti della manipolazione](direct-manipulation-portal.md) , alla guida degli aggiornamenti di inerzia e alla fornitura di informazioni sui tempi di composizione per la manipolazione diretta, inoltre, un'applicazione deve usare il [DCompManipulationCompositor](direct-manipulation-guids.md) fornito dalla [manipolazione diretta](direct-manipulation-portal.md), che gestirà tutti gli aggiornamenti visivi per conto dell'applicazione e gli aggiornamenti dell'inerzia.

[DCompManipulationCompositor](direct-manipulation-guids.md) è un'implementazione dell'interfaccia [**IDirectManipulationCompositor**](/windows/win32/api/DirectManipulation/nn-directmanipulation-idirectmanipulationcompositor) che esegue il wrapping di [DirectComposition](../directcomp/directcomposition-portal.md). Anziché fare in modo che l'applicazione applichi l'output, tramite questa [manipolazione diretta](direct-manipulation-portal.md) dell'oggetto Compositor è possibile applicare l'output impostando le trasformazioni direttamente nell'albero DirectComposition. Utilizzando questa configurazione, è possibile elaborare l'input e applicare le trasformazioni di output, indipendentemente dall'attività nel thread UI.

Per fornire informazioni di [manipolazione diretta](direct-manipulation-portal.md) sull'intervallo di tempo del motore di composizione, la classe [DCompManipulationCompositor](direct-manipulation-guids.md) implementa l'interfaccia [**IDirectManipulationFrameInfoProvider**](/windows/win32/api/DirectManipulation/nn-directmanipulation-idirectmanipulationframeinfoprovider) . Quando si crea un viewport, [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) il puntatore [**IDirectManipulationCompositor**](/windows/win32/api/DirectManipulation/nn-directmanipulation-idirectmanipulationcompositor) ottenuto da [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) per un'istanza di **IDirectManipulationFrameInfoProvider**. Il puntatore **IDirectManipulationFrameInfoProvider** viene passato alla funzione [**IDirectManipulationManager:: CreateViewport ()**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationmanager-createviewport) .
