---
title: Copia di descrittori
description: I metodi ID3D12Device CopyDescriptors e ID3D12Device CopyDescriptorsSimple sull'interfaccia del dispositivo utilizzano la CPU per copiare immediatamente i descrittori.
ms.assetid: 65AE4D96-6221-46B5-BF55-F86479FCF97C
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14fdec6c76f29800f2a0e42bde76b32ebc794275
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104739"
---
# <a name="copying-descriptors"></a>Copia di descrittori

I metodi [**ID3D12Device:: CopyDescriptors**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptors) e [**ID3D12Device:: CopyDescriptorsSimple**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptorssimple) sull'interfaccia del dispositivo utilizzano la CPU per copiare immediatamente i descrittori. Possono essere denominati thread gratuiti purché più thread sulla CPU o sulla GPU non eseguano Scritture potenzialmente in conflitto.

## <a name="copying-descriptors-immediately-cpu-timeline"></a>Copia immediata dei descrittori (sequenza temporale CPU)

Il numero di descrittori di origine (da copiare), specificato come set di intervalli di descrittori, deve essere uguale al numero di descrittori di destinazione (da copiare in), specificato come set separato di intervalli di descrittori. Gli intervalli di origine e di destinazione non devono altrimenti essere allineati. Un set di descrittori di tipo sparse, ad esempio, può essere copiato in una destinazione contigua, viceversa o in una combinazione.

Nell'operazione di copia possono essere necessari più heap dei descrittori, sia come origine che come destinazione. L'uso di handle di descrittore come parametri significa che i metodi di copia non sono interessati agli heap in cui si trova un determinato descrittore. si tratta solo di memoria.

I tipi di heap del descrittore che vengono copiati da e a devono corrispondere, quindi i metodi accettano un solo tipo di heap del descrittore come input. Il driver deve conoscere il tipo di heap di tutti i descrittori nell'operazione di copia specificata, quindi sa quali dimensioni dei dati sono incluse nell'operazione di copia. Il driver potrebbe anche dover eseguire operazioni di copia personalizzate se un determinato tipo di heap del descrittore lo garantisce, ovvero un dettaglio di implementazione. Si noti che gli handle di descrittore non identificano in altro modo il tipo a cui puntano; Pertanto, per l'operazione di copia è necessario un parametro aggiuntivo.

Viene fornita un'API alternativa a [**CopyDescriptors**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptors) per il semplice caso di copiare un singolo intervallo di descrittori da una posizione a un'altra, [**CopyDescriptorsSimple**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptorssimple).

Per questi metodi di copia del descrittore (sequenza temporale CPU) basati su dispositivo, i descrittori di origine devono provenire da un heap dei descrittori non shader visibile. I descrittori di destinazione possono trovarsi in qualsiasi heap del descrittore che sia visibile alla CPU (visibile o meno dello shader).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Descrittori](descriptors.md)
</dt> </dl>

 

 




