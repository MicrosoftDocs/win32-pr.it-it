---
description: Uso di DMO buffer multimediali
ms.assetid: 6d0c51b8-0d79-4f04-8e90-0cea4f3b1427
title: Uso di DMO buffer multimediali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 311778898fbfa669a602cd189fb5518f7a2814089a87ed33fba7e303c4327cac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118236957"
---
# <a name="working-with-dmo-media-buffers"></a>Uso di DMO buffer multimediali

I dati di input vengono passati ai DMO del codec usando buffer multimediali. Un buffer multimediale è un oggetto che implementa [**l'interfaccia IMediaBuffer.**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediabuffer) È possibile implementare una classe a questo scopo oppure, se si usa Windows Media Format SDK nell'applicazione, è possibile usare gli oggetti buffer definiti in tale SDK.

Se si implementa una classe di buffer personalizzata, prestare attenzione a come viene gestita la memoria del buffer. Quando si passa un esempio di input, il DMO mantiene un riferimento al buffer fino al termine dell'esempio. È possibile rilasciare immediatamente il riferimento [**all'interfaccia IMediaBuffer,**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediabuffer) ma non è possibile sapere quando il codec non necessita più del relativo riferimento. Per essere certi che la memoria viene liberata quando l'oggetto viene eliminato, è necessario implementare la classe in modo che alloca e libera internamente la memoria per il buffer.

Poiché le dmo mantengono i riferimenti ai buffer per un periodo di tempo sconosciuto, non è semplice usare un pool limitato di buffer. La soluzione più semplice consiste nell'allocare un nuovo buffer per ogni campione, anche se questa operazione è inefficiente.

Una soluzione migliore consiste nell'implementare un oggetto per gestire un pool di buffer. A tale scopo, scrivere codice nel metodo **Release** dell'implementazione [**di IMediaBuffer**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediabuffer) che chiama un metodo di Gestione buffer (anziché eliminare se stesso) quando il conteggio dei riferimenti scende a zero. Gestione buffer può quindi gestire un elenco di puntatori agli oggetti buffer allocati. Creare un metodo in Gestione buffer per controllare l'elenco dei buffer liberi e restituire un puntatore in modo che l'applicazione possa accedere ai buffer quando necessario. Questo metodo deve creare nuovi buffer in base alle esigenze e aggiungerli all'elenco.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso degli oggetti DMO codec](workingwithcodecdmos.md)
</dt> </dl>

 

 
