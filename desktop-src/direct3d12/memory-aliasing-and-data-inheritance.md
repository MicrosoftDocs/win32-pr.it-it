---
title: Aliasing della memoria ed ereditarietà dei dati
description: Le risorse posizionate e riservate possono creare alias per la memoria fisica all'interno di un heap. Le risorse posizionate consentono più scenari di ereditarietà dei dati rispetto alle risorse riservate quando per l'heap è impostato il flag condiviso o quando le risorse con alias hanno layout di memoria completamente definiti.
ms.assetid: 53C5804B-0F81-41AF-83D2-A96DCDFDC94A
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b584ef95f4ee89bc98940c8407427203a19f55046134e1d3c15cb672fef8fef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119460921"
---
# <a name="memory-aliasing-and-data-inheritance"></a>Aliasing della memoria ed ereditarietà dei dati

Le risorse posizionate e riservate possono creare alias per la memoria fisica all'interno di un heap. Le risorse posizionate consentono più scenari di ereditarietà dei dati rispetto alle risorse riservate quando per l'heap è impostato il flag condiviso o quando le risorse con alias hanno layout di memoria completamente definiti.

-   [Aliasing](#memory-aliasing-and-data-inheritance)
-   [Ereditarietà dei dati](#data-inheritance)
-   [Argomenti correlati](#related-topics)

## <a name="aliasing"></a>Aliasing

È necessario creare una barriera di aliasing tra l'utilizzo di due risorse che condividono la stessa memoria fisica, anche se non si desidera ereditarietà dei dati. I modelli di utilizzo semplici devono indicare almeno la risorsa di destinazione coinvolta in un'operazione di questo tipo. Vedere [**CreatePlacedResource per**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createplacedresource) altri dettagli e modelli di utilizzo avanzati.

Dopo l'accesso a una risorsa, tutte le risorse che condividono memoria fisica con tale risorsa vengono invalidate, a meno che non sia consentita l'ereditarietà dei dati. Le operazioni di lettura delle risorse invalidate comportano contenuti di risorse non definiti. Le scritture nelle risorse invalidate comportano anche contenuti di risorse non definiti, a meno che non si verifichino due condizioni:

-   La risorsa non ha lo STENCIL D3D12 RESOURCE FLAG ALLOW RENDER TARGET o \_ \_ \_ \_ \_ D3D12 \_ RESOURCE FLAG ALLOW DEPTH \_ \_ \_ \_ STENCIL.
-   La scrittura è un'operazione di copia o cancellazione in un'intera sottorisorsa o riquadro. L'inizializzazione del riquadro è disponibile solo per le risorse con SWIZZLE RIQUADRO NON DEFINITO da 64 KB e SWIZZLE STANDARD per riquadri \_ \_ a \_ 64 \_ \_ \_ KB.

Le convalide sovrapposte hanno come ambito granularità più piccole, quando i layout forniscono informazioni sulla posizione dei dati texel e su quando le risorse si verificano in determinati stati di barriera di transizione. Tuttavia, le convalide non possono essere inferiori alle granularità di allineamento delle risorse.

Una granularità di allineamento del buffer è di 64 KB e la granularità di allineamento maggiore ha la precedenza. Questo è importante quando si considerano le trame da 4 KB, perché più trame da 4 KB possono risiedere in un'area di 64 KB senza sovrapporsi tra loro. Tuttavia, non è possibile usare un alias del buffer con la stessa area di 64 KB in combinazione con nessuna di queste trame da 4 KB. L'applicazione non può mantenere in modo affidabile l'accesso al buffer dall'intersezione delle trame da 4 KB, perché le GPU possono eseguire lo scorrimento rapido dei dati delle trame da 4 KB all'interno dell'area di 64 KB in un modello non definito.

I layout di trama 64 KB TILE \_ \_ \_ UNDEFINED SWIZZLE, 64KB \_ TILE STANDARD \_ \_ SWIZZLE e ROW \_ MAJOR informano l'applicazione che le granularità di allineamento sovrapposte non sono più valide. Ad esempio: un'applicazione può creare una matrice di trame di destinazione di rendering 2D con 2 sezioni di matrice, un singolo livello mip e il \_ \_ layout SWIZZLE NON DEFINITO tile di 64 \_ KB. Si supponga che l'applicazione comprendi che ogni sezione della matrice occupa 100 riquadri da 64 KB. L'applicazione può non usare la sezione di matrice 0 e usare nuovamente tale memoria per un buffer di ~6 MB, una trama di ~6 MB con layout non definito e così via. In seguito, si supponga che l'applicazione non richiede più il primo riquadro della sezione di matrice 1. L'applicazione potrebbe quindi anche individuare un buffer di 64 KB fino a quando il rendering non richiederà di nuovo il primo riquadro della sezione di matrice 1. L'applicazione deve cancellare o copiare un riquadro completo per usare nuovamente il primo riquadro con la matrice di trame.

Tuttavia, anche le trame con layout definiti hanno ancora casi problematici. Le dimensioni delle risorse di trama possono differire significativamente da ciò che l'applicazione può calcolare, perché alcune architetture di adattatori allocano memoria aggiuntiva per le trame per ridurre la larghezza di banda effettiva durante scenari di rendering comuni. Eventuali convalide in tale area di memoria aggiuntiva causano l'invalidazione dell'intera risorsa. Per [**altri dettagli, vedere GetResourceAllocationInfo.**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getresourceallocationinfo)

## <a name="data-inheritance"></a>Ereditarietà dei dati

Le risorse posizionate consentono la maggior parte dell'ereditarietà dei dati per le trame, anche con layout di memoria non definiti. Le applicazioni possono simulare le funzionalità di ereditarietà dei dati abilitate dalle risorse condivise di cui è stato eseguito il commit individuando due trame con proprietà di risorse identiche allo stesso offset in un heap condiviso. L'intera descrizione della risorsa deve essere identica, inclusi il valore non crittografato ottimizzato e il tipo di metodo di creazione delle risorse (posizionato o riservato). Tuttavia, entrambe le risorse potrebbero avere stati di barriera di transizione iniziale diversi.

Le risorse riservate abilitano l'ereditarietà dei dati per riquadro; ma esistono in genere restrizioni per gli stati della barriera di transizione delle risorse.

Per ereditare i dati, entrambe le risorse devono essere in uno stato di barriera di transizione delle risorse compatibile:

-   Per i buffer, le trame ad accesso simultaneo e le trame tra adattatori incrociati, lo stato di transizione delle risorse non è importante e tutti gli stati sono "compatibili".
-   Per le trame riservate senza le proprietà precedenti o altre ereditarietà dei dati per riquadro tramite SWIZZLE TILE UNDEFINED di 64 KB o \_ \_ \_ \_ SWIZZLE TILE STANDARD da 64 \_ KB, lo stato della barriera di transizione della risorsa, incluso il \_ riquadro, deve essere nello stato comune.
-   Per tutte le altre trame, in cui le descrizioni delle risorse corrispondono esattamente, lo stato della barriera di transizione della risorsa per ogni coppia corrispondente di sottorisorse deve:
    -   Essere nello stato comune.
    -   Essere uguale quando lo stato contiene lo stesso flag di scrittura GPU.

Quando la GPU supporta lo swizzle standard, i buffer e le trame dello swizzle standard possono essere alias alla stessa memoria ed ereditare i dati tra di essi. L'applicazione può modificare i texel dalla rappresentazione del buffer, perché il modello di swizzle standard descrive il modo in cui i texel vengono disposti in memoria. Il modello di swizzle visibile alla CPU è equivalente al modello di swizzle visibile alla GPU visualizzato nei buffer.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sottoallocazione all'interno degli heap](suballocation-within-heaps.md)
</dt> </dl>

 

 




