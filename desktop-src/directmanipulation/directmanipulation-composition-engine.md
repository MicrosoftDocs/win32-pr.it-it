---
description: Per eseguire gli aggiornamenti visivi, l'applicazione deve usare IDirectManipulationCompositor.
ms.assetid: 6D8FB359-F52B-43F9-8A62-6BB2AEDE4F2B
title: Motore di composizione
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 14bc2ad60405dba7874493096e022b553a8b276cd6f0bb21ea9ae3cf191f5d3b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120117901"
---
# <a name="composition-engine"></a>Motore di composizione

Per eseguire gli aggiornamenti visivi, l'applicazione deve usare [**IDirectManipulationCompositor**](/windows/win32/api/DirectManipulation/nn-directmanipulation-idirectmanipulationcompositor). Questo oggetto è responsabile dell'aggiornamento degli oggetti visivi in base agli aggiornamenti della manipolazione diretta, della gestione in avanti degli aggiornamenti dell'inerzia e della fornitura di informazioni temporali di composizione alla manipolazione diretta. Inoltre, un'applicazione deve usare [il DCompManipulationCompositor](direct-manipulation-guids.md) fornito da [Manipolazione](direct-manipulation-portal.md)diretta, che gestirà tutti gli aggiornamenti visivi per conto dell'applicazione e gestirà gli aggiornamenti dell'inerzia. [](direct-manipulation-portal.md)

[DCompManipulationCompositor è](direct-manipulation-guids.md) un'implementazione [**dell'interfaccia IDirectManipulationCompositor**](/windows/win32/api/DirectManipulation/nn-directmanipulation-idirectmanipulationcompositor) che esegue il wrapping [di DirectComposition.](../directcomp/directcomposition-portal.md) Anziché richiedere all'applicazione di applicare l'output, tramite questo oggetto compositor [Direct Manipulation](direct-manipulation-portal.md) è possibile applicare l'output impostando le trasformazioni direttamente nell'albero DirectComposition. Usando questa configurazione, è possibile elaborare l'input e applicare trasformazioni di output, indipendentemente dall'attività nel thread dell'interfaccia utente.

Per fornire [informazioni sulla manipolazione](direct-manipulation-portal.md) diretta sui tempi del motore di composizione, la classe [DCompManipulationCompositor](direct-manipulation-guids.md) implementa l'interfaccia [**IDirectManipulationFrameInfoProvider.**](/windows/win32/api/DirectManipulation/nn-directmanipulation-idirectmanipulationframeinfoprovider) Quando si crea un viewport, [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) il puntatore [**IDirectManipulationCompositor**](/windows/win32/api/DirectManipulation/nn-directmanipulation-idirectmanipulationcompositor) ottenuto da [**CoCreateInstance per**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) un'istanza di **IDirectManipulationFrameInfoProvider.** Il **puntatore IDirectManipulationFrameInfoProvider** viene passato alla [**funzione IDirectManipulationManager::CreateViewport().**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationmanager-createviewport)
