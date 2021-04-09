---
description: Le modalità di codifica a due passaggi sono supportate da determinati codificatori Windows Media e Media Foundation a livello di pipeline.
ms.assetid: 3fd5baff-142f-453e-bb97-b355ee6678fc
title: Come creare una topologia per la codifica Two-Pass Windows Media
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c813b9a3c31fafaa3efbea83180c997bc46079d
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "103968887"
---
# <a name="how-to-create-a-topology-for-two-pass-windows-media-encoding"></a>Come creare una topologia per la codifica Two-Pass Windows Media

Le modalità di codifica a due passaggi sono supportate da determinati codificatori Windows Media e Media Foundation a livello di pipeline. Nell'applicazione deve essere configurata e configurata la topologia di codifica simile a quella della codifica a passaggio singolo, ma nella modalità di codifica a 2 passaggi, l'applicazione deve eseguire due volte la sessione di codifica. Al primo passaggio, il codificatore raccoglie informazioni sul contenuto del flusso. Al secondo passaggio, usando le informazioni raccolte al primo passaggio, viene generato il file di output finale. Elaborando due volte gli esempi per il flusso, la codifica a due passaggi ottimizza il processo di codifica e produce file codificati di qualità superiore. Non è possibile usare le modalità di codifica a due passaggi sui flussi live.

Media Foundation supporta le seguenti modalità di codifica a due passaggi:

-   [Codifica della velocità in bit variabile non vincolata](unconstrained-variable-bit-rate--vbr--encoding.md)
-   [Codifica della velocità in bit a variabili con vincoli di picco](peak-constrained-variable-bit-rate--vbr--encoding.md)

La creazione di una topologia di codifica per la codifica a due passaggi è simile a quella delle modalità single-pass. Nell'elenco seguente vengono illustrate le differenze principali.

-   La configurazione del codificatore deve includere la proprietà [**\_ PASSESUSED di MFPKEY**](mfpkey-passesusedproperty.md) impostata su 2 e la proprietà [**MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md) su Variant \_ true. Questa operazione consente di filtrare le funzionalità del codificatore in modalità a due passaggi. Se si usano oggetti Activation, passare queste proprietà a [**MFCreateWMAEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) o [**MFCreateWMVEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmvencoderactivate).
-   Per il primo passaggio, usare un sink di supporti fittizio nel nodo di output perché gli esempi generati in questo passaggio non vengono aggiunti al file finale.
-   Per la seconda sessione, eseguire una query sul codificatore per le proprietà post-codifica richieste e sostituire il nodo del sink multimediale fittizio con il sink multimediale ASF con queste proprietà impostate.

Per ulteriori informazioni sulla configurazione di una topologia di codifica, vedere [esercitazione: codifica Windows Media single pass](tutorial--1-pass-windows-media-encoding.md).

Nella procedura riportata di seguito vengono riepilogati i passaggi per la codifica di contenuto Windows Media in un contenitore ASF utilizzando una modalità di codifica a due passaggi.

1.  Creare un'origine multimediale per l'oggetto specificato utilizzando il resolver di origine.
2.  Enumerare i flussi nell'origine multimediale.
3.  Creare il sink multimediale ASF e aggiungere i sink di flusso a seconda dei flussi nell'origine multimediale che devono essere codificati.
4.  Creare il sink multimediale.
5.  Creare i codificatori Windows Media per i flussi nel file di output.
6.  Configurare i codificatori con le proprietà di codifica a 2 passaggi.
7.  Creare una topologia di codifica parziale connettendo l'origine, i codificatori e il sink multimediale.
8.  Creare un'istanza della sessione multimediale e impostare la topologia nella sessione multimediale.
9.  Eseguire il primo passaggio di codifica controllando la sessione multimediale e ottenendo tutti gli eventi rilevanti dalla sessione multimediale.
10. Chiudere e arrestare la sessione di codifica.
11. Eseguire una query sul codificatore per le proprietà seguenti a seconda del tipo di codifica: 

    | Tipo di codifica                                                                                        | Nome proprietà                                                                                                                                                                                                                                                                                                                                                     |
    |------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | [Codifica della velocità in bit variabile non vincolata](unconstrained-variable-bit-rate--vbr--encoding.md)       | [**\_PASSESUSED MFPKEY**](mfpkey-passesusedproperty.md)<br/> [**\_VBRENABLED MFPKEY**](mfpkey-vbrenabledproperty.md)<br/> [**\_BAVG MFPKEY**](mfpkey-bavgproperty.md)<br/> [**\_RAVG MFPKEY**](mfpkey-ravgproperty.md)<br/>                                                                                                               |
    | [Codifica della velocità in bit a variabili con vincoli di picco](peak-constrained-variable-bit-rate--vbr--encoding.md) | [**\_PASSESUSED MFPKEY**](mfpkey-passesusedproperty.md)<br/> [**\_VBRENABLED MFPKEY**](mfpkey-vbrenabledproperty.md)<br/> [**\_BAVG MFPKEY**](mfpkey-bavgproperty.md)<br/> [**\_RAVG MFPKEY**](mfpkey-ravgproperty.md)<br/> [**\_BMAX MFPKEY**](mfpkey-bmaxproperty.md)<br/> [**\_Rmax MFPKEY**](mfpkey-rmaxproperty.md)<br/> |

    

     

12. Creare il sink di file ASF e aggiungere i sink di flusso necessari a seconda dei flussi che si desidera includere nel file di output finale.
13. Impostare le proprietà del codificatore recuperate nel passaggio 11 sul sink di file.
14. Sostituire il sink multimediale nel nodo di output con il sink di file appena creato.
15. Creare un'istanza della sessione multimediale e impostare la topologia aggiornata nella sessione multimediale.
16. Eseguire il secondo passaggio di codifica controllando la sessione multimediale e ricevendo tutti gli eventi rilevanti dalla sessione multimediale.
17. Attendere l'evento [MEEndOfPresentation](meendofpresentation.md) dalla sessione multimediale e nel gestore dell'evento ottenere i valori delle proprietà di codifica dal codificatore e impostarli nel sink di file. Per ulteriori informazioni, vedere l'argomento relativo all'aggiornamento delle proprietà di codifica nel sink di file in [esercitazione: codifica Windows Media single pass](tutorial--1-pass-windows-media-encoding.md).
18. Chiudere e arrestare la sessione di codifica.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Componenti ASF a livello pipeline](pipeline-layer-asf-components.md)
</dt> </dl>

 

 




