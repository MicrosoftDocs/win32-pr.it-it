---
description: Questo argomento descrive come usare i profili ASF in Microsoft Media Foundation.
ms.assetid: 03a0981b-29c3-450d-aa58-bc56a76e6cb6
title: Profilo ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d38d5d2c869bd8af61289fa15361d216f686abac4eaa366b3c036f40338d355
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035524"
---
# <a name="asf-profile"></a>Profilo ASF

Questo argomento descrive come usare i profili ASF in Microsoft Media Foundation.

Un file ASF (Advanced Systems Format) contiene uno o più flussi. Per ogni flusso, l'intestazione ASF contiene un'intestazione delle proprietà del flusso che descrive il flusso. A livello [WMContainer,](wmcontainer-asf-components.md) per impostare o leggere le proprietà dei flussi ASF vengono usati gli oggetti seguenti:

-   *Oggetto profilo ASF:* descrive i flussi e le relative relazioni tra loro. L'oggetto profilo ASF espone [**l'interfaccia IMFASFProfile.**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile)
-   *Oggetto di configurazione* stream: descrive un flusso. L'oggetto di configurazione del flusso contiene un tipo di supporto che descrive il formato del flusso. Per i flussi audio e video, il tipo di contenuto multimediale descrive esattamente come viene configurato il flusso e viene usato dai codec che codificano o decodificano il flusso. L'oggetto di configurazione del flusso espone [**l'interfaccia IMFASFStreamConfig.**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) Un profilo ASF valido contiene almeno un oggetto di configurazione del flusso.
-   *Oggetto di* esclusione reciproca: descrive più flussi che non devono essere letti contemporaneamente. Un oggetto di esclusione reciproca espone [**l'interfaccia IMFASFMutualExclusion.**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfmutualexclusion) Un profilo ASF contiene zero o più oggetti di esclusione reciproca.

Il diagramma seguente illustra la relazione tra il profilo asf e gli oggetti contenuti nel profilo.

![diagramma ad albero di un nodo del profilo asf con nodi figlio di configurazione del flusso; il primo punta al tipo di supporto, i due successivi all'esclusione reciproca](images/asf-components02.png)

Per la riproduzione, il profilo ASF viene usato per enumerare i flussi e trovare i formati di flusso. Per la codifica, il profilo ASF viene usato per configurare i flussi nel file di destinazione.

Il profilo ASF viene usato anche per configurare il [sink multimediale di ASF.](asf-media-sinks.md) Per ogni flusso nel profilo ASF, il sink multimediale di ASF crea un sink di flusso corrispondente.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                           | Descrizione                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [Creazione di un profilo ASF](creating-an-asf-profile.md)<br/>                               | Viene descritto come creare un oggetto profilo ASF.<br/>          |
| [Creazione e configurazione di asf Flussi](creating-and-configuring-asf-streams.md)<br/>     | Viene descritto come aggiungere flussi a un profilo ASF.<br/>         |
| [Uso dell'esclusione reciproca per asf Flussi](using-mutual-exclusion-for-asf-streams.md)<br/> | Viene descritto come aggiungere esclusioni reciproche ai flussi ASF. <br/> |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tipi di supporti](media-types.md)
</dt> <dt>

[Esercitazione: Codifica multimediale Windows 1 passaggio](tutorial--1-pass-windows-media-encoding.md)
</dt> <dt>

[Esercitazione: Scrittura di un file WMA usando la codifica CBR](tutorial--writing-a-wma-file-by-using-cbr-encoding.md)
</dt> <dt>

[Componenti ASF WMContainer](wmcontainer-asf-components.md)
</dt> </dl>

 

 




