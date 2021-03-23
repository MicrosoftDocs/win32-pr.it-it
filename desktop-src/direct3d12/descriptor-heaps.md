---
title: Heap descrittore
description: Un heap del descrittore è una raccolta di allocazioni contigue di descrittori, un'allocazione per ogni descrittore.
ms.assetid: 04d3facf-21ec-45ca-ad9b-78fdcddc7136
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f19821cff5e8730c376e5c80fef07e67974d31d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104655"
---
# <a name="descriptor-heaps"></a>Heap descrittore

Un heap del descrittore è una raccolta di allocazioni contigue di descrittori, un'allocazione per ogni descrittore.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                             | Descrizione                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Cenni preliminari sugli heap di descrittori](descriptor-heaps-overview.md)<br/>                             | Gli heap del descrittore contengono molti tipi di oggetto che non fanno parte di un oggetto di stato della pipeline (PSO), ad esempio viste di risorse shader (SRVs), viste di accesso non ordinate (UAV), viste del buffer costante (CBVs) e Samplers. <br/>                |
| [Livelli hardware](hardware-support.md)<br/>                                                 | I livelli di hardware dal livello 1 al livello 3 hanno risorse crescenti disponibili per la pipeline. <br/>                                                                                                                              |
| [Heap del descrittore visibile dello shader](shader-visible-descriptor-heaps.md)<br/>                 | Gli heap del descrittore visibile dello shader sono heap di descrittori a cui possono fare riferimento gli shader tramite le tabelle dei descrittori.<br/>                                                                                                              |
| [Heap descrittori non shader visibili](non-shader-visible-descriptor-heaps.md)<br/>         | Per gli shader non è possibile fare riferimento ad alcuni heap del descrittore tramite le tabelle dei descrittori, ma esistono per supportare l'app nella gestione temporanea dei descrittori prima di registrare un elenco di comandi o perché non è necessario alcun heap visibile dello shader.<br/> |
| [Creazione di heap descrittore](creating-descriptor-heaps.md)<br/>                             | Per creare e configurare un heap del descrittore, è necessario selezionare un tipo di heap del descrittore, determinare il numero di descrittori in esso contenuti e impostare i flag che indicano se si tratta di una CPU visibile e/o uno shader visibile. <br/>                    |
| [Impostazione e popolamento degli heap descrittore](setting-descriptor-heaps.md)<br/>                | I tipi di heap del descrittore che è possibile impostare in un elenco di comandi sono quelli che contengono descrittori per cui è possibile usare le tabelle dei descrittori (al massimo uno per volta). <br/>                                                        |
| [Riepilogo di configurabilità heap descrittore](descriptor-heap-configurability-summary.md)<br/> | Nella tabella seguente sono riepilogate le informazioni sullo shader e sul supporto dell'heap visibile non shader.<br/>                                                                                                                                    |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Descrittori](descriptors.md)
</dt> <dt>

[Tabelle descrittore](descriptor-tables.md)
</dt> <dt>

[**ID3D12DescriptorHeap**](/windows/desktop/api/d3d12/nn-d3d12-id3d12descriptorheap)
</dt> <dt>

[Associazione di risorse](resource-binding.md)
</dt> <dt>

[Firme radice](root-signatures.md)
</dt> </dl>

 

 





