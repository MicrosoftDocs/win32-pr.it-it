---
description: Trasformazioni Media Foundation
ms.assetid: cb23fe0a-c42c-4912-a0bf-1f0b18a6f4e0
title: Trasformazioni Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa0518ced06169f6d998bdad1747878d109e0676
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320707"
---
# <a name="media-foundation-transforms"></a>Trasformazioni Media Foundation

Le trasformazioni Media Foundation (MFTs) forniscono un modello generico per l'elaborazione dei dati multimediali. MFTs vengono usati per i decodificatori, i codificatori e i processori di segnale digitale (DSP). In breve, tutto ciò che si trova nella pipeline multimediale tra l'origine multimediale e il sink multimediale è un MFT.

In questa sezione viene descritto il modello di programmazione MFT e viene illustrato come implementare un MFT, con consigli per tipi specifici di MFTs, ad esempio i decodificatori.



| Argomento                                                                    | Descrizione                                                                                                                                                                                         |
|--------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Informazioni su MFTs](about-mfts.md)                                             | Viene fornita una breve panoramica di MFTs                                                                                                                                                                   |
| [Modello di elaborazione MFT di base](basic-mft-processing-model.md)             | Viene descritto in dettaglio il modello di base per l'elaborazione dei dati con un MFT.                                                                                                                           |
| [MFTs asincrono](asynchronous-mfts.md)                               | Descrive un modello di elaborazione asincrona che rappresenta un'alternativa al modello di base.<br/> L'elaborazione asincrona è stata introdotta in Windows 7. Non tutte le MFT supportano questo modello.<br/> |
| [Registrazione ed enumerazione di MFTs](registering-and-enumerating-mfts.md) | Come registrare un MFT e come enumerare MFTs nel registro di sistema.                                                                                                                                   |
| [Limitazioni per l'utilizzo dei campi](field-of-use-restrictions.md)               | Viene descritto il meccanismo per sbloccare un MFT con restrizioni di campo per l'utilizzo.                                                                                                                    |
| [Confronto tra MFT e DMO](comparison-of-mfts-and-dmos.md)           | Riepiloga le differenze tra MFTs e DMOs.                                                                                                                                                   |
| [Scrittura di un MFT personalizzato](writing-a-custom-mft.md)                         | Linee guida per la scrittura di un MFT personalizzato.                                                                                                                                                                |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Pipeline Media Foundation](media-foundation-pipeline.md)
</dt> <dt>

[Architettura di Media Foundation](media-foundation-architecture.md)
</dt> <dt>

[**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
</dt> </dl>

 

 




