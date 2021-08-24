---
title: Gestione della memoria in Direct3D 12
description: Il passaggio a D3D12 comporta la sincronizzazione e la gestione corrette della residenza della memoria.
ms.assetid: 94D47EBB-8060-49F6-A1FF-8B7B98AD5363
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42547b85836711efc4e9aa5b621d90c672617aacff779567f118d4af5041512c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119123794"
---
# <a name="memory-management-in-direct3d-12"></a>Gestione della memoria in Direct3D 12

Il passaggio a D3D12 comporta la sincronizzazione e la gestione corrette della residenza della memoria. La gestione della residenza della memoria significa che è necessario eseguire una sincronizzazione ancora maggiore. Questa sezione illustra le strategie di gestione della memoria e la sottoallocazione all'interno di heap e buffer.

-   [In questa sezione](#in-this-section)
-   [Argomenti correlati](#related-topics)

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                       | Descrizione                                                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Strategie di gestione della memoria](memory-management-strategies.md)<br/> | Un gestore di memoria per Direct3D 12 potrebbe essere molto complicato rapidamente con tutti i diversi livelli di supporto, per schede UMA o discrete (non UMA) e con una notevole gamma di differenze di architettura tra le schede GPU.<br/> La strategia consigliata per la gestione della memoria Direct3D 12, descritta in questa sezione, è "classificazione, budget e flusso".<br/> |
| [Sottoallocazione all'interno dei buffer](large-buffers.md)<br/>                | I buffer hanno tutte le funzionalità necessarie in D3D12 per le applicazioni per trasferire un'ampia gamma di dati temporanei dalla CPU alla GPU. Questa sezione illustra quattro scenari comuni per l'uso e la gestione di risorse e buffer.<br/>                                                                                                                                     |
| [Sottoallocazione all'interno degli heap](suballocation-within-heaps.md)<br/>     | Gli heap delle risorse trasferiscono i dati dalla CPU alla GPU (caricamento) e dalla GPU alla CPU (read-back). <br/>                                                                                                                                                                                                                                                                  |
| [Residency](residency.md)<br/>                                       | Un oggetto viene considerato *residente* quando è accessibile dalla GPU.<br/>                                                                                                                                                                                                                                                                                                |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida per programmatori Direct3D 12](directx-12-programming-guide.md)
</dt> <dt>

[Associazione di risorse](resource-binding.md)
</dt> </dl>

 

 





