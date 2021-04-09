---
description: Gerarchia dell'interfaccia e dell'oggetto streaming multimediale
ms.assetid: dbb6dc3b-b55e-4f6c-918f-068308e2dba9
title: Gerarchia dell'interfaccia e dell'oggetto streaming multimediale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52339644730139af22fd21fa2c24b8448a1afaf3
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "103886033"
---
# <a name="multimedia-streaming-object-and-interface-hierarchy"></a>Gerarchia dell'interfaccia e dell'oggetto streaming multimediale

> [!Note]  
> Queste API sono deprecate. Le applicazioni devono usare il filtro [**grabber di esempio**](sample-grabber-filter.md) o implementare un filtro personalizzato per ottenere i dati da un grafico filtro DirectShow.

 

Nel diagramma seguente viene illustrata la gerarchia di oggetti utilizzata nel flusso multimediale.

![gerarchia di oggetti multimediastreaming](images/mmstream02.png)

L'architettura di streaming multimediale definisce tre tipi generali di oggetto:

-   L'oggetto **AMMultimediaStream** espone l'interfaccia [**IAMMultiMediaStream**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammultimediastream) . Internamente, questo oggetto esegue il wrapping del grafico del filtro DirectShow.
-   Gli oggetti del *flusso multimediale* espongono l'interfaccia [**IMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream) e sono specifici dei dati. L'oggetto AMMultimediaStream contiene uno o più flussi multimediali.
-   Gli oggetti di *esempio di flusso* contengono i dati per un flusso specifico.

Sono supportati gli oggetti del flusso multimediale seguenti:

-   Flusso audio. Espone l'interfaccia [**IAudioMediaStream**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiomediastream) .
-   Flusso DirectDraw. Rappresenta un flusso video di cui viene eseguito il rendering in una superficie DirectDraw. Espone l'interfaccia [**IDirectDrawMediaStream**](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawmediastream) .
-   Flusso del tipo di supporto. Rappresenta dati arbitrari. Espone l'interfaccia [**IAMMediaTypeStream**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediatypestream) .

Ogni oggetto flusso multimediale crea il proprio tipo di oggetto di esempio di flusso:

-   I flussi audio creano esempi audio, che espongono l'interfaccia [**IAudioStreamSample**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiostreamsample) .
-   I flussi DirectDraw creano esempi di DirectDraw, che espongono l'interfaccia [**IDirectDrawStreamSample**](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawstreamsample) .
-   Flussi di tipi di supporti creare esempi di tipi di supporto, che espongono l'interfaccia [**IAMMediaTypeSample**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediatypesample) .

Il diagramma seguente mostra la gerarchia di interfaccia per le interfacce elencate in precedenza:

![gerarchia dell'interfaccia multimediastreaming](images/mmstream01.png)

 

 



