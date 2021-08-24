---
description: Negoziazione del tipo di supporto nel codificatore
ms.assetid: c8ae543e-68f7-4c74-9cb7-2a200bd51820
title: Negoziazione del tipo di supporto nel codificatore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20ac5dd5a107633feba4ce2a74da7e9aea7e9f71d51be1b5cad5b85ab4adda35
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119941511"
---
# <a name="media-type-negotiation-on-the-encoder"></a>Negoziazione del tipo di supporto nel codificatore

In Microsoft Media Foundation, i codificatori vengono [](media-foundation-transforms.md) implementati come trasformazioni Media Foundation (MFT) con un input e un output. Prima di una sessione di codifica, un codificatore deve conoscere le caratteristiche del flusso che riceverà come input e il formato del flusso che produrrà come output. È necessario impostare i tipi di supporti di input e output e le caratteristiche correlate prima di passare i dati tramite il codificatore. È necessario specificare i formati di input [](media-type-guids.md) e output specificando i GUID del tipo di [](media-type-attributes.md) supporto appropriati e impostare le caratteristiche del flusso di output impostando gli attributi del tipo di supporto pertinenti nel tipo di supporto di output. Un codificatore di cui è stata appena creata un'istanza non ha alcun tipo di supporto impostato.

Il tipo di supporto di input è un formato non compresso, ad esempio audio PCM o video RGB. I tipi di formato usati dal codificatore sono limitati a quelli descritti dalle **strutture VIDEOINFOHEADER** e **WAVEFORMATEX.** Per altre informazioni su queste strutture, vedere la documentazione Windows SDK. Media Foundation fornisce funzioni helper per creare tipi di file multimediali da strutture di formato. Ad esempio, la funzione [**MFInitMediaTypeFromVideoInfoHeader**](/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromvideoinfoheader) inizializza un tipo di video da una struttura **VIDEOINFOHEADER** e la funzione [**MFInitMediaTypeFromWaveFormatEx**](/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromwaveformatex) inizializza un tipo di video da una struttura **WAVEFORMATEX** o **WAVEFORMATEXTENSIBLE.** Per altre informazioni, vedere [Conversioni di tipi di supporti.](media-type-conversions.md) È necessario impostare il tipo di supporto di input nel codificatore chiamando [**IMFTransform::SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype).

Il tipo di supporto di output è il formato di compressione usato nel flusso o nel file di origine finale. È possibile impostare il tipo di supporto di output disponibile solo dopo aver impostato il tipo di supporto di input. È possibile recuperare i tipi di output supportati chiamando [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) in un ciclo finché il codificatore non restituisce **MF \_ E NO MORE \_ \_ \_ TYPES**. Incrementare l'indice del tipo con ogni iterazione. Quando si trova un tipo di supporto appropriato, impostare il tipo di supporto di output chiamando [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).

Il fattore determinante nella scelta del tipo di supporto di output dipende dal tipo di codifica e dai requisiti di codifica. Ad esempio, per i flussi audio con codifica CBR, si vuole trovare un tipo di supporto che corrisponda all'input e abbia una velocità in bit il più vicina possibile a un valore di destinazione.

Se si vuole usare una modalità di codifica diversa da CBR, è necessario impostare la modalità e quindi enumerare i tipi di output per tale modalità, perché il codificatore modifica i tipi di output supportati a seconda della modalità impostata. Le proprietà che controllano la modalità di codifica [**sono MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md) e [**MFPKEY \_ PASSESUSED.**](mfpkey-passesusedproperty.md) Ad esempio, se si enumerano i tipi di output per la codifica di qualità VBR, il tipo di supporto dipende dal valore di qualità che si decide di usare. Per informazioni sull'impostazione di queste proprietà, vedere [Proprietà di codifica.](configuring-the-encoder.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di un'istanza di un codificatore MFT](instantiating-the-encoder-mft.md)
</dt> <dt>

[Windows Codificatori multimediali](windows-media-encoders.md)
</dt> </dl>

 

 



