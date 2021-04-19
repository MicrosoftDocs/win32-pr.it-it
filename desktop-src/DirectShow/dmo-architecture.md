---
description: Architettura DMO
ms.assetid: f74b2d0f-b40c-4598-97a4-9c1dc71bbb1a
title: Architettura DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93fcf7f4ef4528cd4d7949d804b149588075d5ef
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303746"
---
# <a name="dmo-architecture"></a>Architettura DMO

In questa sezione viene descritta l'architettura complessiva di un DMO.

**Flussi**

Un DMO è un oggetto che accetta input *m* e produce *n* output. Gli input e gli output sono detti *flussi*. Ogni DMO ha almeno un flusso. I flussi non sono oggetti; si fa semplicemente riferimento a DMO in base al numero di indice. Il numero di flussi viene corretto in fase di progettazione.

**Tipi di supporto**

Tutti i dati vengono digitati utilizzando un *tipo di supporto*, che definisce come interpretare il contenuto dei dati. Ad esempio, il video RGB a 320 x 240 24 bit è un tipo; 44,1-kilohertz (kHz) audio PCM stereo a 16 bit è un altro tipo. I tipi di supporto vengono descritti utilizzando la struttura del [**\_ \_ tipo di supporto DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) . Prima che il client possa elaborare i dati, deve impostare il tipo di supporto per ogni flusso nel DMO.

In genere, un flusso può accettare un intervallo di tipi di supporti. Alcuni DMOs supportano una più ampia gamma di tipi rispetto ad altri. Le interfacce DMO definiscono i metodi che consentono al client di individuare i tipi supportati. Ad esempio, un DMO potrebbe supportare video RGB con una profondità qualsiasi, mentre un altro potrebbe supportare solo RGB a 24 bit. Inoltre, un DMO potrebbe essere limitato a determinate combinazioni di input e output. Se, ad esempio, il tipo di input è video a 16 bit, il flusso di output potrebbe richiedere la stessa profondità del bit. Il client può enumerare i tipi preferiti di ogni flusso e quindi testare combinazioni specifiche.

**Buffer**

Nel modello DMO predefinito, il client alloca buffer di input e buffer di output distinti. Riempie i buffer di input con i dati e li recapita a DMO e DMO scrive nuovi dati nei buffer di output.

Facoltativamente, un DMO può supportare l'elaborazione "sul posto". Con l'elaborazione sul posto, DMO scrive l'output direttamente nel buffer di input, sui dati originali. L'elaborazione sul posto elimina la necessità di buffer distinti. D'altra parte, modifica i dati originali, che potrebbero non essere accettabili per alcune applicazioni.

Il modello di buffering predefinito (non sul posto) è supportato tramite l'interfaccia [**IMediaObject**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject) . Tutti DMOs devono implementare questa interfaccia. Se un DMO supporta l'elaborazione sul posto, espone anche l'interfaccia [**IMediaObjectInPlace**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobjectinplace) . Il client è responsabile dell'allocazione di tutti i buffer, sia di input che di output.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni su DMOs](about-dmos.md)
</dt> </dl>

 

 



