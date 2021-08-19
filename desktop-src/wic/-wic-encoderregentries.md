---
description: Encoder-Specific voci del Registro di sistema
ms.assetid: bbb78d70-bd3e-4d5a-ba59-2e17d2d1cf30
title: Encoder-Specific voci del Registro di sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83d5d91d917be3940bcece4bed7c224e0f281dbb1cade5d0dc2c25872f89af93
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118711230"
---
# <a name="encoder-specific-registry-entries"></a>Encoder-Specific voci del Registro di sistema


Oltre alle voci elencate in precedenza per il codificatore, è anche necessario registrare il codificatore nella categoria di codificatori wic (Windows Imaging Component) in modo che il motore di individuazione possa trovarlo. A tale scopo, creare le voci del Registro di sistema seguenti. Il primo GUID nelle voci seguenti è l'identificatore di categoria (CATID) per WICBitmapEncoders.

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

Se si crea un nuovo formato contenitore per il codec, è necessario creare anche voci del Registro di sistema per supportare i writer di metadati per i blocchi di metadati nelle immagini. Le voci seguenti devono essere create sotto l'identificatore di classe (CLSID) del writer di metadati per ogni formato di metadati supportato nel formato del contenitore. Se il codec usa un contenitore Tagged Image File Format (TIFF), queste informazioni sono già presenti nel Registro di sistema e non è necessario creare queste voci.

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

Se si usa un formato di contenitore in stile TIFF o JPEG, è necessario registrare un'associazione tra il contenitore e il formato del contenitore. Per altre informazioni, vedere l'introduzione in [Integrazione con Windows Raccolta foto e Windows Explorer.](-wic-integrationregentries.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Voci generali del Registro di sistema](-wic-generalregentries.md)
</dt> <dt>

[Voci del Registro di sistema specifiche del codificatore](-wic-decoderregentries.md)
</dt> <dt>

[Come scrivere un codec WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[Windows Panoramica del componente di creazione dell'immagine](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



