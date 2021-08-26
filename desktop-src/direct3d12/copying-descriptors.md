---
title: Copia di descrittori
description: I metodi ID3D12Device CopyDescriptors e ID3D12Device CopyDescriptorsSimple nell'interfaccia del dispositivo usano la CPU per copiare immediatamente i descrittori.
ms.assetid: 65AE4D96-6221-46B5-BF55-F86479FCF97C
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce02abfb433b36738de0fd62285e44b2f065ac017217a1e61f8c305e8ca76228
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120069701"
---
# <a name="copying-descriptors"></a>Copia di descrittori

I [**metodi ID3D12Device::CopyDescriptors**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptors) e [**ID3D12Device::CopyDescriptorsSimple**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptorssimple) nell'interfaccia del dispositivo usano la CPU per copiare immediatamente i descrittori. Possono essere chiamate a thread libero purché più thread nella CPU o nella GPU non esegueranno operazioni di scrittura potenzialmente in conflitto.

## <a name="copying-descriptors-immediately-cpu-timeline"></a>Copia immediata dei descrittori (sequenza temporale CPU)

Il numero di descrittori di origine (da cui copiare), specificato come set di intervalli di descrittori, deve essere uguale al numero di descrittori di destinazione (in cui copiare), specificato come set separato di intervalli di descrittori. In caso contrario, gli intervalli di origine e di destinazione non devono essere allineati. Ad esempio, un set di descrittori di tipo sparse può essere copiato in una destinazione contigua, viceversa o in una combinazione.

Nell'operazione di copia possono essere coinvolti più heap di descrittori, sia come origine che come destinazione. L'uso di handle di descrittore come parametri significa che i metodi di copia non si preoccupano degli heap in cui si trova un determinato descrittore, ma sono tutti semplicemente memoria.

I tipi di heap dei descrittori copiati da e in devono corrispondere, quindi i metodi accettano un singolo tipo di heap descrittore come input. Il driver deve conoscere il tipo di heap di tutti i descrittori nell'operazione di copia specificata, in modo da sapere quali dimensioni dei dati sono coinvolte nell'operazione di copia. Il driver potrebbe anche dover eseguire operazioni di copia personalizzate se un determinato tipo di heap descrittore lo garantisce, un dettaglio di implementazione. Si noti che gli handle di descrittore stessi non identificano in altro modo il tipo a cui puntano; Pertanto, è necessario un parametro aggiuntivo per l'operazione di copia.

Viene fornita un'API alternativa a [**CopyDescriptors**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptors) per il semplice caso di copia di un singolo intervallo di descrittori da una posizione a un'altra: [**CopyDescriptorsSimple.**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptorssimple)

Per questi metodi di copia dei descrittori basati su dispositivo (sequenza temporale CPU), i descrittori di origine devono derivare da un heap dei descrittori non visibili allo shader. I descrittori di destinazione possono essere in qualsiasi heap dei descrittori visibile alla CPU (visibile o meno allo shader).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Descrittori](descriptors.md)
</dt> </dl>

 

 




