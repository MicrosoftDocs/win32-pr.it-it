---
title: Descrittori
description: I descrittori sono l'unità principale di binding per una singola risorsa in D3D12.
ms.assetid: f35b5776-46b0-4659-9e61-c6ebfdb55f87
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ccc2b501a79eddf942e92a3296f2b23af58b08a69ebbb0cded2570752f96263b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118530399"
---
# <a name="descriptors"></a>Descrittori

I descrittori sono l'unità principale di binding per una singola risorsa in D3D12.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                       | Descrizione                                                                                                                                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Cenni preliminari sui descrittori](descriptors-overview.md)<br/> | I descrittori vengono creati dalle chiamate API e identificano le risorse.<br/>                                                                                                                                                                                                                                                                                                                   |
| [Creazione di descrittori](creating-descriptors.md)<br/> | Vengono descritti e illustrati esempi per la creazione di viste di indice, vertice e buffer costanti. risorsa shader, destinazione di rendering, accesso non ordinato, output del flusso e visualizzazioni degli stencil di profondità; e campionatori. Tutti i metodi per la creazione di descrittori sono a thread libero.<br/>                                                                                                                             |
| [Copia di descrittori](copying-descriptors.md)<br/>   | I [**metodi ID3D12Device::CopyDescriptors**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptors) e [**ID3D12Device::CopyDescriptorsSimple**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptorssimple) nell'interfaccia del dispositivo usano la CPU per copiare immediatamente i descrittori. Possono essere chiamate a thread libero purché più thread nella CPU o nella GPU non esegueranno operazioni di scrittura potenzialmente in conflitto.<br/> |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Heap dei descrittori](descriptor-heaps.md)
</dt> <dt>

[Tabelle dei descrittori](descriptor-tables.md)
</dt> <dt>

[Associazione di risorse](resource-binding.md)
</dt> <dt>

[Firme radice](root-signatures.md)
</dt> </dl>

 

 





