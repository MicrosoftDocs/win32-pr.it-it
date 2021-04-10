---
description: Configurazione della codifica audio
ms.assetid: 40004f07-0b8c-49cd-9e17-1f6ad7604fbb
title: Configurazione della codifica audio (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e47595f440d10ad0d3c5695f117204f357035d4f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225828"
---
# <a name="configuring-audio-encoding-microsoft-media-foundation"></a>Configurazione della codifica audio (Microsoft Media Foundation)

Il codificatore Windows Media Audio enumera tutti i tipi di output supportati nel formato completo. Recuperare il tipo desiderato chiamando **IMediaObject:: GetOutputType** o **IMFTransform:: GetAvailableOutputType** e quindi impostare il tipo recuperato, inalterato, come tipo di output chiamando **IMediaObject:: SetOutputType** o **IMFTransform:: SetOutputType**.

I tipi di supporto di output supportati dal codificatore audio cambiano in base alla configurazione delle proprietà del codificatore. Prima di enumerare il tipo di output, è necessario configurare tutte le proprietà del codificatore che si desidera utilizzare.

Le modalità Two-pass e VBR sono supportate dai codificatori audio, ma sono configurate in modo diverso rispetto ai video. Per altre informazioni, vedere [enumerazione di tipi audio per modalità di codifica specifiche](enumeratingaudiotypesforspecificencodingmodes.md).

I tipi di input supportati dal codificatore audio non sono disponibili finché non si imposta il tipo di output. Se si chiama **IMediaObject:: GetInputType** o **IMFTransform:: GetInputType** prima di impostare un tipo di output, il metodo restituisce DMO \_ e \_ non \_ più \_ elementi o MFT \_ e \_ non \_ più \_ tipi rispettivamente. Dopo aver impostato il tipo di output, il codificatore enumera i tipi di input supportati per il tipo di output selezionato.

Il codificatore Windows Media Audio non esegue alcun ricampionamento audio. Ciò significa che il tipo di output del codificatore e il tipo di input del codificatore devono avere lo stesso numero di canali, BITS per campione e frequenza di campionamento. Per altre informazioni, vedere [ricerca di tipi di output del codificatore audio](findingaudioencoderoutputtypes.md).

> [!Note]  
>    Ogni tipo di output enumerato dal codificatore audio contiene una struttura **WAVEFORMATEX** (a cui **fa riferimento am \_ media \_ Type. pbFormat**) con dati estesi aggiunti. La dimensione dei dati estesi è specificata da **WAVEFORMATEX. cbSize**. Questi dati devono essere conservati con il contenuto codificato in modo che possano essere recapitati al decodificatore. Il contenuto non può essere decompresso senza i dati in formato esteso.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Utilizzo di audio](workingwithaudio.md)
</dt> </dl>

 

 



