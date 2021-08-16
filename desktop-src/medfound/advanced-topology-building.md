---
description: Compilazione avanzata della topologia
ms.assetid: 66aa07d8-6756-4d5b-9f0a-24b902da6fa2
title: Compilazione avanzata della topologia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49d7f2bba412a698d688bc9d88e9935ed0988cc909931634633a0d75b88c2fae
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119664871"
---
# <a name="advanced-topology-building"></a>Compilazione avanzata della topologia

In questa sezione vengono descritte alcune tecniche avanzate per la creazione di topologie. È possibile usare queste tecniche se si vuole un maggiore controllo sulle topologie inviate alla sessione multimediale.

Poiché queste tecniche sono destinate a scenari che vanno oltre le funzionalità fornite dal caricatore di topologia standard, molti dettagli dipendono dai requisiti specifici dell'applicazione. Pertanto, questa sezione è organizzata in modo libero attorno a sottoattività più piccole, anziché a scenari end-to-end completi.

La tipica applicazione di riproduzione segue questi passaggi:

1.  L'applicazione compila una topologia parziale e la accoda nella sessione multimediale.
2.  La sessione multimediale richiama il caricatore della topologia per risolvere la topologia.

Per andare oltre le funzionalità del caricatore della topologia, sono disponibili tre approcci generali:

-   Creare una topologia completa. Quando si accoda la topologia nella sessione multimediale, chiamare [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) con il flag MFSESSION \_ SETTOPOLOGY \_ NORESOLUTION. Questo flag impedisce alla sessione multimediale di tentare di risolvere la topologia.

-   Richiamare direttamente il caricatore della topologia per risolvere la topologia. È quindi possibile modificare la topologia completa prima di eseguire l'accodamento nella sessione multimediale.

-   Implementare un caricatore di topologia personalizzato. Con questo approccio, si accoda una topologia parziale, ma la sessione multimediale richiama il caricatore personalizzato anziché l'implementazione Media Foundation standard. Uno dei vantaggi di questo approccio è che è possibile eseguire la creazione di topologia personalizzata all'interno dell'ambiente protetto. In tal caso, tuttavia, il caricatore della topologia deve essere un componente attendibile. Per altre informazioni, vedere [Percorso supporto protetto.](protected-media-path.md)

In questa sezione vengono trattati gli argomenti seguenti.



| Argomento                                                                          | Descrizione                                                                                                      |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [Caricatori di topologia personalizzati](custom-topology-loaders.md)                         | Come fornire un'implementazione personalizzata [**di IMFTopoLoader**](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader) per la sessione multimediale.          |
| [Associazione di nodi di output a sink multimediali](binding-output-nodes-to-media-sinks.md) | Come preparare i nodi di output in una topologia se si usa il caricatore della topologia all'esterno della sessione multimediale. |
| [Aggiunta di un decodificatore a una topologia](adding-a-decoder-to-a-topology.md)           | Come selezionare manualmente un decodificatore e aggiungerlo a una topologia.                                                       |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Topologie](topologies.md)
</dt> </dl>

 

 



