---
title: Supporto DRM in DirectShow
description: Supporto DRM in DirectShow
ms.assetid: f464d4a4-3478-489a-b9ce-8ab1acabc3c8
keywords:
- Windows Media Format SDK, supporto DRM in DirectShow
- Windows Media Format SDK, DirectShow
- Windows Media Format SDK, Digital Rights Management (DRM)
- ASF (Advanced Systems Format), supporto DRM in DirectShow
- ASF (Advanced Systems Format), supporto DRM in DirectShow
- ASF (Advanced Systems Format), DirectShow
- ASF (Advanced Systems Format), DirectShow
- ASF (Advanced Systems Format), Digital Rights Management (DRM)
- ASF (formato avanzato dei sistemi), Digital Rights Management (DRM)
- DirectShow, supporto DRM
- Digital Rights Management (DRM), DirectShow
- DRM (Digital Rights Management), DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85a211a3d3b438bac246c0bd90759f648818ac2e
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "103956177"
---
# <a name="drm-support-in-directshow"></a>Supporto DRM in DirectShow

La lettura e la scrittura di file protetti da DRM in DirectShow viene eseguita in modo sostanzialmente analogo a quando si utilizza direttamente Windows Media Format SDK. Per iniziare, è necessaria la libreria statica WMStubDRM, ottenuta separatamente da Microsoft. Inoltre, è necessario implementare l'interfaccia **IKeyProvider** per consentire all'applicazione di accedere agli oggetti runtime di Windows Media Format SDK quando è abilitato DRM.

Quando si applica la protezione DRM versione 1, usare l'interfaccia [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) , ottenuta come descritto nella pagina relativa alla [lettura di file ASF in DirectShow](reading-asf-files-in-directshow.md). Quando si applica la protezione DRM versione 7, ottenere l'interfaccia [**IWMDRMWriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter) chiamando **QueryService** sul filtro del [writer ASF WM](wm-asf-writer-filter.md) , come illustrato nel frammento di codice più avanti in questo argomento.

Tutte le altre configurazioni specifiche di DRM sono identiche a quelle descritte in [Abilitazione del supporto DRM](enabling-drm-support.md). Usare **QueryService** per ottenere l'interfaccia [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) dal filtro del [lettore WM ASF](wm-asf-reader-filter.md) .

DirectX 9,0 contiene un esempio, PlayWndASF, un'applicazione DirectShow Player abilitata per DRM che illustra l'acquisizione di licenze DRM versione 1 e 7. Questo esempio include anche un'implementazione della classe **CKeyProvider** , che supporta l'interfaccia **IKeyProvider** .

 

 




