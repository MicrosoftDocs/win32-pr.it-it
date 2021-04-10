---
description: Implementazione di IWICBitmapCodecProgressNotification (encoder)
ms.assetid: d470ec93-d329-48c0-9556-0c15daece491
title: Implementazione di IWICBitmapCodecProgressNotification (encoder)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 260fac41068de0695813d569881e4a71938eb83d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883981"
---
# <a name="implementing-iwicbitmapcodecprogressnotification-encoder"></a>Implementazione di IWICBitmapCodecProgressNotification (encoder)

## <a name="iwicbitmapcodecprogressnotification"></a>IWICBitmapCodecProgressNotification

Sebbene l'interfaccia [**IWICBitmapCodecProgressNotification**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecprogressnotification) sia facoltativa, è consigliabile implementarla nella classe del codificatore a livello di contenitore. Questa interfaccia viene illustrata in dettaglio nell' [implementazione di IWICBitmapCodecProgressNotification (decodificatore)](-wic-imp-iwicbitmapcodecprogressnotification-decoder.md). L'implementazione è identica sia per il decodificatore che per il codificatore.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Implementazione di IWICBitmapEncoder](-wic-imp-iwicbitmapencoder.md)
</dt> <dt>

[Implementazione di IWICBitmapFrameEncode](-wic-imp-iwicbitmapframeencode.md)
</dt> <dt>

[Come scrivere un CODEC WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[Panoramica del componente imaging Windows](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Implementazione di IWICBitmapCodecProgressNotification (decodificatore)](-wic-imp-iwicbitmapcodecprogressnotification-decoder.md)
</dt> </dl>

 

 



