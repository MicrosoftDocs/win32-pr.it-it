---
description: Le modalità di codifica a due passi sono supportate da Windows codificatori multimediali e Media Foundation a livello di pipeline.
ms.assetid: 3fd5baff-142f-453e-bb97-b355ee6678fc
title: Come creare una topologia per la codifica Two-Pass Windows media
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 525a98faa424371f2d80739e5c68f199cfc7ed6443c25ab3d15b575afdd003e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119724881"
---
# <a name="how-to-create-a-topology-for-two-pass-windows-media-encoding"></a>Come creare una topologia per la codifica Two-Pass Windows media

Le modalità di codifica a due passi sono supportate da Windows codificatori multimediali e Media Foundation a livello di pipeline. L'applicazione deve configurare e configurare la topologia di codifica simile a quella nella codifica a passaggio singolo, ma nella modalità di codifica a 2 passi l'applicazione deve eseguire la sessione di codifica due volte. Al primo passaggio, il codificatore raccoglie informazioni sul contenuto del flusso. Al secondo passaggio, usando le informazioni raccolte al primo passaggio, viene generato il file di output finale. Elaborando due volte gli esempi per il flusso, la codifica a due passi ottimizza il processo di codifica e produce file codificati di qualità superiore. Le modalità di codifica a due passi non possono essere usate nei flussi live.

Media Foundation supporta le modalità di codifica a due passaggi seguenti:

-   [Codifica a velocità in bit variabile non vincolata](unconstrained-variable-bit-rate--vbr--encoding.md)
-   [Codifica della velocità in bit delle variabili con vincoli di picco](peak-constrained-variable-bit-rate--vbr--encoding.md)

La creazione di una topologia di codifica per la codifica a due passi è simile alle modalità a passaggio singolo. L'elenco seguente illustra le differenze principali.

-   La configurazione del codificatore deve includere la proprietà [**MFPKEY \_ PASSESUSED**](mfpkey-passesusedproperty.md) impostata su 2 e la proprietà [**MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md) su VARIANT \_ TRUE. In questo modo le funzionalità del codificatore vengono filtrate in modalità a due passi. Se si usano oggetti attivazione, passare queste proprietà a [**MFCreateWMAEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) o [**MFCreateWMVEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmvencoderactivate).
-   Per il primo passaggio, usare un sink multimediale fittizio nel nodo di output perché gli esempi generati in questo passaggio non vengono aggiunti al file finale.
-   Per il secondo passaggio, eseguire una query sul codificatore per le proprietà di post-codifica necessarie e sostituire il nodo sink del supporto fittizio con il sink multimediale asf con queste proprietà impostate.

Per altre informazioni sulla configurazione di una topologia di codifica, vedere [Esercitazione: Single Pass Windows Media Encoding](tutorial--1-pass-windows-media-encoding.md).

La procedura seguente riepiloga i passaggi per la codifica Windows contenuto multimediale in un contenitore ASF usando una modalità di codifica a due passaggi.

1.  Crea un'origine multimediale per l'oggetto specificato utilizzando il resolver di origine.
2.  Enumerare i flussi nell'origine multimediale.
3.  Creare il sink multimediale asf e aggiungere i sink di flusso a seconda dei flussi nell'origine multimediale che devono essere codificati.
4.  Creare il sink multimediale.
5.  Creare il Windows codificatori multimediali per i flussi nel file di output.
6.  Configurare i codificatori con le proprietà di codifica a 2 passi.
7.  Creare una topologia di codifica parziale connettendo l'origine, i codificatori e il sink multimediale.
8.  Creare un'istanza della sessione multimediale e impostare la topologia nella sessione multimediale.
9.  Eseguire il primo passaggio di codifica controllando la sessione multimediale e ottenendo tutti gli eventi pertinenti dalla sessione multimediale.
10. Chiudere e arrestare la sessione di codifica.
11. Eseguire una query sul codificatore per le proprietà seguenti a seconda del tipo di codifica: 

    | Tipo di codifica                                                                                        | Nome proprietà                                                                                                                                                                                                                                                                                                                                                     |
    |------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | [Codifica a velocità in bit variabile non vincolata](unconstrained-variable-bit-rate--vbr--encoding.md)       | [**MFPKEY \_ PASSESUSED**](mfpkey-passesusedproperty.md)<br/> [**MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md)<br/> [**MFPKEY \_ BAVG**](mfpkey-bavgproperty.md)<br/> [**MFPKEY \_ RAVG**](mfpkey-ravgproperty.md)<br/>                                                                                                               |
    | [Codifica della velocità in bit delle variabili con vincoli di picco](peak-constrained-variable-bit-rate--vbr--encoding.md) | [**MFPKEY \_ PASSESUSED**](mfpkey-passesusedproperty.md)<br/> [**MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md)<br/> [**MFPKEY \_ BAVG**](mfpkey-bavgproperty.md)<br/> [**MFPKEY \_ RAVG**](mfpkey-ravgproperty.md)<br/> [**MFPKEY \_ BMAX**](mfpkey-bmaxproperty.md)<br/> [**MFPKEY \_ RMAX**](mfpkey-rmaxproperty.md)<br/> |

    

     

12. Creare il sink del file ASF e aggiungere i sink di flusso necessari a seconda dei flussi da includere nel file di output finale.
13. Impostare le proprietà del codificatore recuperate nel passaggio 11 nel sink del file.
14. Sostituire il sink multimediale nel nodo di output con il sink di file appena creato.
15. Creare un'istanza della sessione multimediale e impostare la topologia aggiornata nella sessione multimediale.
16. Eseguire il secondo passaggio di codifica controllando la sessione multimediale e ottenendo tutti gli eventi pertinenti dalla sessione multimediale.
17. Attendere [l'evento MEEndOfPresentation](meendofpresentation.md) dalla sessione multimediale e nel gestore eventi ottenere i valori delle proprietà di codifica dal codificatore e impostarli nel sink del file. Per altre informazioni, vedere "Aggiornare le proprietà di codifica nel sink di file" in [Esercitazione: Single Pass Windows media encoding](tutorial--1-pass-windows-media-encoding.md).
18. Chiudere e arrestare la sessione di codifica.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Componenti ASF del livello pipeline](pipeline-layer-asf-components.md)
</dt> </dl>

 

 




