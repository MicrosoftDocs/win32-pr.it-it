---
description: Media Detector (MediaDet)
ms.assetid: 5cdbb6ca-d2c3-4123-b545-198863fed25f
title: Media Detector (MediaDet)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a072a5d70cf392a1b81fc8387d976bea1db2ddaa5ca2328df914be96a791d19
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119684971"
---
# <a name="media-detector-mediadet"></a>Media Detector (MediaDet)

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future Windows.\]

 

L'oggetto Media Detector (MediaDet) recupera le informazioni sul formato e ancora i fotogrammi dalle origini file. Media Detector non richiede il funzionamento di Filter Graph Manager. Per creare questo oggetto, chiamare **CoCreateInstance**. L'identificatore di classe è CLSID \_ MediaDet.

Per leggere Windows file ™, l'applicazione deve fornire un certificato software, denominato anche chiave. Registrare l'applicazione come provider di chiavi tramite **l'interfaccia IObjectWithSite** di Media Detector. Per altre informazioni, vedere [Unlocking the Windows Media Format SDK](unlocking-the-windows-media-format-sdk.md).

L'oggetto MediaDet espone le interfacce seguenti:

-   [**IMediaDet**](imediadet.md)
-   **IObjectWithSite**

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso delle origini](working-with-sources.md)
</dt> </dl>

 

 



