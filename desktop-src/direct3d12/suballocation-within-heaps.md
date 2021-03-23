---
title: Sottoallocazione negli heap
description: Gli heap delle risorse trasferiscono i dati dalla CPU alla GPU (caricamento) e dalla GPU alla CPU (lettura indietro).
ms.assetid: 7E319BCF-FF3F-43CB-9C48-A9DD2A043592
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 701e68e31e698bbf2c955a252bd46876f45d6b7c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104158"
---
# <a name="suballocation-within-heaps"></a>Sottoallocazione negli heap

Gli heap delle risorse trasferiscono i dati dalla CPU alla GPU (caricamento) e dalla GPU alla CPU (lettura indietro).

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                       | Descrizione                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Alias di memoria ed ereditarietà dei dati](memory-aliasing-and-data-inheritance.md)<br/> | La risorsa posizionata e riservata potrebbe avere l'alias della memoria fisica in un heap. Le risorse posizionate abilitano più scenari di ereditarietà dei dati rispetto alle risorse riservate quando l'heap dispone del flag condiviso impostato o quando le risorse con alias hanno layout di memoria completamente definiti. <br/> |
| [Heap condivisi](shared-heaps.md)<br/>                                                 | La condivisione è utile per le architetture a più processi e a più adapter.<br/>                                                                                                                                                                                          |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**ID3D12Device:: Createheap ha provocato**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createheap)
</dt> <dt>

[**ID3D12Heap**](/windows/desktop/api/d3d12/nn-d3d12-id3d12heap)
</dt> <dt>

[Gestione della memoria](memory-management.md)
</dt> </dl>

 

 





