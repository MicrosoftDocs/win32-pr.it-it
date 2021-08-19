---
description: Configurazione della codifica audio
ms.assetid: 40004f07-0b8c-49cd-9e17-1f6ad7604fbb
title: Configurazione della codifica audio (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2344808decffd4b50d5926074dbf71d60445580adb4556703367369e1e146d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117880366"
---
# <a name="configuring-audio-encoding-microsoft-media-foundation"></a>Configurazione della codifica audio (Microsoft Media Foundation)

Il Windows media audio enumera tutti i tipi di output supportati nel formato completo. Recuperare il tipo desiderato chiamando **IMediaObject::GetOutputType** o **IMFTransform::GetAvailableOutputType** e quindi impostare il tipo recuperato, non modificato, come tipo di output chiamando **IMediaObject::SetOutputType** o **IMFTransform::SetOutputType**.

I tipi di supporti di output supportati dal codificatore audio cambiano quando vengono configurate le proprietà del codificatore. È necessario configurare tutte le proprietà del codificatore da usare prima di enumerare il tipo di output.

Le modalità a due passi e VBR sono supportate dai codificatori audio, ma sono configurate in modo diverso rispetto al video. Per altre informazioni, vedere [Enumerazione dei tipi audio per modalità di codifica specifiche.](enumeratingaudiotypesforspecificencodingmodes.md)

I tipi di input supportati dal codificatore audio non sono disponibili fino a quando non si imposta il tipo di output. Se si chiama **IMediaObject::GetInputType** o **IMFTransform::GetInputType** prima di impostare un tipo di output, il metodo restituisce rispettivamente DMO E NO MORE ITEMS o \_ \_ \_ \_ MFT \_ E NO \_ MORE \_ \_ TYPES. Dopo aver impostato il tipo di output, il codificatore enumera i tipi di input supportati per il tipo di output selezionato.

Non viene eseguito alcun ricampionamento audio dal Windows Media Audio. Ciò significa che il tipo di output del codificatore e il tipo di input del codificatore devono avere lo stesso numero di canali, bit per campione e frequenza di campionamento. Per altre informazioni, vedere Ricerca [di tipi di output del codificatore audio.](findingaudioencoderoutputtypes.md)

> [!Note]  
>    Ogni tipo di output enumerato dal codificatore audio contiene una struttura **WAVEFORMATEX** (a cui punta **AM MEDIA \_ \_ TYPE.pbFormat)** a cui vengono aggiunti dati estesi. Le dimensioni dei dati estesi sono specificate da **WAVEFORMATEX.cbSize.** Questi dati devono essere conservati con il contenuto codificato in modo che possano essere recapitati al decodificatore. Il contenuto non può essere decompresso senza i dati in formato esteso.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso dell'audio](workingwithaudio.md)
</dt> </dl>

 

 



