---
description: Compilazione avanzata della topologia
ms.assetid: 66aa07d8-6756-4d5b-9f0a-24b902da6fa2
title: Compilazione avanzata della topologia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b4cc061d4e557dda4ccbb81eabc55e8e1b3e33b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343336"
---
# <a name="advanced-topology-building"></a>Compilazione avanzata della topologia

In questa sezione vengono descritte alcune tecniche avanzate per la creazione di topologie. È possibile utilizzare queste tecniche se si desidera un maggiore controllo sulle topologie inviate alla sessione multimediale.

Poiché queste tecniche sono destinate a scenari che vanno oltre la funzionalità fornita dal caricatore della topologia standard, molti dei dettagli dipendono dai requisiti specifici dell'applicazione. Questa sezione è quindi organizzata in modo più ampio per le sottoattività più piccole, anziché per completare gli scenari end-to-end.

L'applicazione di riproduzione tipica segue questa procedura:

1.  L'applicazione compila una topologia parziale e la accoda nella sessione multimediale.
2.  La sessione multimediale richiama il caricatore della topologia per risolvere la topologia.

Se si vuole superare le funzionalità del caricatore della topologia, sono disponibili tre approcci generali:

-   Creare una topologia completa. Quando si accoda la topologia nella sessione multimediale, chiamare [**IMFMediaSession:: la topologia**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) con il \_ flag MFSESSION della topologia \_ NoSolution. Questo flag impedisce alla sessione multimediale di tentare di risolvere la topologia.

-   Richiamare direttamente il caricatore della topologia per risolvere la topologia. È quindi possibile modificare la topologia completa prima di accodarla nella sessione multimediale.

-   Implementare un caricatore di topologia personalizzato. Con questo approccio, viene accodata una topologia parziale, ma la sessione multimediale richiama il caricatore personalizzato invece dell'implementazione di Media Foundation standard. Un vantaggio di questo approccio è che è possibile eseguire la compilazione di topologia personalizzata all'interno dell'ambiente protetto. In tal caso, tuttavia, il caricatore della topologia deve essere un componente attendibile. Per ulteriori informazioni, vedere [percorso multimediale protetto](protected-media-path.md).

In questa sezione vengono trattati gli argomenti seguenti.



| Argomento                                                                          | Descrizione                                                                                                      |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [Caricatori topologia personalizzati](custom-topology-loaders.md)                         | Come fornire un'implementazione personalizzata di [**IMFTopoLoader**](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader) per la sessione multimediale.          |
| [Associazione di nodi di output a sink di supporto](binding-output-nodes-to-media-sinks.md) | Come preparare i nodi di output in una topologia se si usa il caricatore della topologia al di fuori della sessione multimediale. |
| [Aggiunta di un decodificatore a una topologia](adding-a-decoder-to-a-topology.md)           | Come selezionare un decodificatore manualmente e aggiungerlo a una topologia.                                                       |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Topologie](topologies.md)
</dt> </dl>

 

 



