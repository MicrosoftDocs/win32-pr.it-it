---
description: Media Detector (MediaDet)
ms.assetid: 5cdbb6ca-d2c3-4123-b545-198863fed25f
title: Media Detector (MediaDet)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90f34b1dc267480d3d6ea9efe9b9a743623a917b
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "104132174"
---
# <a name="media-detector-mediadet"></a>Media Detector (MediaDet)

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

L'oggetto Media Detector (MediaDet) recupera le informazioni sul formato e comunque i frame dalle origini file. Il rilevatore multimediale non richiede la gestione del grafo del filtro per funzionare. Per creare questo oggetto, chiamare **CoCreateInstance**. L'identificatore di classe è CLSID \_ mediadet.

Per leggere i file di Windows Media™, l'applicazione deve fornire un certificato software, detto anche chiave. Registrare l'applicazione come provider di chiavi tramite l'interfaccia **IObjectWithSite** del detector multimediale. Per ulteriori informazioni, vedere [sblocco di Windows Media Format SDK](unlocking-the-windows-media-format-sdk.md).

L'oggetto MediaDet espone le interfacce seguenti:

-   [**IMediaDet**](imediadet.md)
-   **IObjectWithSite**

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Utilizzo di origini](working-with-sources.md)
</dt> </dl>

 

 



