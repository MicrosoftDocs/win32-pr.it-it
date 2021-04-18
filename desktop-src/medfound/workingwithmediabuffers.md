---
description: Uso dei buffer multimediali DMO
ms.assetid: 6d0c51b8-0d79-4f04-8e90-0cea4f3b1427
title: Uso dei buffer multimediali DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c870b3a4a035c71a4dcadf9a38b4c2a150097e7
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320544"
---
# <a name="working-with-dmo-media-buffers"></a>Uso dei buffer multimediali DMO

I dati di input vengono passati al codec DMOs usando i buffer multimediali. Un buffer multimediale è un oggetto che implementa l'interfaccia [**IMediaBuffer**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediabuffer) . È possibile implementare una classe a questo scopo oppure, se si usa Windows Media Format SDK nell'applicazione, è possibile usare gli oggetti buffer definiti in tale SDK.

Se si implementa una classe di buffer personalizzata, prestare attenzione a come viene gestita la memoria del buffer. Quando si passa un esempio di input, DMO mantiene un riferimento al buffer fino a quando non viene terminato con l'esempio. È possibile rilasciare immediatamente il riferimento all'interfaccia [**IMediaBuffer**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediabuffer) , ma non si ha modo di sapere quando il codec non necessita più del riferimento. Per essere certi che la memoria venga liberata quando l'oggetto viene eliminato, è necessario implementare la classe in modo da allocare e liberare la memoria per il buffer internamente.

Poiché il DMOs mantiene i riferimenti ai buffer per un periodo di tempo sconosciuto, non è una cosa banale usare un pool limitato di buffer. La soluzione più semplice consiste nell'allocare un nuovo buffer per ogni esempio, anche se questa operazione non è efficiente.

Una soluzione migliore consiste nell'implementare un oggetto per gestire un pool di buffer. A tale scopo, scrivere il codice nel metodo di **rilascio** dell'implementazione di [**IMediaBuffer**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediabuffer) che chiama un metodo di gestione buffer (anziché eliminarlo) quando il conteggio dei riferimenti scende a zero. Gestione buffer può quindi gestire un elenco di puntatori agli oggetti buffer allocati. Creare un metodo in Gestione buffer per controllare l'elenco dei buffer liberi e restituire un puntatore in modo che l'applicazione possa accedere ai buffer quando necessario. Questo metodo deve creare nuovi buffer in base alle esigenze e aggiungerli all'elenco.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di codec DMOs](workingwithcodecdmos.md)
</dt> </dl>

 

 
