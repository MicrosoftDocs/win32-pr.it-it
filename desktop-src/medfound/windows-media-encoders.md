---
description: Un codificatore converte audio o video non compressi in pacchetti compressi nel formato specificato dall'applicazione. Per convertire i file multimediali in formato ASF, è possibile usare i codec audio e video di Windows Media.
ms.assetid: 6dcf12d0-ea37-446b-a807-2b27fd1f6124
title: Codificatori Windows Media
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a642702562cbb6a70b0380deb196c70c4f8207b6
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320557"
---
# <a name="windows-media-encoders"></a>Codificatori Windows Media

Un codificatore converte audio o video non compressi in pacchetti compressi nel formato specificato dall'applicazione. Per convertire i file multimediali in formato ASF, è possibile usare i codec audio e video di Windows Media.

Un codificatore viene identificato dal GUID che rappresenta la categoria: audio o video. Il tipo di output del codificatore è rappresentato da un elemento principale del tipo di supporto e dal GUID del sottotipo.

-   Codec audio Windows Media

    Categoria: **\_ \_ \_ codificatore audio della categoria MFT**

    Tipo principale: MFMediaType \_ audio

    Sottotipo: MFAudioFormat \_ WMAudioV9, MFAudioFormat \_ WMAudioV8, MFAudioFormat \_ WMAudio \_ Lossless, MFAudioFormat \_ WMASPDIF

-   Codec video di Windows Media

    Categoria: **\_ \_ \_ codificatore video della categoria MFT**

    Tipo principale: video di MFMediaType \_

    Sottotipo: MFVideoFormat \_ WVC1, MFVideoFormat \_ WMV3, MFVideoFormat WMV2 \_ , MFVideoFormat \_ WMV1

Questi codificatori vengono implementati come [Media Foundation Transform](media-foundation-transforms.md) (MFT) e Media Foundation forniscono l'accesso all'applicazione tramite l'interfaccia [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) del codificatore. Se si usano componenti del livello pipeline per la codifica ASF, il codificatore MFT viene inserito nella pipeline come nodo di trasformazione perché è responsabile della trasformazione dei dati multimediali che passano attraverso l'origine al sink. Se l'origine è un tipo compresso, la pipeline aggiunge i decodificatori necessari per convertire l'origine in un tipo non compresso. Un codificatore ha un flusso di input e un flusso di output. Il codificatore riceve i dati di input e produce dati codificati in base alla configurazione e al formato impostati dall'applicazione prima della sessione di codifica. Il formato del flusso di output è descritto da un tipo di supporto.

In questa sezione vengono trattati gli argomenti seguenti.



| Argomento                                                                              | Descrizione                                                                                 |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [Creazione di un'istanza di un codificatore MFT](instantiating-the-encoder-mft.md)                  | Viene illustrato come creare il codificatore.                                                         |
| [Proprietà di codifica](configuring-the-encoder.md)                                 | Viene illustrato come configurare il codificatore impostando le proprietà appropriate nel codificatore MFT. |
| [Negoziazione del tipo di supporto sul codificatore](media-type-negotiation-on-the-encoder.md) | Viene illustrato come impostare i tipi di supporto di input e di output nel codificatore.                            |
| [Configurazione di un codificatore WMV](configuring-a-wmv-encoder.md)                         | Viene illustrato come configurare un codificatore Windows Media Video (WMV).                              |
| [Impostazione di un tipo di output per un codificatore WMA](configuring-a-wma-encoder.md)          | Viene illustrato come impostare un tipo di output in un codificatore Windows Media Audio (WMA).                  |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Componenti ASF a livello pipeline](pipeline-layer-asf-components.md)
</dt> </dl>

 

 



