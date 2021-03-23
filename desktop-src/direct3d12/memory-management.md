---
title: Gestione della memoria in Direct3D 12
description: Il passaggio a D3D12 comporta una corretta sincronizzazione e gestione della residenza di memoria.
ms.assetid: 94D47EBB-8060-49F6-A1FF-8B7B98AD5363
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 037a2d75adcde6ff03adf2ccee8ce30d33d090c7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "74103649"
---
# <a name="memory-management-in-direct3d-12"></a>Gestione della memoria in Direct3D 12

Il passaggio a D3D12 comporta una corretta sincronizzazione e gestione della residenza di memoria. La gestione della residenza della memoria significa che è necessario eseguire ancora più sincronizzazioni. In questa sezione vengono illustrate le strategie di gestione della memoria e le sottoallocazioni all'interno di heap e buffer.

-   [In questa sezione](#in-this-section)
-   [Argomenti correlati](#related-topics)

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                       | Descrizione                                                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Strategie di gestione della memoria](memory-management-strategies.md)<br/> | Un gestore della memoria per Direct3D 12 potrebbe essere molto complicato rapidamente con tutti i diversi livelli di supporto, per gli adapter UMA o discreti (non-UMA) e con una vasta gamma di differenze di architettura tra gli adattatori GPU.<br/> La strategia consigliata per la gestione della memoria di Direct3D 12, descritta in questa sezione, è "classificazione, budget e flusso".<br/> |
| [Sottoallocazione nei buffer](large-buffers.md)<br/>                | I buffer hanno tutte le funzionalità necessarie in D3D12 per le applicazioni per trasferire una vasta gamma di dati temporanei dalla CPU alla GPU. Questa sezione illustra quattro scenari comuni per l'uso e la gestione delle risorse e dei buffer.<br/>                                                                                                                                     |
| [Sottoallocazione negli heap](suballocation-within-heaps.md)<br/>     | Gli heap delle risorse trasferiscono i dati dalla CPU alla GPU (caricamento) e dalla GPU alla CPU (lettura indietro). <br/>                                                                                                                                                                                                                                                                  |
| [Residenza](residency.md)<br/>                                       | Un oggetto viene considerato *residente* quando è accessibile dalla GPU.<br/>                                                                                                                                                                                                                                                                                                |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida per programmatori Direct3D 12](directx-12-programming-guide.md)
</dt> <dt>

[Associazione di risorse](resource-binding.md)
</dt> </dl>

 

 





