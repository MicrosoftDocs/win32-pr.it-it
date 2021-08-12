---
description: Un codificatore converte audio o video non compresso in pacchetti compressi nel formato specificato dall'applicazione. Per convertire i file multimediali in formato ASF, è possibile usare i codec audio e video Windows media.
ms.assetid: 6dcf12d0-ea37-446b-a807-2b27fd1f6124
title: Windows Codificatori multimediali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d79ff55e98227c63e9761a8dec5ae068c8b1786c067230548ad0028dbe301a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118237290"
---
# <a name="windows-media-encoders"></a>Windows Codificatori multimediali

Un codificatore converte audio o video non compresso in pacchetti compressi nel formato specificato dall'applicazione. Per convertire i file multimediali in formato ASF, è possibile usare i codec audio e video Windows media.

Un codificatore è identificato dal GUID che rappresenta la categoria: audio o video. Il tipo di output del codificatore è rappresentato dalla principale di un tipo di supporto e dal GUID del sottotipo.

-   Windows Codec audio multimediali

    Categoria: **CODIFICATORE \_ AUDIO DI CATEGORIA \_ \_ MFT**

    Tipo principale: audio \_ MFMediaType

    SubType: MFAudioFormat \_ WMAudioV9, MFAudioFormat \_ WMAudioV8, MFAudioFormat \_ WMAudio \_ Lossless, MFAudioFormat \_ WMASPDIF

-   Windows Codec video multimediali

    Categoria: **CODIFICATORE \_ VIDEO DI CATEGORIA \_ \_ MFT**

    Tipo principale: video \_ MFMediaType

    SubType: MFVideoFormat \_ WVC1, MFVideoFormat \_ WMV3, MFVideoFormat \_ WMV2, MFVideoFormat \_ WMV1

Questi codificatori vengono implementati [come Media Foundation transform](media-foundation-transforms.md) (MFT) e Media Foundation l'accesso all'applicazione tramite l'interfaccia [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) del codificatore. Se si usano componenti del livello pipeline per la codifica ASF, il codificatore MFT viene inserito nella pipeline come nodo di trasformazione perché è responsabile della trasformazione dei dati multimediali che passano attraverso l'origine al sink. Se l'origine è un tipo compresso, la pipeline aggiunge i decodificatori necessari per convertire l'origine in un tipo non compresso. Un codificatore ha un flusso di input e un flusso di output. Il codificatore riceve i dati di input e produce dati codificati in base alla configurazione e al formato impostati dall'applicazione prima della sessione di codifica. Il formato del flusso di output è descritto da un tipo di supporto.

In questa sezione vengono trattati gli argomenti seguenti.



| Argomento                                                                              | Descrizione                                                                                 |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [Creazione di un'istanza di un codificatore MFT](instantiating-the-encoder-mft.md)                  | Viene illustrato come creare il codificatore.                                                         |
| [Proprietà di codifica](configuring-the-encoder.md)                                 | Viene illustrato come configurare il codificatore impostando le proprietà appropriate sul codificatore MFT. |
| [Negoziazione del tipo di supporto nel codificatore](media-type-negotiation-on-the-encoder.md) | Viene illustrato come impostare i tipi di supporti di input e output nel codificatore.                            |
| [Configurazione di un codificatore WMV](configuring-a-wmv-encoder.md)                         | Illustra come configurare un codificatore Windows Media Video (WMV).                              |
| [Impostazione di un tipo di output per un codificatore WMA](configuring-a-wma-encoder.md)          | Illustra come impostare un tipo di output in un Windows WMA (Media Audio).                  |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Componenti ASF del livello pipeline](pipeline-layer-asf-components.md)
</dt> </dl>

 

 



