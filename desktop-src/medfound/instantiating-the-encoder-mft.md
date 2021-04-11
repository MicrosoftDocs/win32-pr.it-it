---
description: Creazione di un'istanza di un codificatore MFT
ms.assetid: 50b71c00-b7cf-4c38-8114-bb36b358fda5
title: Creazione di un'istanza di un codificatore MFT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5344c19a3a00c659efbbfd88d42176b876528380
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232536"
---
# <a name="instantiating-an-encoder-mft"></a>Creazione di un'istanza di un codificatore MFT

In Microsoft Media Foundation i codificatori vengono implementati come [trasformazioni di Media Foundation](media-foundation-transforms.md) (MFTS). Prima di creare un codificatore, è necessario innanzitutto trovare il codificatore più adatto alle proprie esigenze.

-   Codec audio Windows Media

    Categoria: **\_ \_ \_ codificatore audio della categoria MFT**

    Tipo principale: MFMediaType \_ audio

    Sottotipo: MFAudioFormat \_ WMAudioV9, MFAudioFormat \_ WMAudioV8, MFAudioFormat \_ WMAudio \_ Lossless, MFAudioFormat \_ WMASPDIF

-   Codec video di Windows Media

    Categoria: **\_ \_ \_ codificatore video della categoria MFT**

    Tipo principale: video di MFMediaType \_

    Sottotipo: MFVideoFormat \_ WVC1, MFVideoFormat \_ WMV3, MFVideoFormat WMV2 \_ , MFVideoFormat \_ WMV1

Media Foundation offre diverse funzioni che l'applicazione può chiamare per enumerare i vari codificatori disponibili nel sistema. I codificatori sono registrati come oggetti COM e la voce del registro di sistema segue il formato standard per le class factory COM. Il registro di sistema gestisce i CLSID per i codificatori, classificati in base al formato multimediale (audio o video). Gli identificatori di classe dei codificatori Windows Media sono definiti come costanti nel file di intestazione wmcodecdsp. h. In Media Foundation, i codificatori possono essere registrati tramite chiamate a [**MFTRegisterLocal**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal) o [**MFTRegisterLocalByCLSID**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocalbyclsid) specificando pullula, i tipi di input supportati e i tipi di output supportati. Una volta completata la registrazione tramite queste funzioni, i MFTs vengono considerati dalle funzioni di enumerazione Media Foundation.

Per creare un'istanza di un codificatore MFT, un'applicazione ha le opzioni seguenti.

-   Creare direttamente il codificatore MFT e ricevere un puntatore all'interfaccia [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) . Per ulteriori informazioni, vedere [creazione di un codificatore tramite CoCreateInstance](using-an-encoder-s-imftransform--interface.md).
-   Creare un'istanza dell'oggetto Activation per il codificatore MFT e ricevere un puntatore all'interfaccia [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) . Per ulteriori informazioni, vedere [utilizzo degli oggetti di attivazione di un codificatore](using-an-encoder-s-activation-objects.md).

Se l'applicazione usa [componenti ASF di livello pipeline](pipeline-layer-asf-components.md) per codificare un file in formato ASF, è necessario inserire il codificatore MFT nella pipeline come nodo di trasformazione. Durante la creazione del nodo Transform nella topologia di codifica, è possibile impostare il tipo di oggetto come puntatore all'interfaccia [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) o all'oggetto [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) . Media Foundation fornisce oggetti attivazione per codificatori Windows Media, in modo che possano essere impostati comodamente come nodo di trasformazione nella topologia di codifica. Quando la topologia viene risolta, la sessione multimediale usa l'oggetto attivazione per creare un'istanza del codificatore MFT.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Codificatori Windows Media](windows-media-encoders.md)
</dt> </dl>

 

 



