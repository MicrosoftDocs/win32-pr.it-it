---
description: Creazione di un'istanza di un codificatore MFT
ms.assetid: 50b71c00-b7cf-4c38-8114-bb36b358fda5
title: Creazione di un'istanza di un codificatore MFT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40337bbef63cf243777978d1672a60de5ebfba8874b3cce0271ca06ccf4ab38b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974270"
---
# <a name="instantiating-an-encoder-mft"></a>Creazione di un'istanza di un codificatore MFT

In Microsoft Media Foundation, i codificatori vengono implementati [come](media-foundation-transforms.md) trasformazioni Media Foundation (MFT). Prima di creare un codificatore, è necessario trovare il codificatore più adatto alle proprie esigenze.

-   Windows Codec audio multimediali

    Categoria: **CODIFICATORE \_ \_ AUDIO \_ CATEGORIA MFT**

    Tipo principale: MFMediaType \_ Audio

    SubType: MFAudioFormat \_ WMAudioV9, MFAudioFormat \_ WMAudioV8, MFAudioFormat \_ WMAudio \_ Lossless, MFAudioFormat \_ WMASPDIF

-   Windows Codec video multimediali

    Categoria: **CODIFICATORE \_ \_ VIDEO \_ CATEGORIA MFT**

    Tipo principale: video \_ MFMediaType

    SubType: MFVideoFormat \_ WVC1, MFVideoFormat \_ WMV3, MFVideoFormat \_ WMV2, MFVideoFormat \_ WMV1

Media Foundation fornisce diverse funzioni che l'applicazione può chiamare per enumerare i vari codificatori disponibili nel sistema. I codificatori vengono registrati come oggetti COM e la voce del Registro di sistema segue il formato standard per le class factory COM. Il Registro di sistema gestisce i CLSID per i codificatori, classificati in base al formato multimediale (audio o video). Gli identificatori di classe Windows codificatori multimediali sono definiti come costanti nel file di intestazione wmcodecdsp.h. In Media Foundation, i codificatori possono essere registrati tramite chiamate a [**MFTRegisterLocal**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal) o [**MFTRegisterLocalByCLSID**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocalbyclsid) specificando la catergory, i tipi di input supportati e i tipi di output supportati. Al completamento della registrazione tramite queste funzioni, i MFT vengono considerati dalle Media Foundation di enumerazione.

Per creare un'istanza di un codificatore MFT, un'applicazione ha le opzioni seguenti.

-   Creare direttamente il codificatore MFT e ricevere un puntatore [**all'interfaccia IMFTransform.**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) Per altre informazioni, vedere [Creazione di un codificatore tramite CoCreateInstance.](using-an-encoder-s-imftransform--interface.md)
-   Creare un'istanza dell'oggetto di attivazione per il codificatore MFT e ricevere un puntatore [**all'interfaccia IMFActivate.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) Per altre informazioni, vedere [Uso degli oggetti di attivazione di un codificatore.](using-an-encoder-s-activation-objects.md)

Se l'applicazione usa [componenti ASF](pipeline-layer-asf-components.md) del livello pipeline per codificare un file in formato ASF, è necessario inserire il codificatore MFT nella pipeline come nodo di trasformazione. Durante la creazione del nodo di trasformazione nella topologia di codifica, è possibile impostare il tipo di oggetto come puntatore [**all'interfaccia IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) o [**all'oggetto IMFActivate.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) Media Foundation fornisce oggetti di attivazione per Windows codificatori multimediali in modo che possano essere facilmente impostati come nodo di trasformazione nella topologia di codifica. Quando la topologia viene risolta, la sessione multimediale usa l'oggetto di attivazione per creare un'istanza del codificatore MFT.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Windows Codificatori multimediali](windows-media-encoders.md)
</dt> </dl>

 

 



