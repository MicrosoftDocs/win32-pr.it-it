---
title: Descrittori
description: I descrittori sono l'unità primaria di binding per una singola risorsa in D3D12.
ms.assetid: f35b5776-46b0-4659-9e61-c6ebfdb55f87
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9576a2d40ade89c9c7a342feb6b069ca1321028e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104247"
---
# <a name="descriptors"></a>Descrittori

I descrittori sono l'unità primaria di binding per una singola risorsa in D3D12.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                       | Descrizione                                                                                                                                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Cenni preliminari sui descrittori](descriptors-overview.md)<br/> | I descrittori vengono creati dalle chiamate API e identificano le risorse.<br/>                                                                                                                                                                                                                                                                                                                   |
| [Creazione di descrittori](creating-descriptors.md)<br/> | Vengono descritti e illustrati esempi per la creazione di viste di buffer di indice, vertex e costanti; risorsa shader, destinazione di rendering, accesso non ordinato, output del flusso e visualizzazioni di stencil Depth; e Samplers. Tutti i metodi per la creazione di descrittori sono a thread libero.<br/>                                                                                                                             |
| [Copia di descrittori](copying-descriptors.md)<br/>   | I metodi [**ID3D12Device:: CopyDescriptors**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptors) e [**ID3D12Device:: CopyDescriptorsSimple**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptorssimple) sull'interfaccia del dispositivo utilizzano la CPU per copiare immediatamente i descrittori. Possono essere denominati thread gratuiti purché più thread sulla CPU o sulla GPU non eseguano Scritture potenzialmente in conflitto.<br/> |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Heap descrittore](descriptor-heaps.md)
</dt> <dt>

[Tabelle descrittore](descriptor-tables.md)
</dt> <dt>

[Associazione di risorse](resource-binding.md)
</dt> <dt>

[Firme radice](root-signatures.md)
</dt> </dl>

 

 





