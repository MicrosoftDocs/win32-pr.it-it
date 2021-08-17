---
description: Media Foundation trasformazioni
ms.assetid: cb23fe0a-c42c-4912-a0bf-1f0b18a6f4e0
title: Media Foundation trasformazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e61057831383c808a3e05cbe2e9cd779b46522a7a3d52d379b936f27c549d46
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119268701"
---
# <a name="media-foundation-transforms"></a>Media Foundation trasformazioni

Media Foundation trasformazioni (MFT) forniscono un modello generico per l'elaborazione dei dati multimediali. Le MFT vengono usate per decodificatori, codificatori e processori di segnali digitali (DSP). In breve, tutto ciò che si trova nella pipeline multimediale tra l'origine multimediale e il sink multimediale è un MFT.

Questa sezione descrive il modello di programmazione MFT e come implementare un MFT, con raccomandazioni per tipi specifici di MFT, ad esempio decodificatori.



| Argomento                                                                    | Descrizione                                                                                                                                                                                         |
|--------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Informazioni sulle MFT](about-mfts.md)                                             | Offre una breve panoramica dei MFT                                                                                                                                                                   |
| [Modello di elaborazione MFT di base](basic-mft-processing-model.md)             | Descrive in modo più dettagliato il modello di base per l'elaborazione dei dati con un MFT.                                                                                                                           |
| [MFT asincroni](asynchronous-mfts.md)                               | Descrive un modello di elaborazione asincrona che rappresenta un'alternativa al modello di base.<br/> L'elaborazione asincrona è stata introdotta Windows 7. Non tutti i MFT supportano questo modello.<br/> |
| [Registrazione ed enumerazione di MFT](registering-and-enumerating-mfts.md) | Come registrare un MFT e come enumerare MFT nel Registro di sistema.                                                                                                                                   |
| [Restrizioni per il campo di utilizzo](field-of-use-restrictions.md)               | Descrive il meccanismo per sbloccare un MFT con restrizioni sul campo d'uso.                                                                                                                    |
| [Confronto tra MFT e DMO](comparison-of-mfts-and-dmos.md)           | Riepiloga le differenze tra MFT e DMO.                                                                                                                                                   |
| [Scrittura di un MFT personalizzato](writing-a-custom-mft.md)                         | Linee guida per la scrittura di un MFT personalizzato.                                                                                                                                                                |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Media Foundation Pipeline](media-foundation-pipeline.md)
</dt> <dt>

[Architettura di Media Foundation](media-foundation-architecture.md)
</dt> <dt>

[**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
</dt> </dl>

 

 




