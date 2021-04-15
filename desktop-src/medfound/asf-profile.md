---
description: In questo argomento viene descritto come utilizzare i profili ASF in Microsoft Media Foundation.
ms.assetid: 03a0981b-29c3-450d-aa58-bc56a76e6cb6
title: Profilo ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 616670e7de68fd73c168c474544fc6236f1586e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524658"
---
# <a name="asf-profile"></a>Profilo ASF

In questo argomento viene descritto come utilizzare i profili ASF in Microsoft Media Foundation.

Un file di formato di sistema avanzato (ASF) contiene uno o più flussi. Per ogni flusso, l'intestazione ASF contiene un'intestazione di proprietà del flusso che descrive il flusso. A livello di [WMContainer](wmcontainer-asf-components.md) , per impostare o leggere le proprietà dei flussi ASF vengono usati gli oggetti seguenti:

-   Oggetto *profilo ASF* : descrive i flussi e le relazioni tra di essi. L'oggetto profilo ASF espone l'interfaccia [**IMFASFProfile**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile) .
-   Oggetto di *configurazione del flusso* : descrive un flusso. L'oggetto di configurazione del flusso contiene un tipo di supporto che descrive il formato del flusso. Per i flussi audio e video, il tipo di supporto descrive esattamente il modo in cui il flusso viene configurato e viene usato dai codec che codificano o decodificano il flusso. L'oggetto di configurazione del flusso espone l'interfaccia [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) . Un profilo ASF valido contiene almeno un oggetto di configurazione del flusso.
-   Oggetto di *esclusione reciproca* : descrive più flussi che non sono previsti per la lettura simultanea. Un oggetto di esclusione reciproca espone l'interfaccia [**IMFASFMutualExclusion**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfmutualexclusion) . Un profilo ASF contiene zero o più oggetti di esclusione reciproca.

Nel diagramma seguente viene illustrata la relazione tra il profilo ASF e gli oggetti contenuti nel profilo.

![diagramma dell'albero di un nodo del profilo ASF con nodi figlio di configurazione del flusso; il primo punto per il tipo di supporto, i successivi due ad esclusione reciproca](images/asf-components02.png)

Per la riproduzione, il profilo ASF viene usato per enumerare i flussi e trovare i formati dei flussi. Per la codifica, il profilo ASF viene usato per configurare i flussi nel file di destinazione.

Il profilo ASF viene utilizzato anche per configurare il [sink multimediale ASF](asf-media-sinks.md). Per ogni flusso nel profilo ASF, il sink multimediale ASF crea un sink di flusso corrispondente.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                           | Descrizione                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [Creazione di un profilo ASF](creating-an-asf-profile.md)<br/>                               | Viene descritto come creare un oggetto profilo ASF.<br/>          |
| [Creazione e configurazione di flussi ASF](creating-and-configuring-asf-streams.md)<br/>     | Viene descritto come aggiungere flussi a un profilo ASF.<br/>         |
| [Uso dell'esclusione reciproca per i flussi ASF](using-mutual-exclusion-for-asf-streams.md)<br/> | Viene descritto come aggiungere esclusioni reciproche ai flussi ASF. <br/> |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tipi di supporto](media-types.md)
</dt> <dt>

[Esercitazione: codifica Windows Media da 1 passaggio](tutorial--1-pass-windows-media-encoding.md)
</dt> <dt>

[Esercitazione: scrittura di un file WMA usando la codifica CBR](tutorial--writing-a-wma-file-by-using-cbr-encoding.md)
</dt> <dt>

[Componenti ASF WMContainer](wmcontainer-asf-components.md)
</dt> </dl>

 

 




