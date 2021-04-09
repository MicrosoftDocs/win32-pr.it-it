---
description: Negoziazione del tipo di supporto sul codificatore
ms.assetid: c8ae543e-68f7-4c74-9cb7-2a200bd51820
title: Negoziazione del tipo di supporto sul codificatore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7845e9d50c5d418198dc0e08313e2e9329ffab8
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "103968962"
---
# <a name="media-type-negotiation-on-the-encoder"></a>Negoziazione del tipo di supporto sul codificatore

In Microsoft Media Foundation i codificatori vengono implementati come [trasformazioni di Media Foundation](media-foundation-transforms.md) (MFTS) con un input e un output. Prima di una sessione di codifica, un codificatore deve essere in grado di individuare le caratteristiche del flusso che riceverà come input e il formato del flusso che verrà generato come output. Prima di passare i dati attraverso il codificatore, è necessario impostare i tipi di supporto di input e di output e le relative caratteristiche. Per specificare i formati di input e di output, è necessario specificare i GUID appropriati per il [tipo di supporto](media-type-guids.md) e impostare le caratteristiche del flusso di output impostando gli attributi del [tipo di supporto](media-type-attributes.md) pertinente sul tipo di supporto di output. Un nuovo codificatore di cui è stata creata un'istanza non ha alcun tipo di supporto set.

Il tipo di supporto di input è un formato non compresso, ad esempio audio PCM o video RGB. I tipi di formato utilizzati dal codificatore sono limitati a quelli descritti dalle strutture **VIDEOINFOHEADER** e **WAVEFORMATEX** . Per ulteriori informazioni su queste strutture, vedere la documentazione Windows SDK. Media Foundation fornisce funzioni helper per creare tipi di supporto da strutture di formato. Ad esempio, la funzione [**MFInitMediaTypeFromVideoInfoHeader**](/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromvideoinfoheader) Inizializza un tipo di video da una struttura **VIDEOINFOHEADER** e la funzione [**MFInitMediaTypeFromWaveFormatEx**](/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromwaveformatex) Inizializza un tipo di video da una struttura **WAVEFORMATEX** o **WAVEFORMATEXTENSIBLE** . Per altre informazioni, vedere [conversioni di tipi di supporti](media-type-conversions.md). È necessario impostare il tipo di supporto di input nel codificatore chiamando [**IMFTransform:: SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype).

Il tipo di supporto di output è il formato di compressione usato nel flusso o nel file di origine finale. È possibile impostare il tipo di supporto di output disponibile solo dopo aver impostato il tipo di supporto di input. È possibile recuperare i tipi di output supportati chiamando [**IMFTransform:: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) in un ciclo finché il codificatore **non restituisce MF \_ E \_ non \_ più \_ tipi**. Incrementare l'indice del tipo con ogni iterazione. Quando si trova un tipo di supporto appropriato, impostare il tipo di supporto di output chiamando [**IMFTransform:: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).

Il fattore decisivo nella scelta del tipo di supporto di output dipende dal tipo di codifica e dai requisiti di codifica. Per i flussi audio con codifica CBR, ad esempio, si vuole trovare un tipo di supporto che corrisponda all'input e che abbia una velocità in bit il più vicino possibile a un valore di destinazione.

Se si vuole usare una modalità di codifica diversa da CBR, è necessario impostare la modalità e quindi enumerare i tipi di output per tale modalità, perché il codificatore modifica i tipi di output supportati a seconda della modalità impostata. Le proprietà che controllano la modalità di codifica sono [**MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md) e [**MFPKEY \_ PASSESUSED**](mfpkey-passesusedproperty.md). Se, ad esempio, si enumerano i tipi di output per la codifica di qualità VBR, il tipo di supporto dipende dal valore di qualità che si decide di usare. Per informazioni sull'impostazione di queste proprietà, vedere [Encoding Properties](configuring-the-encoder.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di un'istanza di un codificatore MFT](instantiating-the-encoder-mft.md)
</dt> <dt>

[Codificatori Windows Media](windows-media-encoders.md)
</dt> </dl>

 

 



