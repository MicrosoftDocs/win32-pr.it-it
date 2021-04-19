---
description: Voci generali del registro di sistema
ms.assetid: 6a140c7f-df8c-4a8e-9e4d-dbb38901e14f
title: Voci generali del registro di sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d7c3514adcc0aeaaf9adadd2b71dfdffcd8d408
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314473"
---
# <a name="general-registry-entries"></a>Voci generali del registro di sistema


Le seguenti voci del registro di sistema devono essere effettuate separatamente per il decodificatore e il codificatore:

```
HKEY_CLASSES_ROOT
   CLSID
      {Your Encoder/Decoder CLSID}
         Author = Author's Name
         Description = Your Codec Description
         DeviceManufacturer = Manufacturer's Name
         DeviceModels = Device,Device
         FriendlyName = Codec Friendly Name
         Date = mm-dd-yyyy
         Vendor = {GUID_Vendor}
         ContainerFormat = {GUID_ContainerFormat}
         Version = Major.Minor.Build.Number
         SpecVersion = Major.Minor.Build.Number
         MimeTypes = Your Mime Type
         SupportAnimation = 0|1
         SupportChromakey = 0|1
         SupportLossless = 0|1
         SupportMultiframe = 0|1
         Formats
            {Supported PixelFormat GUID 1}
            {Supported PixelFormat GUID ...}
            {Supported PixelFormat GUID N}
         ArbitrationPriority  = 0-10
```

Sono necessarie le voci FriendlyName, VendorGUID, ContainerFormat, MimeTypes, FileExtensions e formats. Tutte le altre sono facoltative.

Si noti che le voci DeviceManufacturer e DeviceModels sono specifiche dei codec non elaborati e fanno riferimento al produttore della fotocamera e ai modelli di fotocamera a cui è applicabile il codec. La versione delle specifiche è la versione della specifica del formato di immagine con cui è conforme il codec. La voce formats specifica i formati di pixel supportati dal codec. Un codec può supportare più di un formato pixel. In tal caso, immettere più chiavi in HKEY \_ classi \_ radice \\ CLSID \\ {codificatore/decodificatore CLSID} \\ formati.

## <a name="arbitrationpriority"></a>ArbitrationPriority

A partire da Windows 8, ArbitrationPriority è una nuova voce del registro di sistema. I valori validi sono compresi tra 0 e 10. Quando la chiave ArbitrationPriority è presente, il valore di questa chiave indicherà a WIC di classificare in ordine di priorità il codec associato dietro qualsiasi altro codec con un valore ArbitrationPriority più basso. Questa valutazione si verifica prima che venga eseguito l'arbitraggio di codec WIC esistente e garantisce che il codec associato venga classificato in ordine di priorità sotto qualsiasi codec in competizione, anche se è più idoneo. Qualsiasi codec che non dispone di un valore ArbitrationPriority esplicito definito nel registro di sistema avrà come valore predefinito la priorità 0.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Installazione e registrazione di CODEC](-wic-codecinstallandreg.md)
</dt> <dt>

[Voci del registro di sistema specifiche del codificatore](-wic-encoderregentries.md)
</dt> <dt>

[Come scrivere un CODEC WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[Panoramica del componente imaging Windows](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[**Funzionamento del componente Windows Imaging: individuazione e arbitraggio dei codec**](-wic-howwicworks.md)
</dt> </dl>

 

 



