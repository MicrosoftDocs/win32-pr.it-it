---
description: È possibile aggiungere il supporto dei parametri della fase di esecuzione a un XAPO implementando l'interfaccia IXAPOParameters. Il supporto dei parametri in fase di esecuzione consente a un XAPO di modificare il comportamento in base ai parametri passati in fase di esecuzione.
ms.assetid: 13f974ec-fcf5-1749-e69d-88de79b7d82b
title: 'Procedura: Aggiungere supporto per i parametri di runtime a un oggetto di elaborazione audio di XAudio2'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 582f51b3dfbdc6d31422494906d5f945f77ccb03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485180"
---
# <a name="how-to-add-run-time-parameter-support-to-an-xapo"></a>Procedura: Aggiungere supporto per i parametri di runtime a un oggetto di elaborazione audio di XAudio2

È possibile aggiungere il supporto dei parametri della fase di esecuzione a un XAPO implementando l'interfaccia [**IXAPOParameters**](/windows/desktop/api/XAPO/nn-xapo-ixapoparameters) . Il supporto dei parametri in fase di esecuzione consente a un XAPO di modificare il comportamento in base ai parametri passati in fase di esecuzione.

1.  Seguire i passaggi in [procedura: creare un XAPO](how-to--create-an-xapo.md).
2.  Modificare il XAPO in modo che derivi da [**CXAPOParametersBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) e [**CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase).
3.  Aggiungere le chiamate ai metodi [**CXAPOParametersBase:: BeginProcess**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-beginprocess) e [**CXAPOParametersBase:: EndProcess**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-endprocess) all'implementazione di [**IXAPO::P rocess**](/windows/win32/api/xapo/nf-xapo-ixapo-process).

    > [!Note]  
    > L'aggiunta di questi metodi a [IXAPO::P rocess](how-to--build-a-basic-audio-processing-graph.md) consente a [**CXAPOParametersBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) di preservare le copie dei parametri degli effetti in uno stato thread-safe. Chiamare [**CXAPOParametersBase:: BeginProcess**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-beginprocess) all'inizio di [**IXAPO::P rocess**](/windows/win32/api/xapo/nf-xapo-ixapo-process)e [**CXAPOParametersBase:: EndProcess**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-endprocess) alla fine di **IXAPO::P rocess**.

     

4.  Aggiungere altro codice all'implementazione [**IXAPO::P rocess**](/windows/win32/api/xapo/nf-xapo-ixapo-process) per modificarne il comportamento in base ai valori archiviati dal metodo [**separameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-setparameters) .

    > [!Note]  
    > L'aggiunta di codice al metodo [**IXAPO::P rocess**](/windows/win32/api/xapo/nf-xapo-ixapo-process) per usare i parametri specificati da [**separameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-setparameters) consente di modificare il comportamento di XAPO per tutta la sua vita.

     

5.  Quando si crea un'istanza dell'effetto, allocare un buffer di tre strutture che rappresenteranno i parametri dell'effetto e passarlo al costruttore [**CXAPOParametersBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) .

    > [!Note]  
    > L'istanza di [**CXAPOParametersBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) usa internamente questo buffer per gestire i parametri degli effetti passati quando [**si chiamano i parametri.**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-setparameters) È necessario inizializzare tutti i blocchi di parametri di processo in *pParameterBlocks* con lo stesso valore predefinito prima di chiamare uno dei metodi [**IXAPO::P rocess**](/windows/win32/api/xapo/nf-xapo-ixapo-process), [**IXAPOParameters:: GetParameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-getparameters)e **IXAPOParameters::** SetValue. Questa inizializzazione viene in genere gestita in [**IXAPO:: Initialize**](/windows/win32/api/xapo/nf-xapo-ixapo-initialize) o in [**IXAPO:: LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess).

     

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Effetti audio](audio-effects.md)
</dt> <dt>

[Panoramica di XAPO](xapo-overview.md)
</dt> </dl>

 

 
