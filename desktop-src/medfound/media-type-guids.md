---
description: Tipi di supporti principali
ms.assetid: 1cca3539-a920-4938-93b9-ae41e1c0a287
title: Tipi di supporti principali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a93a1aa430a720ff4b2f3591071d0bc8b178d6a
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "103968942"
---
# <a name="major-media-types"></a>Tipi di supporti principali

In un tipo di supporto, il *tipo principale* descrive la categoria complessiva dei dati, ad esempio audio o video. Il *sottotipo*, se presente, perfeziona ulteriormente il tipo principale. Se, ad esempio, il tipo principale è video, il sottotipo potrebbe essere video RGB a 32 bit. I sottotipi distinguono inoltre formati codificati, ad esempio video H. 264, da formati non compressi.

Il tipo e il sottotipo principali sono identificati dai GUID e archiviati negli attributi seguenti:



| Attributo                                             | Descrizione |
|-------------------------------------------------------|-------------|
| [\_ \_ tipo principale MF \_ mt](mf-mt-major-type-attribute.md) | Tipo principale. |
| [sottotipo MF \_ mt \_](mf-mt-subtype-attribute.md)        | Sottotipo.    |



 

Sono definiti i seguenti tipi principali.



| Tipo principale                    | Descrizione                                                                                                                                                | Sottotipi                                             |
|-------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| **\_Audio MFMediaType**        | Audio.                                                                                                                                                     | [GUID del sottotipo audio](audio-subtype-guids.md).      |
| **\_Binario MFMediaType**       | Flusso binario.                                                                                                                                             | Nessuna.                                                |
| **MFMediaType \_ filetransfer** | Flusso contenente file di dati.                                                                                                                         | Nessuna.                                                |
| **\_HTML MFMediaType**         | Flusso HTML.                                                                                                                                               | Nessuna.                                                |
| **Immagine di MFMediaType \_**        | Flusso di immagini ancora.                                                                                                                                        | [GUID e CLSID WIC](../wic/-wic-guids-clsids.md).       |
| **MFMediaType \_ protetto**    | Supporti protetti.                                                                                                                                           | Il sottotipo specifica lo schema di protezione del contenuto. |
| **\_Percezione MFMediaType**   | Flussi da un sensore della fotocamera o da un'unità di elaborazione che motiva e riconosce i dati video non elaborati e fornisce informazioni sull'ambiente o sugli utenti. | Nessuna.                                                |
| **\_Sami MFMediaType**         | Didascalie di Media Interchange accessibili (SAMI) sincronizzate.                                                                                                 | Nessuna.                                                |
| **\_Script MFMediaType**       | Flusso di script.                                                                                                                                             | Nessuna.                                                |
| **\_Flusso MFMediaType**       | Flusso multiplex o elementare.                                                                                                                   | [GUID del sottotipo di flusso](stream-subtype-guids.md)     |
| **Video di MFMediaType \_**        | Video.                                                                                                                                                     | [GUID del sottotipo video](video-subtype-guids.md).      |



 

I componenti di terze parti possono definire nuovi tipi principali e nuovi sottotipi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Tipi di supporto](media-types.md)
</dt> </dl>

 

 
