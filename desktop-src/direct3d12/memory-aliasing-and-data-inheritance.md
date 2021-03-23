---
title: Alias di memoria ed ereditarietà dei dati
description: La risorsa posizionata e riservata potrebbe avere l'alias della memoria fisica in un heap. Le risorse posizionate abilitano più scenari di ereditarietà dei dati rispetto alle risorse riservate quando l'heap dispone del flag condiviso impostato o quando le risorse con alias hanno layout di memoria completamente definiti.
ms.assetid: 53C5804B-0F81-41AF-83D2-A96DCDFDC94A
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cace5b5997e2a460406ae72abb247224886f3926
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "74105090"
---
# <a name="memory-aliasing-and-data-inheritance"></a>Alias di memoria ed ereditarietà dei dati

La risorsa posizionata e riservata potrebbe avere l'alias della memoria fisica in un heap. Le risorse posizionate abilitano più scenari di ereditarietà dei dati rispetto alle risorse riservate quando l'heap dispone del flag condiviso impostato o quando le risorse con alias hanno layout di memoria completamente definiti.

-   [Aliasing](#memory-aliasing-and-data-inheritance)
-   [Ereditarietà dei dati](#data-inheritance)
-   [Argomenti correlati](#related-topics)

## <a name="aliasing"></a>Aliasing

È necessario emettere una barriera di alias tra l'utilizzo di due risorse che condividono la stessa memoria fisica, anche se non si desidera l'ereditarietà dei dati. I modelli di utilizzo semplice devono indicare, almeno, la risorsa di destinazione in cui è presente un'operazione di questo tipo. Per altri dettagli e modelli di utilizzo avanzati, vedere [**CreatePlacedResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createplacedresource) .

Dopo l'accesso a una risorsa, tutte le risorse che condividono la memoria fisica con tale risorsa diventano Invalidate, a meno che non sia consentita l'ereditarietà dei dati. Le letture delle risorse Invalidate generano contenuto di risorse non definito. Anche le Scritture nelle risorse Invalidate generano contenuto di risorse non definito, a meno che non si verifichino due condizioni:

-   La risorsa non contiene il \_ flag di risorsa D3D12 \_ Consenti la destinazione di \_ \_ rendering o il flag di \_ \_ risorsa D3D12 \_ \_ Consenti stencil di \_ profondità \_ .
-   La scrittura è un'operazione di copia o cancellazione in un'intera sottorisorsa o un riquadro. L'inizializzazione dei riquadri è disponibile solo per le risorse con il riquadro 64KB \_ \_ undefined \_ SWIZZLE e 64KB \_ tile \_ standard \_ SWIZZLE.

Le invalide sovrapposte hanno un ambito limitato a granularità più piccole, quando i layout forniscono informazioni sulla posizione in cui si trovano i dati Texel e quando le risorse sono in determinati stati di barriera di transizione. Tuttavia, le invalide non possono superare le granularità di allineamento delle risorse.

Una granularità dell'allineamento del buffer è 64KB e la granularità dell'allineamento maggiore ha la precedenza. Questo è importante quando si considerano le trame 4KB, in quanto più trame 4KB possono trovarsi in un'area 64KB senza sovrapporsi. Tuttavia, non è possibile usare in combinazione con una qualsiasi di queste trame 4KB un alias del buffer con la stessa area 64KB. L'applicazione non è in grado di impedire in modo affidabile l'accesso al buffer dall'intersezione delle trame 4KB, in quanto le GPU sono autorizzate a swizzle i dati della trama 4KB all'interno dell'area 64KB in un modello non definito.

\_il riquadro 64KB \_ undefined \_ SWIZZLE, 64KB \_ tile \_ standard \_ SWIZZLE e \_ i layout di trama principali della riga indicano all'applicazione che le granularità di allineamento sovrapposte sono diventate non valide. Ad esempio: un'applicazione può creare una matrice di trama di destinazione di rendering 2D con due sezioni di matrice, un singolo livello MIP e \_ il \_ layout di SWIZZLE indefinito del riquadro 64KB \_ . Si supponga che l'applicazione riconosca che ogni sezione della matrice occupa 100 riquadri 64KB. L'applicazione può non riuscire a usare la sezione della matrice 0 e riusare tale memoria per un buffer di ~ 6 MB, una trama di ~ 6 MB con layout non definito e così via. In futuro, si supponga che l'applicazione non abbia più richiesto il primo riquadro della sezione della matrice 1. Quindi, l'applicazione potrebbe anche individuare un buffer 64KB fino a quando il rendering richiederebbe nuovamente il primo riquadro della sezione della matrice 1. Per riutilizzare il primo riquadro con la matrice di trama, l'applicazione deve eseguire una copia o una copia completa del riquadro.

Tuttavia, anche le trame con layout definiti presentano ancora casi problematici. Le dimensioni delle risorse di trama possono essere notevolmente diverse da quelle che possono essere calcolate dall'applicazione, perché alcune architetture degli adattatori allocano memoria aggiuntiva per le trame per ridurre la larghezza di banda effettiva durante scenari di rendering comuni. Eventuali invalide nell'area di memoria aggiuntiva determinano l'invalidazione dell'intera risorsa. Per ulteriori informazioni, vedere [**GetResourceAllocationInfo**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getresourceallocationinfo) .

## <a name="data-inheritance"></a>Ereditarietà dei dati

Le risorse posizionate abilitano la maggior parte dell'ereditarietà dei dati per le trame, anche con layout di memoria non definiti. Le applicazioni possono simulare le funzionalità di ereditarietà dei dati che consentono di abilitare le risorse condivise individuando due trame con proprietà di risorse identiche allo stesso offset in un heap condiviso. L'intera descrizione della risorsa deve essere identica, inclusi il valore Clear ottimizzato e il tipo di metodo di creazione delle risorse (inserito o riservato). Tuttavia, entrambe le risorse potrebbero avere stati diversi della barriera di transizione iniziale.

Le risorse riservate consentono l'ereditarietà dei dati per riquadro. Tuttavia, esistono restrizioni per gli Stati della barriera di transizione delle risorse.

Per ereditare i dati, entrambe le risorse devono trovarsi in uno stato di barriera di transizione delle risorse compatibile:

-   Per i buffer, le trame con accesso simultaneo e le trame tra adattatori, lo stato di transizione delle risorse non è importante e tutti gli Stati sono "compatibili".
-   Per le trame riservate senza le proprietà precedenti o altre ereditarietà dei dati per riquadro tramite il \_ riquadro 64KB \_ undefined \_ SWIZZLE o 64KB \_ tile \_ standard \_ SWIZZLE, lo stato della barriera di transizione delle risorse, incluso il riquadro, deve essere nello stato comune.
-   Per tutte le altre trame, in cui le descrizioni delle risorse corrispondono esattamente, lo stato della barriera di transizione delle risorse per ogni coppia corrispondente di sottorisorse deve:
    -   Si trova nello stato comune.
    -   Essere uguali quando lo stato ha lo stesso flag di scrittura GPU.

Quando la GPU supporta swizzle standard, i buffer e le trame swizzle standard possono essere con alias sulla stessa memoria e ereditano i dati tra di essi. L'applicazione può modificare i Texel dalla rappresentazione del buffer, perché il modello swizzle standard descrive in che modo i Texel sono disposti in memoria. Il modello swizzle visibile alla CPU è equivalente al modello swizzle visibile in GPU visualizzato nei buffer.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sottoallocazione negli heap](suballocation-within-heaps.md)
</dt> </dl>

 

 




