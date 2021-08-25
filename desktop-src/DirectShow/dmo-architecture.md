---
description: DMO Architettura
ms.assetid: f74b2d0f-b40c-4598-97a4-9c1dc71bbb1a
title: DMO Architettura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcb2e125fda635c70e03e02af15d12e0ffb4f3ac4d5083eb91a4b99d3d3590e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119906491"
---
# <a name="dmo-architecture"></a>DMO Architettura

Questa sezione descrive l'architettura complessiva di un DMO.

**Flussi**

Un DMO è un oggetto che accetta input *m* e produce *n* output. Gli input e gli output sono denominati *flussi*. Ogni DMO ha almeno un flusso. Flussi non sono oggetti. viene fatto semplicemente riferimento al DMO in base al numero di indice. Il numero di flussi è fisso in fase di progettazione.

**Tipi di supporti**

Tutti i dati vengono tipiati usando un *tipo di* supporto , che definisce come interpretare il contenuto dei dati. Ad esempio, 320 x 240 video RGB a 24 bit è un tipo; L'audio PCM stereo a 16 bit a 44,1 kilohertz (kHz) è un altro tipo. I tipi di supporti vengono descritti [**usando la DMO MEDIA \_ \_ TYPE.**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) Prima che il client possa elaborare i dati, deve impostare il tipo di supporto per ogni flusso nel DMO.

In genere, un flusso può accettare un intervallo di tipi di supporti. Alcune DMO supportano una gamma più ampia di tipi rispetto ad altri. Le DMO definiscono metodi per il client per individuare i tipi supportati. Ad esempio, un DMO può supportare video RGB a qualsiasi profondità di bit, mentre un altro potrebbe supportare solo RGB a 24 bit. Inoltre, un DMO può essere limitato a determinate combinazioni di input e output. Ad esempio, se il tipo di input è video a 16 bit, il flusso di output potrebbe richiedere la stessa profondità in bit. Il client può enumerare i tipi preferiti di ogni flusso e quindi testare combinazioni specifiche.

**Buffer**

Nel modello di DMO predefinito, il client alloca buffer di input e buffer di output separati. Riempie i buffer di input con dati e li recapita al DMO e il DMO scrive nuovi dati nei buffer di output.

Facoltativamente, un DMO può supportare l'elaborazione "sul posto". Con l'elaborazione sul posto, DMO scrive l'output direttamente nel buffer di input, sui dati originali. L'elaborazione sul posto elimina la necessità di buffer separati. D'altra parte, modifica i dati originali, che potrebbero non essere accettabili per alcune applicazioni.

Il modello di buffering predefinito (non sul posto) è supportato tramite [**l'interfaccia IMediaObject.**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject) Tutte le DMO devono implementare questa interfaccia. Se un DMO supporta l'elaborazione sul posto, espone anche [**l'interfaccia IMediaObjectInPlace.**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobjectinplace) Il client è responsabile dell'allocazione di tutti i buffer, sia di input che di output.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sulle DMO](about-dmos.md)
</dt> </dl>

 

 



