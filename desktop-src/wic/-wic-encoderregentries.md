---
description: Voci del registro di sistema Encoder-Specific
ms.assetid: bbb78d70-bd3e-4d5a-ba59-2e17d2d1cf30
title: Voci del registro di sistema Encoder-Specific
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49e6fbfafa1f8d3b340d7e3864fddacb8cd7e282
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314474"
---
# <a name="encoder-specific-registry-entries"></a>Voci del registro di sistema Encoder-Specific


Oltre alle voci elencate in precedenza per il codificatore, è inoltre necessario registrare il codificatore nella categoria dei codificatori Windows Imaging Component (WIC), in modo che il motore di individuazione possa trovarlo. A tale scopo, effettuare le seguenti voci del registro di sistema. Il primo GUID nelle voci seguenti è l'identificatore di categoria (CATId) per WICBitmapEncoders.

```
HKEY_CLASSES_ROOT
   CLSID
      {AC757296-3522-4E11-9862-C17BE5A1767E}
         Instance
            {Encoder CLSID}
               CLSID = {Encoder CLSID}
               FriendlyName = {Name of Encoder}
```

## <a name="registering-a-container-format-with-metadata-writers"></a>Registrazione di un formato contenitore con writer di metadati

Se si crea un nuovo formato del contenitore per il codec, è necessario creare anche le voci del registro di sistema per supportare i writer di metadati per i blocchi di metadati nelle immagini. È necessario creare le voci seguenti nell'identificatore di classe (CLSID) del writer di metadati per ogni formato di metadati supportato nel formato del contenitore. Se il codec usa un contenitore Tagged Image File Format (TIFF), queste informazioni sono già presenti nel registro di sistema e non è necessario creare queste voci.

```
HKEY_CLASSES_ROOT
   CLSID
      {Metadata Writer CLSID}
         Containers
            {Container Format GUID}
               WritePosition = Offset relative to its container
               WriteHeader = Pattern used for metadata header
               WriteOffset = Offset from beginning of header
```

Se si usa un formato di contenitore di tipo TIFF o JPEG, è necessario registrare un'associazione tra il contenitore e il formato del contenitore. Per ulteriori informazioni, vedere l'introduzione all' [integrazione con la raccolta foto di Windows e Esplora risorse](-wic-integrationregentries.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Voci generali del registro di sistema](-wic-generalregentries.md)
</dt> <dt>

[Voci del registro di sistema specifiche del codificatore](-wic-decoderregentries.md)
</dt> <dt>

[Come scrivere un CODEC WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[Panoramica del componente imaging Windows](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



