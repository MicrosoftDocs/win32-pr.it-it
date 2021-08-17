---
title: Supporto DRM in DirectShow
description: Supporto DRM in DirectShow
ms.assetid: f464d4a4-3478-489a-b9ce-8ab1acabc3c8
keywords:
- Windows Media Format SDK, supporto DRM in DirectShow
- Windows Media Format SDK,DirectShow
- Windows Media Format SDK, Digital Rights Management (DRM)
- Advanced Systems Format (ASF), supporto DRM in DirectShow
- ASF (Advanced Systems Format), supporto DRM in DirectShow
- Advanced Systems Format (ASF), DirectShow
- ASF (Advanced Systems Format), DirectShow
- Advanced Systems Format (ASF), Digital Rights Management (DRM)
- ASF (Advanced Systems Format),Digital Rights Management (DRM)
- DirectShow, supporto DRM
- DRM (Digital Rights Management), DirectShow
- DRM (Digital Rights Management),DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4b3de3ca80d1b3b2fe27c9af590fe0cba0202b1fdd9b6fc322d8ed1c1871536
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119930881"
---
# <a name="drm-support-in-directshow"></a>Supporto DRM in DirectShow

La lettura e la scrittura di file protetti da DRM in DirectShow vengono eseguite in modo sostanzialmente identico a quando si usa direttamente Windows Media Format SDK. Per iniziare, è necessaria la libreria statica wmstubdrm, ottenuta separatamente da Microsoft. È inoltre necessario implementare **l'interfaccia IKeyProvider** per consentire all'applicazione di accedere agli oggetti di run-time di Windows Media Format SDK quando DRM è abilitato.

Quando si applica la protezione DRM versione 1, usare l'interfaccia [**IWMHeaderInfo,**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) ottenuta come descritto in Lettura di [file ASF in DirectShow](reading-asf-files-in-directshow.md). Quando si applica la protezione DRM versione 7, ottenere l'interfaccia [**IWMDRMWriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter) chiamando **QueryService** sul filtro [WM ASF Writer,](wm-asf-writer-filter.md) come illustrato nel frammento di codice più avanti in questo argomento.

Tutte le altre configurazioni specifiche di DRM sono esattamente le stesse descritte in [Abilitazione del supporto DRM.](enabling-drm-support.md) Usare **QueryService per** ottenere [**l'interfaccia IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) dal filtro [lettore ASF WM.](wm-asf-reader-filter.md)

DirectX 9.0 contiene un esempio, PlayWndASF, un'applicazione lettore DirectShow abilitata per DRM che illustra l'acquisizione delle licenze DRM versione 1 e versione 7. Questo esempio include anche un'implementazione della **classe CKeyProvider,** che supporta l'interfaccia **IKeyProvider.**

 

 




